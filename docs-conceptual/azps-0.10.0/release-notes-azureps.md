---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ab367ed41c77629122d6a4a9a79b96c7c66d09cb
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427584"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="07f67-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="07f67-103">Azure PowerShell release notes</span></span>
## <a name="0100-preview---april-2020"></a><span data-ttu-id="07f67-104">0.10.0-preview - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="07f67-104">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="07f67-105">일반</span><span class="sxs-lookup"><span data-stu-id="07f67-105">General</span></span>
* <span data-ttu-id="07f67-106">이제 Az 모듈이 Azure Stack Hub에서 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-106">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="07f67-107">따라서 Linux 및 macOS와의 플랫폼 간 호환성이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-107">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="07f67-108">Azure Stack Hub는 이제 Az 모듈을 사용하여 PowerShell Core를 지원합니다. 자세한 내용은 [여기](/azure-stack/operator/powershell-install-az-module)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-108">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="07f67-109">Az 모듈은 2019-03-01-hybrid 프로필을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-109">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="07f67-110">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="07f67-110">Az.Billing</span></span>
  - <span data-ttu-id="07f67-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-111">Az.Compute</span></span>
  - <span data-ttu-id="07f67-112">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="07f67-112">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="07f67-113">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="07f67-113">Az.EventHub</span></span>
  - <span data-ttu-id="07f67-114">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="07f67-114">Az.IotHub</span></span>
  - <span data-ttu-id="07f67-115">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07f67-115">Az.KeyVault</span></span>
  - <span data-ttu-id="07f67-116">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-116">Az.Monitor</span></span>
  - <span data-ttu-id="07f67-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-117">Az.Network</span></span>
  - <span data-ttu-id="07f67-118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-118">Az.Resources</span></span>
  - <span data-ttu-id="07f67-119">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-119">Az.Storage</span></span>
  - <span data-ttu-id="07f67-120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-120">Az.Websites</span></span>
* <span data-ttu-id="07f67-121">Azure Stack Hub와 함께 작동하는 az용 새 PowerShell 모듈 3개(Az.Databox, Az.IotHub 및 Az.EventHub)가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-121">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="07f67-122">AzureRM을 Az로 변경하는 것과 같은 사소한 변경을 수행하면 명령이 비교적 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-122">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="07f67-123">Azure Stack Hub에 대한 PowerShell 설명서의 업데이트된 링크는 [여기](/azure-stack/operator/powershell-install-az-module)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-123">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="07f67-124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-124">Az.Accounts</span></span>
* <span data-ttu-id="07f67-125">ADAL에서 MSAL로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="07f67-125">Upgrade from ADAL to MSAL</span></span>


## <a name="370---march-2020"></a><span data-ttu-id="07f67-126">3.7.0 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="07f67-126">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-127">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-127">Az.Accounts</span></span>
* <span data-ttu-id="07f67-128">로그인하지 않을 때 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault'에서 NullReferenceException이 발생하는 문제가 해결되었습니다. [# 10292]</span><span class="sxs-lookup"><span data-stu-id="07f67-128">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-129">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-129">Az.Compute</span></span>
* <span data-ttu-id="07f67-130">'New-AzDiskConfig' cmdlet에 다음 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-130">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="07f67-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="07f67-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="07f67-132">암호화 속성이 'New-AzGalleryImageVersion'cmdlet의 대상 매개 변수에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-132">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="07f67-133">'Set-AzVmss'-Reimage 및 'Invoke-AzVMReimage'cmdlet에 대한 tempDisk 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-133">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="07f67-134">[#11354]</span><span class="sxs-lookup"><span data-stu-id="07f67-134">[#11354]</span></span>
* <span data-ttu-id="07f67-135">새로운 SAP 확장을 위해 아래 cmdlet에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-135">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="07f67-136">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="07f67-136">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="07f67-137">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="07f67-137">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="07f67-138">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="07f67-138">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="07f67-139">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="07f67-139">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="07f67-140">도움말 문서의 예제에서 오류가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-140">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="07f67-141">VM PowerState의 정확한 문자열 값을 테이블 형식으로 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-141">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="07f67-142">'New-AzVmssConfig': SinglePlacementGroup이 비활성화된 경우 AutomaticRepairs 속성의 직렬화가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-142">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="07f67-143">[#11257]</span><span class="sxs-lookup"><span data-stu-id="07f67-143">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-144">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-144">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-145">ADF .Net SDK 버전이 4.8.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-145">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="07f67-146">재실행을 지원하기 위해 'Invoke-AzDataFactoryV2Pipeline' 명령에 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-146">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-147">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-147">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-148">'Export-AzDataLakeStoreItem' 및 'Import-AzDataLakeStoreItem'에 대해 호환성이 손상되는 변경 설명을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-148">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="07f67-149">'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' 및 'Get-AzDAtaLakeStoreItemContent'에 대한 바이트 인코딩 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-149">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="07f67-150">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="07f67-150">Az.HDInsight</span></span>
* <span data-ttu-id="07f67-151">클러스터 생성 시 최소 지원 TLS 버전 지정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-151">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="07f67-152">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="07f67-152">Az.IotHub</span></span>
* <span data-ttu-id="07f67-153">디바이스별 분산 설정을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-153">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="07f67-154">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-154">New Cmdlets are:</span></span>
    - <span data-ttu-id="07f67-155">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="07f67-155">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="07f67-156">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="07f67-156">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="07f67-157">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07f67-157">Az.KeyVault</span></span>
* <span data-ttu-id="07f67-158">'New-AzKeyVault'에 대해 호환성이 손상되는 변경 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-158">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="07f67-159">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-159">Az.Monitor</span></span>
* <span data-ttu-id="07f67-160">'New-AzScheduledQueryRuleLogMetricTrigger'에 대한 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-160">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-161">Az.Network</span></span>
* <span data-ttu-id="07f67-162">교차 테넌트 VirtualHubVnetConnections를 허용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-162">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="07f67-163">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="07f67-163">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="07f67-164">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="07f67-164">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="07f67-165">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="07f67-165">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="07f67-166">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="07f67-166">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="07f67-167">SQL Management SDK 종속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-167">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="07f67-168">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-168">Az.PolicyInsights</span></span>
* <span data-ttu-id="07f67-169">오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-169">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-170">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-171">Azure Site Recovery는 Azure 디스크 암호화 Virtual Machines에 대한 VM 속성을 다시 보호하고 업데이트하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-171">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="07f67-172">Azure Site Recovery VmwareToAzure 속성 DR 모니터링이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-172">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="07f67-173">Azure Backup은 실패한 항목에 대한 정책 업데이트 재시도 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-173">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="07f67-174">Azure Backup은 백업 및 복원 중에 디스크 제외 설정에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-174">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="07f67-175">Azure Backup은 AzureFileShare에서 여러 파일/폴더 복원을 위한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-175">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="07f67-176">Azure Backup은 IaasVM 정책을 업데이트하는 동안 사용자 지정 리소스 그룹 지원에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-176">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-177">Az.Resources</span></span>
* <span data-ttu-id="07f67-178">'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType'이 기본 apiVersion 대신 실제 apiVersion 리소스를 사용하도록 수정했습니다. [# 11267]</span><span class="sxs-lookup"><span data-stu-id="07f67-178">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="07f67-179">오류 시나리오에 대해 correlationId 로깅이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-179">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="07f67-180">작은 설명서가 'Get-AzResourceLock'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-180">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="07f67-181">예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-181">Added example.</span></span>
* <span data-ttu-id="07f67-182">'Get-AzADUser'의 매개 변수 값에서 작은 따옴표를 이스케이프 처리하였습니다. [# 11317]</span><span class="sxs-lookup"><span data-stu-id="07f67-182">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="07f67-183">배포 스크립트('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')에 대한 새로운 cmdlet 추가가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-183">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-184">Az.Sql</span></span>
* <span data-ttu-id="07f67-185">'Invoke-AzSqlDatabaseFailover'에 읽기 가능한 보조 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-185">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="07f67-186">'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-186">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="07f67-187">데이터베이스에서 열을 분류할 때 저장된 민감도 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-187">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="07f67-188">Az.Support</span><span class="sxs-lookup"><span data-stu-id="07f67-188">Az.Support</span></span>
* <span data-ttu-id="07f67-189">'Az.Support' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="07f67-189">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-190">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-190">Az.Websites</span></span>
* <span data-ttu-id="07f67-191">아래의 새로운 cmdlet을 통해 webapp 트래픽 라우팅 규칙을 사용하는 작업에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-191">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="07f67-192">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="07f67-192">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="07f67-193">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="07f67-193">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="07f67-194">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="07f67-194">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="07f67-195">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="07f67-195">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="07f67-196">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="07f67-196">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-197">Az.Accounts</span></span>
* <span data-ttu-id="07f67-198">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="07f67-198">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="07f67-199">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="07f67-199">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="07f67-200">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-200">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="07f67-201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07f67-201">Az.ApiManagement</span></span>
* <span data-ttu-id="07f67-202">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="07f67-202">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="07f67-203">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="07f67-203">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="07f67-204">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-204">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="07f67-205">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="07f67-205">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-206">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-206">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-207">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-207">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="07f67-208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="07f67-208">Az.IotHub</span></span>
* <span data-ttu-id="07f67-209">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-209">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="07f67-210">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-210">New Cmdlets are:</span></span>
    - <span data-ttu-id="07f67-211">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="07f67-211">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="07f67-212">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="07f67-212">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="07f67-213">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="07f67-213">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="07f67-214">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="07f67-214">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="07f67-215">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-215">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="07f67-216">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-216">New Cmdlets are:</span></span>
    - <span data-ttu-id="07f67-217">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="07f67-217">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="07f67-218">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="07f67-218">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="07f67-219">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="07f67-219">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="07f67-220">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="07f67-220">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="07f67-221">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-221">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="07f67-222">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-222">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="07f67-223">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-223">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="07f67-224">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-224">New Cmdlets are:</span></span>
    - <span data-ttu-id="07f67-225">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="07f67-225">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="07f67-226">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="07f67-226">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="07f67-227">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-227">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="07f67-228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-228">Az.Monitor</span></span>
* <span data-ttu-id="07f67-229">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="07f67-229">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-230">Az.Network</span></span>
* <span data-ttu-id="07f67-231">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-231">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="07f67-232">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-232">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="07f67-233">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-233">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="07f67-234">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-234">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-235">Az.Resources</span></span>
* <span data-ttu-id="07f67-236">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-236">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="07f67-237">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="07f67-237">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="07f67-238">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="07f67-238">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="07f67-239">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="07f67-239">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="07f67-240">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-240">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="07f67-241">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-241">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="07f67-242">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-242">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="07f67-243">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-243">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="07f67-244">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f67-244">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="07f67-245">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f67-245">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="07f67-246">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f67-246">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="07f67-247">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-247">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="07f67-248">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f67-248">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="07f67-249">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-249">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-250">Az.Sql</span></span>
* <span data-ttu-id="07f67-251">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-251">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="07f67-252">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-252">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="07f67-253">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-253">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="07f67-254">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-254">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="07f67-255">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-255">Remove an LTR backup</span></span>
    - <span data-ttu-id="07f67-256">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-256">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="07f67-257">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-257">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="07f67-258">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-258">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="07f67-259">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-259">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-260">Az.Storage</span></span>
* <span data-ttu-id="07f67-261">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-261">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="07f67-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="07f67-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="07f67-263">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-263">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="07f67-264">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="07f67-264">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="07f67-265">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="07f67-265">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-266">Az.Websites</span></span>
* <span data-ttu-id="07f67-267">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-267">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="07f67-268">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-268">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="07f67-269">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-269">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="07f67-270">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-270">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="07f67-271">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-271">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="07f67-272">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="07f67-272">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="07f67-273">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="07f67-273">Highlights since the last major release</span></span>
* <span data-ttu-id="07f67-274">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-274">Updated client side telemetry.</span></span>
* <span data-ttu-id="07f67-275">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-275">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="07f67-276">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-276">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="07f67-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-277">Az.Accounts</span></span>
* <span data-ttu-id="07f67-278">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-278">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="07f67-279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-279">Az.Automation</span></span>
* <span data-ttu-id="07f67-280">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-280">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="07f67-281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="07f67-281">Az.CognitiveServices</span></span>
* <span data-ttu-id="07f67-282">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-282">Updated SDK to 7.0</span></span>
* <span data-ttu-id="07f67-283">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-283">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-284">Az.Compute</span></span>
* <span data-ttu-id="07f67-285">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-285">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="07f67-286">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="07f67-286">Az.FrontDoor</span></span>
* <span data-ttu-id="07f67-287">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-287">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="07f67-288">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="07f67-288">Az.IotHub</span></span>
* <span data-ttu-id="07f67-289">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-289">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="07f67-290">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-290">New Cmdlets are:</span></span>
    - <span data-ttu-id="07f67-291">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="07f67-291">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="07f67-292">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="07f67-292">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="07f67-293">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="07f67-293">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="07f67-294">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="07f67-294">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="07f67-295">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07f67-295">Az.KeyVault</span></span>
* <span data-ttu-id="07f67-296">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-296">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="07f67-297">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-297">Az.Monitor</span></span>
* <span data-ttu-id="07f67-298">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-298">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="07f67-299">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-299">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="07f67-300">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-300">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-301">Az.Network</span></span>
* <span data-ttu-id="07f67-302">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-302">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="07f67-303">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-303">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="07f67-304">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-304">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="07f67-305">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="07f67-305">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="07f67-306">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-306">No new cmdlets are added.</span></span> <span data-ttu-id="07f67-307">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-307">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-308">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-309">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-309">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-310">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-310">Az.Resources</span></span>
* <span data-ttu-id="07f67-311">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-311">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="07f67-312">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-312">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="07f67-313">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-313">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="07f67-314">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-314">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="07f67-315">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-315">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="07f67-316">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-316">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="07f67-317">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-317">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="07f67-318">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-318">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-319">Az.Sql</span></span>
* <span data-ttu-id="07f67-320">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-320">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="07f67-321">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-321">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="07f67-322">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-322">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="07f67-323">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="07f67-323">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="07f67-324">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-324">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="07f67-325">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="07f67-325">Az.StorageSync</span></span>
* <span data-ttu-id="07f67-326">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-326">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="07f67-327">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="07f67-327">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="07f67-328">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="07f67-328">Highlights since the last major release</span></span>
* <span data-ttu-id="07f67-329">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="07f67-329">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="07f67-330">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-330">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="07f67-331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-331">Az.Accounts</span></span>
* <span data-ttu-id="07f67-332">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="07f67-332">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="07f67-333">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-333">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="07f67-334">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07f67-334">Az.ApiManagement</span></span>
* <span data-ttu-id="07f67-335">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="07f67-335">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="07f67-336">**New-AzApiManagementProduct** _ 및 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="07f67-336">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="07f67-337"> https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-337">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="07f67-338">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-338">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-339">Az.Compute</span></span>
* <span data-ttu-id="07f67-340">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="07f67-340">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="07f67-341">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-341">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="07f67-342">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="07f67-342">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="07f67-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="07f67-344">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-344">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-345">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-346">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-346">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="07f67-347">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="07f67-347">Az.DeploymentManager</span></span>
* <span data-ttu-id="07f67-348">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-348">Adds LIST operations for resources</span></span>
* <span data-ttu-id="07f67-349">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-349">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="07f67-350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="07f67-350">Az.HDInsight</span></span>
* <span data-ttu-id="07f67-351">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-351">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="07f67-352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07f67-352">Az.KeyVault</span></span>
* <span data-ttu-id="07f67-353">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-353">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-354">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-354">Az.Network</span></span>
* <span data-ttu-id="07f67-355">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-355">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="07f67-356">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="07f67-356">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="07f67-357">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="07f67-357">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="07f67-358">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-358">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="07f67-359">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="07f67-359">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="07f67-360">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-360">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="07f67-361">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-361">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="07f67-362">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-362">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="07f67-363">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-363">New cmdlets added:</span></span>
        - <span data-ttu-id="07f67-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="07f67-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="07f67-365">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="07f67-365">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="07f67-366">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="07f67-366">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="07f67-367">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-367">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="07f67-368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-368">Az.PolicyInsights</span></span>
* <span data-ttu-id="07f67-369">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-369">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="07f67-370">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-370">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="07f67-371">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-371">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="07f67-372">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-372">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-373">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-373">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-374">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-374">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="07f67-375">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-375">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-376">Az.Resources</span></span>
* <span data-ttu-id="07f67-377">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="07f67-377">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="07f67-378">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-378">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-379">Az.Sql</span></span>
<span data-ttu-id="07f67-380">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-380">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-381">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-381">Az.Storage</span></span>
* <span data-ttu-id="07f67-382">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-382">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="07f67-383">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-383">New-AzStorageAccount</span></span>
* <span data-ttu-id="07f67-384">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="07f67-384">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="07f67-385">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-385">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-386">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-386">Az.Websites</span></span>
* <span data-ttu-id="07f67-387">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-387">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="07f67-388">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-388">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="07f67-389">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="07f67-389">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-390">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-390">Az.Accounts</span></span>
* <span data-ttu-id="07f67-391">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-391">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="07f67-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="07f67-392">Az.Cdn</span></span>
* <span data-ttu-id="07f67-393">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="07f67-393">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-394">Az.Compute</span></span>
* <span data-ttu-id="07f67-395">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-395">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="07f67-396">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="07f67-396">Az.ContainerInstance</span></span>
* <span data-ttu-id="07f67-397">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="07f67-397">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="07f67-398">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="07f67-398">Az.DataBoxEdge</span></span>
* <span data-ttu-id="07f67-399">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-399">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="07f67-400">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="07f67-400">Get the Edge Storage Container</span></span>
* <span data-ttu-id="07f67-401">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-401">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="07f67-402">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="07f67-402">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="07f67-403">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-403">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="07f67-404">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-404">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="07f67-405">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-405">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="07f67-406">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="07f67-406">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="07f67-407">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-407">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="07f67-408">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="07f67-408">Get the Edge Storage Account</span></span>
* <span data-ttu-id="07f67-409">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-409">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="07f67-410">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="07f67-410">Create new Edge Storage Account</span></span>
* <span data-ttu-id="07f67-411">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-411">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="07f67-412">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-412">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="07f67-413">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="07f67-413">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="07f67-414">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="07f67-414">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="07f67-415">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-415">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="07f67-416">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="07f67-416">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-417">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-417">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-418">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-418">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="07f67-419">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-419">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="07f67-420">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-420">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="07f67-421">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="07f67-421">Az.DevTestLabs</span></span>
* <span data-ttu-id="07f67-422">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-422">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="07f67-423">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="07f67-423">Az.EventHub</span></span>
* <span data-ttu-id="07f67-424">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-424">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="07f67-425">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="07f67-425">Az.HDInsight</span></span>
* <span data-ttu-id="07f67-426">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-426">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="07f67-427">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="07f67-427">Az.MachineLearning</span></span>
* <span data-ttu-id="07f67-428">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-428">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="07f67-429">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="07f67-429">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="07f67-430">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="07f67-430">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="07f67-431">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="07f67-431">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="07f67-432">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="07f67-432">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="07f67-433">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="07f67-433">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="07f67-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="07f67-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="07f67-435">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="07f67-435">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-436">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-436">Az.Network</span></span>
* <span data-ttu-id="07f67-437">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="07f67-437">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-439">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-439">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="07f67-440">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-440">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="07f67-441">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-441">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="07f67-442">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-442">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-443">Az.Resources</span></span>
* <span data-ttu-id="07f67-444">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-444">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-445">Az.Sql</span></span>
* <span data-ttu-id="07f67-446">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-446">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="07f67-447">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-447">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="07f67-448">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="07f67-448">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="07f67-449">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-449">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-450">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-450">Az.Storage</span></span>
* <span data-ttu-id="07f67-451">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-451">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="07f67-452">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="07f67-452">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="07f67-453">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-453">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="07f67-454">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-454">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="07f67-455">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="07f67-455">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="07f67-456">일반</span><span class="sxs-lookup"><span data-stu-id="07f67-456">General</span></span>
* <span data-ttu-id="07f67-457">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-457">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="07f67-458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-458">Az.Accounts</span></span>
* <span data-ttu-id="07f67-459">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="07f67-459">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="07f67-460">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="07f67-460">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="07f67-461">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="07f67-461">Az.Batch</span></span>
* <span data-ttu-id="07f67-462">**New-AzBatchPool** 이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-462">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-463">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-463">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-464">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-464">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="07f67-465">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="07f67-465">Az.FrontDoor</span></span>
* <span data-ttu-id="07f67-466">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-466">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="07f67-467">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-467">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="07f67-468">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="07f67-468">Az.HealthcareApis</span></span>
* <span data-ttu-id="07f67-469">예외 처리</span><span class="sxs-lookup"><span data-stu-id="07f67-469">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="07f67-470">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07f67-470">Az.KeyVault</span></span>
* <span data-ttu-id="07f67-471">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-471">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="07f67-472">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="07f67-472">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="07f67-473">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-473">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="07f67-474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-474">Az.Monitor</span></span>
* <span data-ttu-id="07f67-475">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-475">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="07f67-476">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="07f67-476">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="07f67-477">나타냄</span><span class="sxs-lookup"><span data-stu-id="07f67-477">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-478">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-478">Az.Network</span></span>
* <span data-ttu-id="07f67-479">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="07f67-479">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-480">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-480">Az.Resources</span></span>
* <span data-ttu-id="07f67-481">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="07f67-481">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="07f67-482">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="07f67-482">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-483">Az.Sql</span></span>
* <span data-ttu-id="07f67-484">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="07f67-484">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-485">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-485">Az.Storage</span></span>
* <span data-ttu-id="07f67-486">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-486">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="07f67-487">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="07f67-487">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="07f67-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="07f67-488">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="07f67-489">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-489">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="07f67-490">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="07f67-490">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="07f67-491">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="07f67-491">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="07f67-492">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-492">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="07f67-493">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="07f67-493">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="07f67-494">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="07f67-494">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="07f67-495">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-495">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="07f67-496">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="07f67-496">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="07f67-497">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-497">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="07f67-498">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="07f67-498">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="07f67-499">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="07f67-499">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="07f67-500">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="07f67-500">Highlights since the last major release</span></span>
* <span data-ttu-id="07f67-501">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="07f67-501">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="07f67-502">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="07f67-502">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-503">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-503">Az.Compute</span></span>
* <span data-ttu-id="07f67-504">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="07f67-504">VM Reapply feature</span></span>
    - <span data-ttu-id="07f67-505">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-505">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="07f67-506">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="07f67-506">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="07f67-507">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="07f67-507">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="07f67-508">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-508">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="07f67-509">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-509">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="07f67-510">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-510">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="07f67-511">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="07f67-511">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="07f67-512">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-512">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="07f67-513">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-513">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="07f67-514">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-514">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="07f67-515">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="07f67-515">Az.DataBoxEdge</span></span>
* <span data-ttu-id="07f67-516">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-516">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="07f67-517">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="07f67-517">Get the Order</span></span>
* <span data-ttu-id="07f67-518">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-518">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="07f67-519">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="07f67-519">Create new Order</span></span>
* <span data-ttu-id="07f67-520">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-520">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="07f67-521">주문 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-521">Remove the Order</span></span>
* <span data-ttu-id="07f67-522">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="07f67-522">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="07f67-523">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="07f67-523">Now creates Local Share</span></span>
* <span data-ttu-id="07f67-524">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-524">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="07f67-525">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="07f67-525">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="07f67-526">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-526">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="07f67-527">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="07f67-527">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="07f67-528">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-528">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="07f67-529">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="07f67-529">Gets the information about Triggers</span></span>
* <span data-ttu-id="07f67-530">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-530">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="07f67-531">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="07f67-531">Create new Triggers</span></span>
* <span data-ttu-id="07f67-532">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-532">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="07f67-533">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-533">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-534">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-535">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-535">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="07f67-536">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-536">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-537">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-537">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-538">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-538">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="07f67-539">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="07f67-539">Az.EventHub</span></span>
* <span data-ttu-id="07f67-540">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-540">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="07f67-541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="07f67-541">Az.FrontDoor</span></span>
* <span data-ttu-id="07f67-542">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-542">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="07f67-543">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-543">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="07f67-544">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-544">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="07f67-545">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="07f67-545">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-546">Az.Network</span></span>
* <span data-ttu-id="07f67-547">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-547">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="07f67-548">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="07f67-548">Az.PrivateDns</span></span>
* <span data-ttu-id="07f67-549">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="07f67-549">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-551">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-551">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="07f67-552">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-552">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="07f67-553">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-553">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="07f67-554">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="07f67-554">Az.RedisCache</span></span>
* <span data-ttu-id="07f67-555">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-555">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="07f67-556">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-556">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="07f67-557">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-557">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-558">Az.Resources</span></span>
- <span data-ttu-id="07f67-559">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-559">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="07f67-560">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-560">Updated create policy definition help example</span></span>
- <span data-ttu-id="07f67-561">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-561">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="07f67-562">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-562">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="07f67-563">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-563">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-564">Az.Sql</span></span>
* <span data-ttu-id="07f67-565">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-565">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="07f67-566">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-566">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="07f67-567">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="07f67-567">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="07f67-568">일반</span><span class="sxs-lookup"><span data-stu-id="07f67-568">General</span></span>
* <span data-ttu-id="07f67-569">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="07f67-569">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="07f67-570">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-570">Az.Accounts</span></span>
* <span data-ttu-id="07f67-571">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-571">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="07f67-572">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="07f67-572">Az.Advisor</span></span>
* <span data-ttu-id="07f67-573">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-573">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="07f67-574">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="07f67-574">Az.Batch</span></span>
* <span data-ttu-id="07f67-575">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-575">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="07f67-576">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-576">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="07f67-577">이 변경 사항은 **Get-AzBatchAccount** 에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-577">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="07f67-578">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-578">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="07f67-579">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-579">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="07f67-580">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask** 에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-580">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="07f67-581">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-581">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="07f67-582">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-582">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="07f67-583">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-583">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="07f67-584">**Get-AzBatchApplication** 으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-584">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="07f67-585">이제 **Get-AzBatchApplicationPackage** 를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-585">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="07f67-586">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="07f67-586">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="07f67-587">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication** 에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-587">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="07f67-588">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-588">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="07f67-589">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-589">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="07f67-590">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-590">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="07f67-591">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-591">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="07f67-592">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-592">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="07f67-593">**Set-AzBatchPoolOSVersion** 이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-593">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="07f67-594">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-594">This operation is no longer supported.</span></span>
* <span data-ttu-id="07f67-595">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-595">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="07f67-596">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-596">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="07f67-597">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-597">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="07f67-598">**Get-AzBatchNodeAgentSku** 가 제거되고 **Get-AzBatchSupportedImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-598">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="07f67-599">**Get-AzBatchSupportedImage** 가 **Get-AzBatchNodeAgentSku** 와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-599">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="07f67-600">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-600">New non-verified images are also now returned.</span></span> <span data-ttu-id="07f67-601">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-601">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="07f67-602">**New-AzBatchPool** 의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-602">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="07f67-603">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-603">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="07f67-604">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-604">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="07f67-605">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-605">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="07f67-606">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-606">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="07f67-607">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-607">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="07f67-608">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-608">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="07f67-609">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="07f67-609">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="07f67-610">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="07f67-610">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="07f67-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="07f67-611">Az.Cdn</span></span>
* <span data-ttu-id="07f67-612">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-612">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="07f67-613">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-613">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-614">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-614">Az.Compute</span></span>
* <span data-ttu-id="07f67-615">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="07f67-615">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="07f67-616">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="07f67-616">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="07f67-617">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="07f67-617">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="07f67-618">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-618">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="07f67-619">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-619">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="07f67-620">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="07f67-620">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="07f67-621">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-621">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="07f67-622">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="07f67-622">Breaking changes</span></span>
    - <span data-ttu-id="07f67-623">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-623">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="07f67-624">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-624">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-625">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-625">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-626">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-626">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-627">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-627">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-628">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="07f67-628">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="07f67-629">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-629">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="07f67-630">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="07f67-630">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="07f67-631">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-631">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="07f67-632">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-632">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="07f67-633">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-633">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="07f67-634">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="07f67-634">Az.FrontDoor</span></span>
* <span data-ttu-id="07f67-635">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-635">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="07f67-636">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="07f67-636">Az.HDInsight</span></span>
* <span data-ttu-id="07f67-637">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-637">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="07f67-638">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-638">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="07f67-639">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="07f67-639">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="07f67-640">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-640">Removed five cmdlets:</span></span>
    - <span data-ttu-id="07f67-641">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="07f67-641">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="07f67-642">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="07f67-642">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="07f67-643">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="07f67-643">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="07f67-644">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="07f67-644">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="07f67-645">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="07f67-645">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="07f67-646">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-646">Added three cmdlets:</span></span>
    - <span data-ttu-id="07f67-647">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="07f67-647">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="07f67-648">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="07f67-648">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="07f67-649">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="07f67-649">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="07f67-650">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-650">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="07f67-651">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-651">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="07f67-652">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-652">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="07f67-653">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-653">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="07f67-654">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-654">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="07f67-655">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-655">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="07f67-656">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-656">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="07f67-657">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-657">Added some scenario test cases.</span></span>
* <span data-ttu-id="07f67-658">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="07f67-658">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="07f67-659">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="07f67-659">Az.IotHub</span></span>
* <span data-ttu-id="07f67-660">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="07f67-660">Breaking changes:</span></span>
    - <span data-ttu-id="07f67-661">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-661">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="07f67-662">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-662">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="07f67-663">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-663">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="07f67-664">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-664">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="07f67-665">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-665">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="07f67-666">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-666">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="07f67-667">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-667">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="07f67-668">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-668">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="07f67-669">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-669">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="07f67-670">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-670">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="07f67-671">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-671">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="07f67-672">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-672">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-673">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-673">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-674">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-674">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="07f67-675">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-675">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="07f67-676">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-676">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="07f67-677">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-677">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="07f67-678">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-678">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="07f67-679">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-679">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="07f67-680">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-680">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="07f67-681">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-681">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="07f67-682">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-682">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-683">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-683">Az.Resources</span></span>
* <span data-ttu-id="07f67-684">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-684">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-685">Az.Network</span></span>
* <span data-ttu-id="07f67-686">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-686">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="07f67-687">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="07f67-687">Updated cmdlet:</span></span>
        - <span data-ttu-id="07f67-688">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-688">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="07f67-689">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-689">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="07f67-690">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-690">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="07f67-691">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-691">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="07f67-692">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-692">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="07f67-693">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-693">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="07f67-694">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="07f67-694">New cmdlet:</span></span>
        - <span data-ttu-id="07f67-695">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="07f67-695">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="07f67-696">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-696">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="07f67-697">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-697">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="07f67-698">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-698">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="07f67-699">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-699">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="07f67-700">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-700">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="07f67-701">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-701">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="07f67-702">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-702">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="07f67-703">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-703">New cmdlets added:</span></span>
        - <span data-ttu-id="07f67-704">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="07f67-704">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="07f67-705">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="07f67-705">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="07f67-706">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="07f67-706">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="07f67-707">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="07f67-707">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="07f67-708">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="07f67-708">Set-AzVirtualHub</span></span>
* <span data-ttu-id="07f67-709">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-709">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="07f67-710">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="07f67-711">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="07f67-711">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="07f67-712">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="07f67-712">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="07f67-713">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="07f67-713">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="07f67-714">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="07f67-714">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="07f67-715">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-715">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="07f67-716">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-716">New cmdlets added:</span></span>
        - <span data-ttu-id="07f67-717">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-717">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="07f67-718">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-718">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="07f67-719">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="07f67-719">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="07f67-720">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="07f67-720">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="07f67-721">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="07f67-721">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="07f67-722">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="07f67-722">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="07f67-723">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="07f67-723">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="07f67-724">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-724">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="07f67-725">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-725">New cmdlets added:</span></span>
        - <span data-ttu-id="07f67-726">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="07f67-726">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="07f67-727">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="07f67-727">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="07f67-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="07f67-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="07f67-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="07f67-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="07f67-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="07f67-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="07f67-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="07f67-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="07f67-732">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-732">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="07f67-733">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="07f67-733">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="07f67-734">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-734">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="07f67-735">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-735">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="07f67-736">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-736">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="07f67-737">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-737">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="07f67-738">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="07f67-738">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="07f67-739">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="07f67-739">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="07f67-740">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-740">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="07f67-741">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-741">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="07f67-742">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-742">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="07f67-743">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-743">New cmdlets added:</span></span>
        - <span data-ttu-id="07f67-744">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="07f67-744">New-AzIpGroup</span></span>
        - <span data-ttu-id="07f67-745">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="07f67-745">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="07f67-746">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="07f67-746">Get-AzIpGroup</span></span>
        - <span data-ttu-id="07f67-747">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="07f67-747">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="07f67-748">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07f67-748">Az.ServiceFabric</span></span>
* <span data-ttu-id="07f67-749">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-749">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-750">Az.Sql</span></span>
* <span data-ttu-id="07f67-751">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-751">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="07f67-752">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-752">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="07f67-753">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-753">Removed deprecated aliases:</span></span>
* <span data-ttu-id="07f67-754">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="07f67-754">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="07f67-755">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="07f67-755">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="07f67-756">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-756">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="07f67-757">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-757">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="07f67-758">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="07f67-758">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="07f67-759">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-759">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-760">Az.Storage</span></span>
* <span data-ttu-id="07f67-761">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-761">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="07f67-762">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-762">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="07f67-763">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-763">Set-AzStorageAccount</span></span>
* <span data-ttu-id="07f67-764">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-764">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="07f67-765">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="07f67-765">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="07f67-766">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="07f67-766">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="07f67-767">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="07f67-767">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="07f67-768">일반</span><span class="sxs-lookup"><span data-stu-id="07f67-768">General</span></span>
* <span data-ttu-id="07f67-769">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="07f67-769">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="07f67-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-770">Az.Accounts</span></span>
* <span data-ttu-id="07f67-771">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-771">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="07f67-772">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07f67-772">Az.ApiManagement</span></span>
* <span data-ttu-id="07f67-773">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-773">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="07f67-774">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-774">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="07f67-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-775">Az.Automation</span></span>
* <span data-ttu-id="07f67-776">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-776">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="07f67-777">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="07f67-777">Az.Batch</span></span>
* <span data-ttu-id="07f67-778">**Get-AzBatchNodeAgentSku** 가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-778">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-779">Az.Compute</span></span>
* <span data-ttu-id="07f67-780">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-780">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="07f67-781">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-781">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="07f67-782">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-782">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="07f67-783">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-783">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-784">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-785">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-785">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="07f67-786">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-786">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="07f67-787">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-787">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-788">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-788">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-789">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-789">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="07f67-790">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="07f67-790">Az.HealthcareApis</span></span>
* <span data-ttu-id="07f67-791">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-791">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="07f67-792">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-792">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="07f67-793">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-793">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="07f67-794">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-794">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="07f67-795">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="07f67-795">Az.IotHub</span></span>
* <span data-ttu-id="07f67-796">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="07f67-796">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="07f67-797">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-797">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="07f67-798">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-798">Az.Monitor</span></span>
* <span data-ttu-id="07f67-799">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-799">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="07f67-800">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-800">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="07f67-801">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-801">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="07f67-802">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-802">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-803">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-803">Az.Network</span></span>
* <span data-ttu-id="07f67-804">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-804">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="07f67-805">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-805">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="07f67-806">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-806">New cmdlets added:</span></span>
        - <span data-ttu-id="07f67-807">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="07f67-807">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="07f67-808">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-808">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="07f67-809">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-809">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="07f67-810">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-810">Updated cmdlets:</span></span>
        - <span data-ttu-id="07f67-811">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-811">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="07f67-812">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-812">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="07f67-813">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-813">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="07f67-814">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-814">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="07f67-815">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="07f67-815">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="07f67-816">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-816">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="07f67-817">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-817">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="07f67-818">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="07f67-818">Az.RedisCache</span></span>
* <span data-ttu-id="07f67-819">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-819">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-820">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-820">Az.Sql</span></span>
* <span data-ttu-id="07f67-821">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-821">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-822">Az.Storage</span></span>
* <span data-ttu-id="07f67-823">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-823">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="07f67-824">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-824">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="07f67-825">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="07f67-825">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="07f67-826">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-826">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="07f67-827">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-827">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="07f67-828">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="07f67-828">Az.StorageSync</span></span>
* <span data-ttu-id="07f67-829">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-829">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-830">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-830">Az.Websites</span></span>
* <span data-ttu-id="07f67-831">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-831">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="07f67-832">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="07f67-832">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="07f67-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07f67-833">Az.ApiManagement</span></span>
* <span data-ttu-id="07f67-834">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-834">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="07f67-835">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-835">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="07f67-836">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-836">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="07f67-837">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-837">Az.Automation</span></span>
* <span data-ttu-id="07f67-838">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-838">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="07f67-839">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-839">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="07f67-840">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-840">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-841">Az.Compute</span></span>
* <span data-ttu-id="07f67-842">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-842">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="07f67-843">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-843">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="07f67-844">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-844">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="07f67-845">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-845">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="07f67-846">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-846">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="07f67-847">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-847">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="07f67-848">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-848">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="07f67-849">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-849">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="07f67-850">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-850">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-851">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-851">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-852">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-852">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="07f67-853">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-853">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="07f67-854">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="07f67-854">Az.HDInsight</span></span>
* <span data-ttu-id="07f67-855">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="07f67-855">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="07f67-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="07f67-856">Az.IotHub</span></span>
* <span data-ttu-id="07f67-857">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-857">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="07f67-858">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-858">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="07f67-859">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-859">New cmdlets are:</span></span>
    - <span data-ttu-id="07f67-860">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="07f67-860">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="07f67-861">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="07f67-861">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="07f67-862">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="07f67-862">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="07f67-863">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="07f67-863">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="07f67-864">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-864">Az.Monitor</span></span>
* <span data-ttu-id="07f67-865">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-865">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="07f67-866">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-866">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="07f67-867">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-867">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="07f67-868">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01** 이고, 이전에는 **2018-03-01** 였습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-868">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="07f67-869">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-869">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="07f67-870">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema** 라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-870">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="07f67-871">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false** 로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-871">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="07f67-872">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-872">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="07f67-873">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-873">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="07f67-874">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-874">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="07f67-875">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-875">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="07f67-876">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-876">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="07f67-877">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-877">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="07f67-878">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-878">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="07f67-879">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-879">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="07f67-880">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="07f67-880">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="07f67-881">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-881">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="07f67-882">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="07f67-882">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="07f67-883">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-883">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="07f67-884">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-884">Overall improved help files</span></span>
* <span data-ttu-id="07f67-885">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-885">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-886">Az.Network</span></span>
* <span data-ttu-id="07f67-887">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-887">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="07f67-888">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-888">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="07f67-889">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-889">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="07f67-890">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-890">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="07f67-891">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-891">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="07f67-892">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-892">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="07f67-893">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-893">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="07f67-894">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-894">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="07f67-895">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-895">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="07f67-896">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-896">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="07f67-897">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-897">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="07f67-898">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-898">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="07f67-899">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-899">New cmdlets</span></span>
        - <span data-ttu-id="07f67-900">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="07f67-900">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="07f67-901">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-901">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="07f67-902">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="07f67-902">Updated cmdlet:</span></span>
        - <span data-ttu-id="07f67-903">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="07f67-903">New-VpnSite</span></span>
        - <span data-ttu-id="07f67-904">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="07f67-904">Update-VpnSite</span></span>
        - <span data-ttu-id="07f67-905">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-905">New-VpnConnection</span></span>
        - <span data-ttu-id="07f67-906">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-906">Update-VpnConnection</span></span>
* <span data-ttu-id="07f67-907">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-907">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-908">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-908">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-909">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-909">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="07f67-910">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-910">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-911">Az.Resources</span></span>
* <span data-ttu-id="07f67-912">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-912">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="07f67-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07f67-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="07f67-914">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-914">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="07f67-915">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-915">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="07f67-916">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="07f67-916">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="07f67-917">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="07f67-917">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="07f67-918">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="07f67-918">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="07f67-919">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="07f67-919">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="07f67-920">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="07f67-920">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="07f67-921">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="07f67-921">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="07f67-922">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="07f67-922">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="07f67-923">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="07f67-923">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="07f67-924">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="07f67-924">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="07f67-925">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="07f67-925">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="07f67-926">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="07f67-926">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="07f67-927">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="07f67-927">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="07f67-928">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="07f67-928">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="07f67-929">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-929">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="07f67-930">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="07f67-930">Az.SignalR</span></span>
* <span data-ttu-id="07f67-931">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-931">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-932">Az.Sql</span></span>
* <span data-ttu-id="07f67-933">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-933">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="07f67-934">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="07f67-934">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="07f67-935">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-935">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="07f67-936">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-936">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="07f67-937">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="07f67-937">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-938">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-938">Az.Storage</span></span>
* <span data-ttu-id="07f67-939">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-939">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="07f67-940">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-940">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="07f67-941">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="07f67-941">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="07f67-942">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="07f67-942">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="07f67-943">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-943">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="07f67-944">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="07f67-944">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="07f67-945">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-945">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="07f67-946">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="07f67-946">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="07f67-947">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="07f67-947">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="07f67-948">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="07f67-948">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="07f67-949">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="07f67-949">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-950">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-950">Az.Websites</span></span>
* <span data-ttu-id="07f67-951">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-951">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="07f67-952">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-952">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="07f67-953">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-953">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="07f67-954">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="07f67-954">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="07f67-955">일반</span><span class="sxs-lookup"><span data-stu-id="07f67-955">General</span></span>
* <span data-ttu-id="07f67-956">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-956">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="07f67-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-957">Az.Accounts</span></span>
* <span data-ttu-id="07f67-958">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="07f67-958">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="07f67-959">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="07f67-959">Az.Aks</span></span>
* <span data-ttu-id="07f67-960">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="07f67-960">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="07f67-961">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-961">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="07f67-962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07f67-962">Az.ApiManagement</span></span>
* <span data-ttu-id="07f67-963">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-963">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="07f67-964">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-964">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="07f67-965">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-965">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="07f67-966">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="07f67-966">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="07f67-967">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-967">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="07f67-968">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="07f67-968">Az.Batch</span></span>
* <span data-ttu-id="07f67-969">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-969">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="07f67-970">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="07f67-970">Az.Cdn</span></span>
* <span data-ttu-id="07f67-971">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-971">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-972">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-972">Az.Compute</span></span>
* <span data-ttu-id="07f67-973">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-973">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="07f67-974">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-974">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="07f67-975">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-975">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="07f67-976">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-976">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="07f67-977">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="07f67-977">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="07f67-978">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-978">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="07f67-979">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-979">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="07f67-980">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-980">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-981">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-982">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-982">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="07f67-983">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-983">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="07f67-984">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-984">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="07f67-985">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-985">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-986">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-987">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-987">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="07f67-988">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="07f67-988">Az.EventHub</span></span>
* <span data-ttu-id="07f67-989">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="07f67-989">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="07f67-990">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="07f67-990">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="07f67-991">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-991">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="07f67-992">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="07f67-992">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="07f67-993">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="07f67-993">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="07f67-994">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-994">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="07f67-995">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-995">Az.Monitor</span></span>
* <span data-ttu-id="07f67-996">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-996">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-997">Az.Network</span></span>
* <span data-ttu-id="07f67-998">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-998">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="07f67-999">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="07f67-999">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="07f67-1000">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1000">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="07f67-1001">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1001">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="07f67-1002">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1002">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="07f67-1003">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1003">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="07f67-1004">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1004">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="07f67-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="07f67-1006">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1006">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="07f67-1007">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1007">Added example</span></span>
    - <span data-ttu-id="07f67-1008">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1008">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="07f67-1009">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1009">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="07f67-1010">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1010">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-1011">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1011">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-1012">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1012">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1013">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1013">Az.Resources</span></span>
* <span data-ttu-id="07f67-1014">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1014">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="07f67-1015">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1015">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="07f67-1016">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1016">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="07f67-1017">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1017">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="07f67-1018">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07f67-1018">Az.ServiceBus</span></span>
* <span data-ttu-id="07f67-1019">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="07f67-1019">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="07f67-1020">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="07f67-1020">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="07f67-1021">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1021">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="07f67-1022">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07f67-1022">Az.ServiceFabric</span></span>
* <span data-ttu-id="07f67-1023">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="07f67-1023">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="07f67-1024">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="07f67-1024">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="07f67-1025">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="07f67-1025">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="07f67-1026">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1026">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="07f67-1027">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="07f67-1027">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="07f67-1028">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="07f67-1028">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1029">Az.Sql</span></span>
* <span data-ttu-id="07f67-1030">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1030">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-1031">Az.Storage</span></span>
* <span data-ttu-id="07f67-1032">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1032">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="07f67-1033">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1033">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="07f67-1034">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="07f67-1034">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="07f67-1035">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="07f67-1035">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="07f67-1036">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1036">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="07f67-1037">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="07f67-1037">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-1038">Az.Websites</span></span>
* <span data-ttu-id="07f67-1039">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1039">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="07f67-1040">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="07f67-1040">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1041">Az.Accounts</span></span>
* <span data-ttu-id="07f67-1042">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1042">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="07f67-1043">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-1043">Az.ApplicationInsights</span></span>
* <span data-ttu-id="07f67-1044">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1044">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="07f67-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-1045">Az.Automation</span></span>
* <span data-ttu-id="07f67-1046">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1046">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="07f67-1047">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1047">Az.CognitiveServices</span></span>
* <span data-ttu-id="07f67-1048">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1048">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1049">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1049">Az.Compute</span></span>
* <span data-ttu-id="07f67-1050">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1050">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="07f67-1051">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="07f67-1051">Az.ContainerRegistry</span></span>
* <span data-ttu-id="07f67-1052">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1052">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="07f67-1053">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1053">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-1054">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-1054">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-1055">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1055">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="07f67-1056">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1056">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="07f67-1057">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="07f67-1057">Az.EventHub</span></span>
* <span data-ttu-id="07f67-1058">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="07f67-1058">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="07f67-1059">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1059">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="07f67-1060">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07f67-1060">Az.KeyVault</span></span>
* <span data-ttu-id="07f67-1061">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1061">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="07f67-1062">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="07f67-1062">Az.LogicApp</span></span>
* <span data-ttu-id="07f67-1063">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1063">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="07f67-1064">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1064">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="07f67-1065">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1065">Az.ManagedServices</span></span>
* <span data-ttu-id="07f67-1066">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1066">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-1067">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1067">Az.Network</span></span>
* <span data-ttu-id="07f67-1068">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1068">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="07f67-1069">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-1069">New cmdlets</span></span>
        - <span data-ttu-id="07f67-1070">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="07f67-1070">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="07f67-1071">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="07f67-1071">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="07f67-1072">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-1072">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="07f67-1073">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-1073">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="07f67-1074">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-1074">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="07f67-1075">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-1075">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="07f67-1076">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="07f67-1076">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="07f67-1077">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="07f67-1077">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="07f67-1078">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="07f67-1078">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="07f67-1079">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-1079">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="07f67-1080">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1080">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="07f67-1081">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1081">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="07f67-1082">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1082">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="07f67-1083">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="07f67-1083">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="07f67-1084">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1084">Updated cmdlets</span></span>
        - <span data-ttu-id="07f67-1085">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-1085">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="07f67-1086">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-1086">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="07f67-1087">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-1087">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="07f67-1088">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1088">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="07f67-1089">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1089">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="07f67-1090">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="07f67-1090">Updated cmdlet:</span></span>
        - <span data-ttu-id="07f67-1091">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-1091">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="07f67-1092">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-1092">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="07f67-1093">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-1093">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="07f67-1094">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1094">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="07f67-1095">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1095">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="07f67-1096">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1096">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="07f67-1097">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-1097">Az.OperationalInsights</span></span>
* <span data-ttu-id="07f67-1098">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1098">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="07f67-1099">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1099">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-1100">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1100">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-1101">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1101">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="07f67-1102">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1102">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="07f67-1103">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1103">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="07f67-1104">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1104">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="07f67-1105">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1105">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="07f67-1106">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1106">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="07f67-1107">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1107">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="07f67-1108">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1108">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="07f67-1109">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1109">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="07f67-1110">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1110">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1111">Az.Resources</span></span>
- <span data-ttu-id="07f67-1112">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-1112">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="07f67-1113">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1113">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="07f67-1114">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07f67-1114">Az.ServiceBus</span></span>
* <span data-ttu-id="07f67-1115">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="07f67-1115">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="07f67-1116">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1116">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1117">Az.Sql</span></span>
* <span data-ttu-id="07f67-1118">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1118">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="07f67-1119">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1119">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="07f67-1120">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1120">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-1121">Az.Storage</span></span>
* <span data-ttu-id="07f67-1122">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="07f67-1122">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="07f67-1123">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="07f67-1123">Az.StorageSync</span></span>
* <span data-ttu-id="07f67-1124">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1124">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="07f67-1125">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1125">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-1126">Az.Websites</span></span>
* <span data-ttu-id="07f67-1127">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1127">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="07f67-1128">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1128">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="07f67-1129">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1129">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="07f67-1130">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="07f67-1130">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-1131">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1131">Az.Accounts</span></span>
* <span data-ttu-id="07f67-1132">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1132">Add support for profile cmdlets</span></span>
* <span data-ttu-id="07f67-1133">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1133">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="07f67-1134">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1134">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="07f67-1135">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="07f67-1135">Az.Advisor</span></span>
* <span data-ttu-id="07f67-1136">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="07f67-1136">GA release of Az.Advisor</span></span>
* <span data-ttu-id="07f67-1137">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1137">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="07f67-1138">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07f67-1138">Az.ApiManagement</span></span>
* <span data-ttu-id="07f67-1139">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1139">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="07f67-1140">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="07f67-1140">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="07f67-1141">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1141">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="07f67-1142">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1142">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="07f67-1143">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1143">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="07f67-1144">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="07f67-1144">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="07f67-1145">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1145">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="07f67-1146">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-1146">Az.Automation</span></span>
* <span data-ttu-id="07f67-1147">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1147">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1148">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1148">Az.Compute</span></span>
* <span data-ttu-id="07f67-1149">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1149">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-1150">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-1151">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1151">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="07f67-1152">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="07f67-1152">Az.EventGrid</span></span>
* <span data-ttu-id="07f67-1153">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1153">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="07f67-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="07f67-1154">Az.IotHub</span></span>
* <span data-ttu-id="07f67-1155">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1155">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1156">Az.Network</span></span>
* <span data-ttu-id="07f67-1157">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="07f67-1157">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="07f67-1158">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="07f67-1158">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="07f67-1159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-1159">Az.PolicyInsights</span></span>
* <span data-ttu-id="07f67-1160">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="07f67-1160">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="07f67-1161">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1161">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="07f67-1162">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-1162">Az.OperationalInsights</span></span>
* <span data-ttu-id="07f67-1163">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1163">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-1165">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1165">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1166">Az.Resources</span></span>
    - <span data-ttu-id="07f67-1167">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1167">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="07f67-1168">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1168">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="07f67-1169">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1169">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="07f67-1170">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1170">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="07f67-1171">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07f67-1171">Az.ServiceBus</span></span>
* <span data-ttu-id="07f67-1172">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="07f67-1172">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1173">Az.Sql</span></span>
* <span data-ttu-id="07f67-1174">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1174">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="07f67-1175">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1175">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="07f67-1176">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="07f67-1176">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="07f67-1177">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="07f67-1177">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="07f67-1178">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="07f67-1178">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="07f67-1179">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="07f67-1179">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="07f67-1180">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="07f67-1180">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="07f67-1181">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="07f67-1181">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="07f67-1182">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-1182">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-1183">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-1183">Az.Storage</span></span>
* <span data-ttu-id="07f67-1184">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1184">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="07f67-1185">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="07f67-1185">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="07f67-1186">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1186">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="07f67-1187">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="07f67-1187">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="07f67-1188">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1188">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="07f67-1189">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-1189">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="07f67-1190">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-1190">Set-AzStorageAccount</span></span>
* <span data-ttu-id="07f67-1191">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="07f67-1191">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="07f67-1192">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="07f67-1192">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="07f67-1193">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="07f67-1193">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="07f67-1194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="07f67-1194">Az.StorageSync</span></span>
* <span data-ttu-id="07f67-1195">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1195">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="07f67-1196">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="07f67-1196">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-1197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1197">Az.Accounts</span></span>
* <span data-ttu-id="07f67-1198">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1198">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="07f67-1199">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1199">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="07f67-1200">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="07f67-1200">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="07f67-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="07f67-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="07f67-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="07f67-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1203">Az.Compute</span></span>
* <span data-ttu-id="07f67-1204">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1204">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="07f67-1205">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1205">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="07f67-1206">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="07f67-1206">Az.Dns</span></span>
* <span data-ttu-id="07f67-1207">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1207">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="07f67-1208">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="07f67-1208">Az.EventGrid</span></span>
* <span data-ttu-id="07f67-1209">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1209">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="07f67-1210">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="07f67-1210">New cmdlets:</span></span>
    - <span data-ttu-id="07f67-1211">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="07f67-1211">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="07f67-1212">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1212">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="07f67-1213">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="07f67-1213">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="07f67-1214">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1214">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="07f67-1215">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="07f67-1215">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="07f67-1216">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1216">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="07f67-1217">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="07f67-1217">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="07f67-1218">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1218">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="07f67-1219">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="07f67-1219">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="07f67-1220">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1220">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="07f67-1221">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="07f67-1221">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="07f67-1222">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1222">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="07f67-1223">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="07f67-1223">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="07f67-1224">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1224">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="07f67-1225">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="07f67-1225">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="07f67-1226">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1226">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="07f67-1227">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1227">Updated cmdlets:</span></span>
    - <span data-ttu-id="07f67-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="07f67-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="07f67-1229">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1229">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="07f67-1230">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1230">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="07f67-1231">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1231">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="07f67-1232">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1232">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="07f67-1233">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="07f67-1233">Event subscription expiration date,</span></span>
            - <span data-ttu-id="07f67-1234">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="07f67-1234">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="07f67-1235">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1235">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="07f67-1236">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="07f67-1236">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="07f67-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="07f67-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="07f67-1238">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1238">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="07f67-1239">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="07f67-1239">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="07f67-1240">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1240">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="07f67-1241">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1241">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="07f67-1242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="07f67-1242">Az.FrontDoor</span></span>
* <span data-ttu-id="07f67-1243">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="07f67-1243">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="07f67-1244">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1244">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="07f67-1245">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="07f67-1245">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="07f67-1246">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1246">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-1247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1247">Az.Network</span></span>
* <span data-ttu-id="07f67-1248">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1248">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="07f67-1249">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-1249">New cmdlets</span></span>
        - <span data-ttu-id="07f67-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="07f67-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="07f67-1251">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1251">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="07f67-1252">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-1252">New cmdlets</span></span>
        - <span data-ttu-id="07f67-1253">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="07f67-1253">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="07f67-1254">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1254">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="07f67-1255">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-1255">New cmdlets</span></span>
        - <span data-ttu-id="07f67-1256">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="07f67-1256">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="07f67-1257">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="07f67-1257">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="07f67-1258">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="07f67-1258">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="07f67-1259">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-1259">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="07f67-1260">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-1260">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="07f67-1261">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1261">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="07f67-1262">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-1262">New cmdlets</span></span>
        - <span data-ttu-id="07f67-1263">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="07f67-1263">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="07f67-1264">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="07f67-1264">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="07f67-1265">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="07f67-1265">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="07f67-1266">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="07f67-1266">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="07f67-1267">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="07f67-1267">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="07f67-1268">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1268">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="07f67-1269">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1269">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="07f67-1270">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1270">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="07f67-1271">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1271">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="07f67-1272">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1272">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="07f67-1273">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1273">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="07f67-1274">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1274">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="07f67-1275">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1275">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="07f67-1276">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1276">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="07f67-1277">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1277">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="07f67-1278">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1278">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="07f67-1279">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1279">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="07f67-1280">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1280">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="07f67-1281">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="07f67-1281">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="07f67-1282">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1282">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="07f67-1283">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1283">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="07f67-1284">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="07f67-1284">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="07f67-1285">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="07f67-1285">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="07f67-1286">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1286">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="07f67-1287">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1287">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="07f67-1288">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1288">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="07f67-1289">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1289">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="07f67-1290">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-1290">Az.OperationalInsights</span></span>
* <span data-ttu-id="07f67-1291">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="07f67-1291">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1292">Az.Resources</span></span>
* <span data-ttu-id="07f67-1293">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1293">Support for additional Template Export options</span></span>
    - <span data-ttu-id="07f67-1294">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1294">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="07f67-1295">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1295">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="07f67-1296">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1296">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="07f67-1297">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07f67-1297">Az.ServiceFabric</span></span>
* <span data-ttu-id="07f67-1298">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1298">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1299">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1299">Az.Sql</span></span>
* <span data-ttu-id="07f67-1300">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1300">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="07f67-1301">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1301">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="07f67-1302">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1302">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="07f67-1303">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="07f67-1303">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="07f67-1304">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="07f67-1304">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="07f67-1305">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="07f67-1305">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="07f67-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="07f67-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="07f67-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="07f67-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-1308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-1308">Az.Storage</span></span>
* <span data-ttu-id="07f67-1309">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1309">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="07f67-1310">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-1310">New-AzStorageAccount</span></span>
* <span data-ttu-id="07f67-1311">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="07f67-1311">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="07f67-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="07f67-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-1313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-1313">Az.Websites</span></span>
* <span data-ttu-id="07f67-1314">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="07f67-1314">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="07f67-1315">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1315">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="07f67-1316">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="07f67-1316">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="07f67-1317">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="07f67-1317">Az.Cdn</span></span>
* <span data-ttu-id="07f67-1318">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1318">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1319">Az.Compute</span></span>
* <span data-ttu-id="07f67-1320">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1320">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="07f67-1321">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="07f67-1321">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="07f67-1322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="07f67-1322">Az.EventHub</span></span>
* <span data-ttu-id="07f67-1323">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="07f67-1323">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="07f67-1324">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="07f67-1324">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-1325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1325">Az.Network</span></span>
* <span data-ttu-id="07f67-1326">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1326">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="07f67-1327">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1327">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="07f67-1328">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-1328">Az.PolicyInsights</span></span>
* <span data-ttu-id="07f67-1329">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="07f67-1329">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-1330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1330">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-1331">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1331">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="07f67-1332">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07f67-1332">Az.ServiceBus</span></span>
* <span data-ttu-id="07f67-1333">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="07f67-1333">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="07f67-1334">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07f67-1334">Az.ServiceFabric</span></span>
* <span data-ttu-id="07f67-1335">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1335">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="07f67-1336">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1336">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1337">Az.Sql</span></span>
* <span data-ttu-id="07f67-1338">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1338">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="07f67-1339">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="07f67-1339">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="07f67-1340">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="07f67-1340">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="07f67-1341">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1341">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-1342">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-1342">Az.Websites</span></span>
* <span data-ttu-id="07f67-1343">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="07f67-1343">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="07f67-1344">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="07f67-1344">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="07f67-1345">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07f67-1345">Az.ApiManagement</span></span>
* <span data-ttu-id="07f67-1346">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1346">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="07f67-1347">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="07f67-1347">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="07f67-1348">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="07f67-1348">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="07f67-1349">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="07f67-1349">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="07f67-1350">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="07f67-1350">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="07f67-1351">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="07f67-1351">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="07f67-1352">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-1352">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="07f67-1353">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1353">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="07f67-1354">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1354">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="07f67-1355">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="07f67-1355">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="07f67-1356">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="07f67-1356">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="07f67-1357">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-1357">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="07f67-1358">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1358">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="07f67-1359">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1359">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="07f67-1360">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="07f67-1360">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="07f67-1361">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="07f67-1361">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="07f67-1362">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-1362">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="07f67-1363">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1363">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="07f67-1364">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1364">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="07f67-1365">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1365">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="07f67-1366">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1366">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="07f67-1367">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1367">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="07f67-1368">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1368">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="07f67-1369">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1369">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="07f67-1370">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1370">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="07f67-1371">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1371">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="07f67-1372">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1372">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="07f67-1373">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1373">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="07f67-1374">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1374">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="07f67-1375">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1375">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="07f67-1376">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1376">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="07f67-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="07f67-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="07f67-1378">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1378">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="07f67-1379">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1379">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="07f67-1380">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="07f67-1380">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="07f67-1381">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="07f67-1381">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="07f67-1382">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="07f67-1382">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="07f67-1383">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1383">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="07f67-1384">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1384">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="07f67-1385">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1385">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="07f67-1386">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="07f67-1386">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="07f67-1387">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="07f67-1387">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="07f67-1388">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="07f67-1388">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="07f67-1389">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="07f67-1389">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="07f67-1390">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1390">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="07f67-1391">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="07f67-1391">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="07f67-1392">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1392">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="07f67-1393">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="07f67-1393">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="07f67-1394">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1394">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="07f67-1395">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="07f67-1395">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="07f67-1396">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1396">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="07f67-1397">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="07f67-1397">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="07f67-1398">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="07f67-1398">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="07f67-1399">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1399">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="07f67-1400">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="07f67-1400">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="07f67-1401">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="07f67-1401">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="07f67-1402">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1402">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="07f67-1403">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="07f67-1403">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="07f67-1404">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="07f67-1404">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="07f67-1405">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1405">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="07f67-1406">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1406">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="07f67-1407">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="07f67-1407">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="07f67-1408">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="07f67-1408">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="07f67-1409">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1409">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="07f67-1410">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="07f67-1410">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="07f67-1411">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="07f67-1411">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="07f67-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="07f67-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="07f67-1413">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="07f67-1413">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="07f67-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="07f67-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="07f67-1415">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="07f67-1415">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="07f67-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="07f67-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="07f67-1417">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="07f67-1417">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="07f67-1418">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="07f67-1418">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="07f67-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="07f67-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="07f67-1420">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="07f67-1420">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="07f67-1421">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="07f67-1421">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="07f67-1422">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="07f67-1422">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="07f67-1423">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-1423">Az.Automation</span></span>
* <span data-ttu-id="07f67-1424">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1424">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="07f67-1425">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1425">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="07f67-1426">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1426">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="07f67-1427">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1427">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="07f67-1428">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1428">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="07f67-1429">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="07f67-1429">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="07f67-1430">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1430">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1431">Az.Compute</span></span>
* <span data-ttu-id="07f67-1432">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1432">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="07f67-1433">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1433">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-1434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-1434">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-1435">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1435">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="07f67-1436">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-1436">Az.Monitor</span></span>
* <span data-ttu-id="07f67-1437">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1437">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-1438">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1438">Az.Network</span></span>
* <span data-ttu-id="07f67-1439">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1439">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="07f67-1440">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="07f67-1440">Updated cmdlet:</span></span>
        - <span data-ttu-id="07f67-1441">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="07f67-1441">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="07f67-1442">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1442">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1443">Az.Resources</span></span>
* <span data-ttu-id="07f67-1444">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1444">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1445">Az.Sql</span></span>
* <span data-ttu-id="07f67-1446">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1446">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="07f67-1447">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="07f67-1447">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-1448">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1448">Az.Accounts</span></span>
* <span data-ttu-id="07f67-1449">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1449">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="07f67-1450">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1450">Az.CognitiveServices</span></span>
* <span data-ttu-id="07f67-1451">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1451">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="07f67-1452">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="07f67-1452">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1453">Az.Compute</span></span>
* <span data-ttu-id="07f67-1454">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="07f67-1454">Proximity placement group feature.</span></span>
    - <span data-ttu-id="07f67-1455">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="07f67-1455">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="07f67-1456">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-1456">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="07f67-1457">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1457">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="07f67-1458">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1458">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="07f67-1459">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1459">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="07f67-1460">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="07f67-1460">Breaking changes</span></span>
    - <span data-ttu-id="07f67-1461">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1461">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="07f67-1462">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1462">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="07f67-1463">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="07f67-1463">Az.DeploymentManager</span></span>
* <span data-ttu-id="07f67-1464">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="07f67-1464">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="07f67-1465">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="07f67-1465">Az.Dns</span></span>
* <span data-ttu-id="07f67-1466">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="07f67-1466">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="07f67-1467">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1467">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="07f67-1468">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1468">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="07f67-1469">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="07f67-1469">Az.FrontDoor</span></span>
* <span data-ttu-id="07f67-1470">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="07f67-1470">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="07f67-1471">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="07f67-1471">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="07f67-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="07f67-1472">Az.HDInsight</span></span>
* <span data-ttu-id="07f67-1473">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1473">Removed two cmdlets:</span></span>
    - <span data-ttu-id="07f67-1474">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="07f67-1474">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="07f67-1475">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="07f67-1475">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="07f67-1476">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1476">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="07f67-1477">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="07f67-1477">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="07f67-1478">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1478">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="07f67-1479">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1479">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="07f67-1480">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-1480">Az.Monitor</span></span>
* <span data-ttu-id="07f67-1481">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-1481">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="07f67-1482">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="07f67-1482">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="07f67-1483">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="07f67-1483">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="07f67-1484">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="07f67-1484">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="07f67-1485">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="07f67-1485">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="07f67-1486">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="07f67-1486">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="07f67-1487">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="07f67-1487">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="07f67-1488">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="07f67-1488">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="07f67-1489">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="07f67-1489">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="07f67-1490">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="07f67-1490">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="07f67-1491">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="07f67-1491">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="07f67-1492">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="07f67-1492">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="07f67-1493">SQR API에 대한 [자세한 내용](/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="07f67-1493">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="07f67-1494">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1494">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1495">Az.Network</span></span>
* <span data-ttu-id="07f67-1496">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1496">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="07f67-1497">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-1497">New cmdlets</span></span>
        - <span data-ttu-id="07f67-1498">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="07f67-1498">New-AzNatGateway</span></span>
        - <span data-ttu-id="07f67-1499">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="07f67-1499">Get-AzNatGateway</span></span>
        - <span data-ttu-id="07f67-1500">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="07f67-1500">Set-AzNatGateway</span></span>
        - <span data-ttu-id="07f67-1501">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="07f67-1501">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="07f67-1502">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1502">Updated cmdlets</span></span>
        - <span data-ttu-id="07f67-1503">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="07f67-1503">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="07f67-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="07f67-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="07f67-1505">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="07f67-1505">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="07f67-1506">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1506">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="07f67-1507">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1507">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="07f67-1508">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-1508">Az.PolicyInsights</span></span>
* <span data-ttu-id="07f67-1509">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1509">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="07f67-1510">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1510">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="07f67-1511">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1511">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-1512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1512">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-1513">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1513">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="07f67-1514">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="07f67-1514">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="07f67-1515">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1515">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="07f67-1516">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1516">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="07f67-1517">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1517">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="07f67-1518">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="07f67-1518">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="07f67-1519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="07f67-1519">Az.Relay</span></span>
* <span data-ttu-id="07f67-1520">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1520">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="07f67-1521">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07f67-1521">Az.ServiceBus</span></span>
* <span data-ttu-id="07f67-1522">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="07f67-1522">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-1523">Az.Storage</span></span>
* <span data-ttu-id="07f67-1524">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="07f67-1524">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="07f67-1525">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1525">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="07f67-1526">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1526">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="07f67-1527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-1527">New-AzStorageAccount</span></span>
* <span data-ttu-id="07f67-1528">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1528">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="07f67-1529">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-1529">New-AzStorageAccount</span></span>
    - <span data-ttu-id="07f67-1530">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-1530">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="07f67-1531">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f67-1531">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-1532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-1532">Az.Websites</span></span>
* <span data-ttu-id="07f67-1533">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1533">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="07f67-1534">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1534">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="07f67-1535">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="07f67-1535">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="07f67-1536">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="07f67-1536">Highlights since the last major release</span></span>
* <span data-ttu-id="07f67-1537">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="07f67-1537">General availability of `Az` module</span></span>
* <span data-ttu-id="07f67-1538">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1538">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="07f67-1539">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="07f67-1539">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="07f67-1540">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1540">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="07f67-1541">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1541">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="07f67-1542">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1542">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="07f67-1543">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1543">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="07f67-1544">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1544">Az.Accounts</span></span>
* <span data-ttu-id="07f67-1545">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1545">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="07f67-1546">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="07f67-1546">Az.Batch</span></span>
* <span data-ttu-id="07f67-1547">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="07f67-1548">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="07f67-1548">Az.Cdn</span></span>
* <span data-ttu-id="07f67-1549">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1549">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="07f67-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="07f67-1551">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1551">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1552">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1552">Az.Compute</span></span>
* <span data-ttu-id="07f67-1553">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1553">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="07f67-1554">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1554">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="07f67-1555">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1555">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-1556">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-1556">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-1557">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1557">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-1559">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1559">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="07f67-1560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="07f67-1560">Az.EventGrid</span></span>
* <span data-ttu-id="07f67-1561">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1561">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="07f67-1562">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="07f67-1562">Az.EventHub</span></span>
* <span data-ttu-id="07f67-1563">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="07f67-1563">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="07f67-1564">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="07f67-1564">Az.HDInsight</span></span>
* <span data-ttu-id="07f67-1565">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="07f67-1566">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="07f67-1566">Az.IotHub</span></span>
* <span data-ttu-id="07f67-1567">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="07f67-1568">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07f67-1568">Az.KeyVault</span></span>
* <span data-ttu-id="07f67-1569">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="07f67-1570">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1570">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="07f67-1571">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="07f67-1571">Az.MachineLearning</span></span>
* <span data-ttu-id="07f67-1572">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1572">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="07f67-1573">Az.Media</span><span class="sxs-lookup"><span data-stu-id="07f67-1573">Az.Media</span></span>
* <span data-ttu-id="07f67-1574">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="07f67-1575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-1575">Az.Monitor</span></span>
  * <span data-ttu-id="07f67-1576">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-1576">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="07f67-1577">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="07f67-1577">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="07f67-1578">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="07f67-1578">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="07f67-1579">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="07f67-1579">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="07f67-1580">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="07f67-1580">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="07f67-1581">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="07f67-1581">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="07f67-1582">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1582">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-1583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1583">Az.Network</span></span>
* <span data-ttu-id="07f67-1584">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1584">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="07f67-1585">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1585">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="07f67-1586">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="07f67-1586">Az.NotificationHubs</span></span>
* <span data-ttu-id="07f67-1587">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="07f67-1588">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-1588">Az.OperationalInsights</span></span>
* <span data-ttu-id="07f67-1589">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="07f67-1590">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="07f67-1590">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="07f67-1591">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1591">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-1593">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="07f67-1594">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1594">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="07f67-1595">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1595">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="07f67-1596">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1596">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="07f67-1597">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="07f67-1597">Az.RedisCache</span></span>
* <span data-ttu-id="07f67-1598">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1599">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1599">Az.Resources</span></span>
* <span data-ttu-id="07f67-1600">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1600">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1601">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1601">Az.Sql</span></span>
* <span data-ttu-id="07f67-1602">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1602">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="07f67-1603">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="07f67-1604">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1604">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="07f67-1605">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1605">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="07f67-1606">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1606">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="07f67-1607">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1607">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="07f67-1608">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1608">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-1609">Az.Websites</span></span>
* <span data-ttu-id="07f67-1610">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1610">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="07f67-1611">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="07f67-1612">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1612">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="07f67-1613">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1613">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="07f67-1614">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="07f67-1614">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="07f67-1615">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="07f67-1615">Highlights since the last major release</span></span>
* <span data-ttu-id="07f67-1616">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="07f67-1616">General availability of `Az` module</span></span>
* <span data-ttu-id="07f67-1617">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1617">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="07f67-1618">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="07f67-1618">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="07f67-1619">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1619">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="07f67-1620">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1620">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="07f67-1621">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1621">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="07f67-1622">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1622">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="07f67-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1623">Az.Accounts</span></span>
* <span data-ttu-id="07f67-1624">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1624">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="07f67-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1625">Az.AnalysisServices</span></span>
* <span data-ttu-id="07f67-1626">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-1626">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="07f67-1627">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="07f67-1627">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="07f67-1628">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-1628">Az.Automation</span></span>
* <span data-ttu-id="07f67-1629">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1629">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="07f67-1630">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="07f67-1630">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="07f67-1631">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1631">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1632">Az.Compute</span></span>
* <span data-ttu-id="07f67-1633">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1633">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="07f67-1634">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="07f67-1634">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="07f67-1635">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="07f67-1635">Az.ContainerInstance</span></span>
* <span data-ttu-id="07f67-1636">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1636">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-1637">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-1637">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-1638">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1638">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="07f67-1639">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1639">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1640">Az.Resources</span></span>
* <span data-ttu-id="07f67-1641">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="07f67-1641">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="07f67-1642">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="07f67-1642">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="07f67-1643">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="07f67-1643">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="07f67-1644">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1644">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="07f67-1645">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1645">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="07f67-1646">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1646">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1647">Az.Sql</span></span>
* <span data-ttu-id="07f67-1648">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1648">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-1649">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-1649">Az.Storage</span></span>
* <span data-ttu-id="07f67-1650">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="07f67-1650">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="07f67-1651">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="07f67-1651">New-AzStorageContext</span></span>
* <span data-ttu-id="07f67-1652">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1652">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="07f67-1653">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="07f67-1653">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="07f67-1654">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="07f67-1654">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="07f67-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="07f67-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="07f67-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="07f67-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="07f67-1657">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1657">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="07f67-1658">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="07f67-1658">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="07f67-1659">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="07f67-1659">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="07f67-1660">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="07f67-1660">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="07f67-1661">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="07f67-1661">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="07f67-1662">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="07f67-1662">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="07f67-1663">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="07f67-1663">Highlights since the last major release</span></span>
* <span data-ttu-id="07f67-1664">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="07f67-1664">General availability of `Az` module</span></span>
* <span data-ttu-id="07f67-1665">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1665">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="07f67-1666">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="07f67-1666">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="07f67-1667">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1667">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="07f67-1668">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1668">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="07f67-1669">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1669">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="07f67-1670">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1670">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="07f67-1671">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-1671">Az.Automation</span></span>
* <span data-ttu-id="07f67-1672">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1672">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="07f67-1673">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="07f67-1673">Dynamic grouping</span></span>
    * <span data-ttu-id="07f67-1674">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="07f67-1674">Pre-Post script</span></span>
    * <span data-ttu-id="07f67-1675">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="07f67-1675">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1676">Az.Compute</span></span>
* <span data-ttu-id="07f67-1677">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1677">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="07f67-1678">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1678">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="07f67-1679">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07f67-1679">Az.KeyVault</span></span>
* <span data-ttu-id="07f67-1680">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1680">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1681">Az.Network</span></span>
* <span data-ttu-id="07f67-1682">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1682">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="07f67-1683">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1683">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-1684">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1684">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-1685">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1685">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="07f67-1686">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1686">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1687">Az.Resources</span></span>
* <span data-ttu-id="07f67-1688">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1688">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="07f67-1689">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1689">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1690">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1690">Az.Sql</span></span>
* <span data-ttu-id="07f67-1691">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1691">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-1692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-1692">Az.Storage</span></span>
* <span data-ttu-id="07f67-1693">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1693">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="07f67-1694">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="07f67-1694">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="07f67-1695">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="07f67-1695">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="07f67-1696">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="07f67-1696">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="07f67-1697">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="07f67-1697">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="07f67-1698">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="07f67-1698">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="07f67-1699">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="07f67-1699">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-1700">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-1700">Az.Websites</span></span>
* <span data-ttu-id="07f67-1701">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1701">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="07f67-1702">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="07f67-1702">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-1703">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1703">Az.Accounts</span></span>
* <span data-ttu-id="07f67-1704">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1704">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="07f67-1705">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1705">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="07f67-1706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-1706">Az.Automation</span></span>
* <span data-ttu-id="07f67-1707">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1707">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="07f67-1708">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1708">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="07f67-1709">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="07f67-1709">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="07f67-1710">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="07f67-1710">Az.Cdn</span></span>
* <span data-ttu-id="07f67-1711">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1711">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1712">Az.Compute</span></span>
* <span data-ttu-id="07f67-1713">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1713">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-1714">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-1714">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-1715">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1715">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="07f67-1716">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="07f67-1716">Az.LogicApp</span></span>
* <span data-ttu-id="07f67-1717">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1717">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1718">Az.Network</span></span>
* <span data-ttu-id="07f67-1719">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1719">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-1720">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1720">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-1721">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1721">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="07f67-1722">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1722">SDK Update</span></span>
* <span data-ttu-id="07f67-1723">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-1723">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="07f67-1724">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1724">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1725">Az.Resources</span></span>
* <span data-ttu-id="07f67-1726">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="07f67-1726">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="07f67-1727">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1727">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="07f67-1728">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1728">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="07f67-1729">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1729">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="07f67-1730">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="07f67-1730">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="07f67-1731">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1731">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1732">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1732">Az.Sql</span></span>
* <span data-ttu-id="07f67-1733">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1733">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="07f67-1734">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1734">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-1735">Az.Storage</span></span>
* <span data-ttu-id="07f67-1736">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1736">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="07f67-1737">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="07f67-1737">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="07f67-1738">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1738">Az.AnalysisServices</span></span>
* <span data-ttu-id="07f67-1739">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-1739">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="07f67-1740">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-1740">Az.Automation</span></span>
* <span data-ttu-id="07f67-1741">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1741">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="07f67-1742">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1742">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="07f67-1743">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="07f67-1743">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="07f67-1744">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1744">Az.CognitiveServices</span></span>
* <span data-ttu-id="07f67-1745">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1745">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1746">Az.Compute</span></span>
* <span data-ttu-id="07f67-1747">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="07f67-1747">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="07f67-1748">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1748">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="07f67-1749">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1749">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="07f67-1750">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1750">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-1751">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-1751">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-1752">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1752">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="07f67-1753">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="07f67-1753">Az.EventHub</span></span>
* <span data-ttu-id="07f67-1754">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1754">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="07f67-1755">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07f67-1755">Az.KeyVault</span></span>
* <span data-ttu-id="07f67-1756">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1756">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="07f67-1757">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="07f67-1757">Az.LogicApp</span></span>
* <span data-ttu-id="07f67-1758">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1758">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="07f67-1759">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1759">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="07f67-1760">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-1760">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="07f67-1761">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="07f67-1761">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="07f67-1762">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="07f67-1762">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="07f67-1763">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="07f67-1763">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="07f67-1764">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="07f67-1764">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="07f67-1765">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-1765">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="07f67-1766">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="07f67-1766">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="07f67-1767">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="07f67-1767">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="07f67-1768">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="07f67-1768">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="07f67-1769">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="07f67-1769">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="07f67-1770">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1770">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="07f67-1771">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-1771">Az.Monitor</span></span>
* <span data-ttu-id="07f67-1772">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1772">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1773">Az.Network</span></span>
* <span data-ttu-id="07f67-1774">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1774">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="07f67-1775">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-1775">Az.OperationalInsights</span></span>
* <span data-ttu-id="07f67-1776">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1776">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="07f67-1777">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1777">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="07f67-1778">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1778">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1779">Az.Resources</span></span>
* <span data-ttu-id="07f67-1780">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1780">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="07f67-1781">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="07f67-1782">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1782">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="07f67-1783">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1783">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1784">Az.Sql</span></span>
* <span data-ttu-id="07f67-1785">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1785">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="07f67-1786">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1786">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-1787">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-1787">Az.Websites</span></span>
* <span data-ttu-id="07f67-1788">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="07f67-1788">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="07f67-1789">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="07f67-1789">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1790">Az.Accounts</span></span>
* <span data-ttu-id="07f67-1791">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1791">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="07f67-1792">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1792">Az.AnalysisServices</span></span>
<span data-ttu-id="07f67-1793">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="07f67-1793">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1794">Az.Compute</span></span>
* <span data-ttu-id="07f67-1795">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1795">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="07f67-1796">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1796">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="07f67-1797">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1797">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-1798">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1798">Az.RecoveryServices</span></span>
<span data-ttu-id="07f67-1799">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="07f67-1799">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1800">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1800">Az.Resources</span></span>
* <span data-ttu-id="07f67-1801">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1801">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="07f67-1802">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1802">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="07f67-1803">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1803">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="07f67-1804">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1804">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1805">Az.Sql</span></span>
* <span data-ttu-id="07f67-1806">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1806">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="07f67-1807">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1807">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="07f67-1808">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1808">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="07f67-1809">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="07f67-1809">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1810">Az.Accounts</span></span>
* <span data-ttu-id="07f67-1811">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="07f67-1811">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="07f67-1812">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1812">Az.AnalysisServices</span></span>
* <span data-ttu-id="07f67-1813">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="07f67-1813">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-1814">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1814">Az.RecoveryServices</span></span>
* <span data-ttu-id="07f67-1815">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="07f67-1815">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="07f67-1816">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="07f67-1816">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-1817">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1817">Az.Accounts</span></span>
* <span data-ttu-id="07f67-1818">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1818">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="07f67-1819">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1819">Update incorrect online help URLs</span></span>
* <span data-ttu-id="07f67-1820">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1820">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="07f67-1821">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="07f67-1821">Az.Aks</span></span>
* <span data-ttu-id="07f67-1822">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1822">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="07f67-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-1823">Az.Automation</span></span>
* <span data-ttu-id="07f67-1824">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1824">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="07f67-1825">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1825">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="07f67-1826">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="07f67-1826">Az.Cdn</span></span>
* <span data-ttu-id="07f67-1827">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1827">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1828">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1828">Az.Compute</span></span>
* <span data-ttu-id="07f67-1829">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1829">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="07f67-1830">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1830">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="07f67-1831">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1831">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="07f67-1832">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="07f67-1832">Az.ContainerRegistry</span></span>
* <span data-ttu-id="07f67-1833">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1833">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="07f67-1834">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="07f67-1834">Az.DataFactory</span></span>
* <span data-ttu-id="07f67-1835">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1835">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-1836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-1836">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-1837">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1837">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="07f67-1838">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1838">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="07f67-1839">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1839">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="07f67-1840">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="07f67-1840">Az.IotHub</span></span>
* <span data-ttu-id="07f67-1841">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1841">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="07f67-1842">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07f67-1842">Az.KeyVault</span></span>
* <span data-ttu-id="07f67-1843">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1843">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-1844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1844">Az.Network</span></span>
* <span data-ttu-id="07f67-1845">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1845">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1846">Az.Resources</span></span>
* <span data-ttu-id="07f67-1847">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1847">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="07f67-1848">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1848">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="07f67-1849">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="07f67-1849">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="07f67-1850">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1850">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="07f67-1851">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1851">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="07f67-1852">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1852">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="07f67-1853">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1853">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="07f67-1854">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07f67-1854">Az.ServiceFabric</span></span>
* <span data-ttu-id="07f67-1855">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1855">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="07f67-1856">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1856">Fix some error messages.</span></span>
* <span data-ttu-id="07f67-1857">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1857">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="07f67-1858">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1858">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="07f67-1859">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="07f67-1859">Az.SignalR</span></span>
* <span data-ttu-id="07f67-1860">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1860">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1861">Az.Sql</span></span>
* <span data-ttu-id="07f67-1862">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1862">Update incorrect online help URLs</span></span>
* <span data-ttu-id="07f67-1863">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1863">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="07f67-1864">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1864">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="07f67-1865">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1865">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-1866">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-1866">Az.Storage</span></span>
* <span data-ttu-id="07f67-1867">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1867">Update incorrect online help URLs</span></span>
* <span data-ttu-id="07f67-1868">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1868">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="07f67-1869">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="07f67-1869">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="07f67-1870">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="07f67-1870">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="07f67-1871">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="07f67-1871">Az.TrafficManager</span></span>
* <span data-ttu-id="07f67-1872">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1872">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-1873">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-1873">Az.Websites</span></span>
* <span data-ttu-id="07f67-1874">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1874">Update incorrect online help URLs</span></span>
* <span data-ttu-id="07f67-1875">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1875">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="07f67-1876">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1876">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="07f67-1877">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="07f67-1877">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="07f67-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1878">Az.Accounts</span></span>
* <span data-ttu-id="07f67-1879">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1879">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-1880">Az.Compute</span></span>
* <span data-ttu-id="07f67-1881">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1881">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="07f67-1882">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1882">Updated the description of ID in help files</span></span>
* <span data-ttu-id="07f67-1883">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-1884">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-1884">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-1885">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1885">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="07f67-1886">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1886">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="07f67-1887">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="07f67-1887">Az.EventGrid</span></span>
* <span data-ttu-id="07f67-1888">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1888">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="07f67-1889">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1889">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="07f67-1890">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1890">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="07f67-1891">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="07f67-1891">Event Time-To-Live,</span></span>
        - <span data-ttu-id="07f67-1892">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="07f67-1892">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="07f67-1893">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1893">Dead letter endpoint.</span></span>
    - <span data-ttu-id="07f67-1894">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1894">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="07f67-1895">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="07f67-1895">Event Time-To-Live,</span></span>
        - <span data-ttu-id="07f67-1896">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="07f67-1896">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="07f67-1897">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1897">Dead letter endpoint.</span></span>
* <span data-ttu-id="07f67-1898">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1898">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="07f67-1899">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1899">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="07f67-1900">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="07f67-1900">Az.IotHub</span></span>
* <span data-ttu-id="07f67-1901">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1901">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="07f67-1902">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="07f67-1902">Az.LogicApp</span></span>
* <span data-ttu-id="07f67-1903">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="07f67-1903">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-1904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1904">Az.Resources</span></span>
* <span data-ttu-id="07f67-1905">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1905">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="07f67-1906">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1906">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="07f67-1907">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1907">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="07f67-1908">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1908">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="07f67-1909">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1909">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="07f67-1910">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1910">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="07f67-1911">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="07f67-1911">Az.SignalR</span></span>
* <span data-ttu-id="07f67-1912">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1912">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1913">Az.Sql</span></span>
* <span data-ttu-id="07f67-1914">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1914">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="07f67-1915">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-1915">Az.Storage</span></span>
* <span data-ttu-id="07f67-1916">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1916">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="07f67-1917">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="07f67-1917">New-AzStorageContext</span></span>
* <span data-ttu-id="07f67-1918">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1918">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="07f67-1919">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="07f67-1919">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-1920">Az.Websites</span></span>
* <span data-ttu-id="07f67-1921">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1921">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="07f67-1922">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1922">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="07f67-1923">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="07f67-1923">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="07f67-1924">일반</span><span class="sxs-lookup"><span data-stu-id="07f67-1924">General</span></span>

- <span data-ttu-id="07f67-1925">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="07f67-1925">General Availability of Az Module</span></span>
- <span data-ttu-id="07f67-1926">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="07f67-1926">Online help for each module</span></span>
- <span data-ttu-id="07f67-1927">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1927">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="07f67-1928">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1928">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="07f67-1929">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="07f67-1929">Az.Accounts</span></span>
- <span data-ttu-id="07f67-1930">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="07f67-1930">Changed from Az.Profile</span></span>
- <span data-ttu-id="07f67-1931">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1931">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="07f67-1932">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07f67-1932">Az.ApiManagement</span></span>
- <span data-ttu-id="07f67-1933">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-1933">Fixes for #7002</span></span>
- <span data-ttu-id="07f67-1934">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1934">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="07f67-1935">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="07f67-1935">Az.Batch</span></span>
- <span data-ttu-id="07f67-1936">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1936">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="07f67-1937">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1937">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="07f67-1938">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1938">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="07f67-1939">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="07f67-1939">Az.Billing</span></span>
- <span data-ttu-id="07f67-1940">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1940">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="07f67-1941">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1941">Az.CognitivServices</span></span>
- <span data-ttu-id="07f67-1942">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1942">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="07f67-1943">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-1943">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="07f67-1944">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="07f67-1944">Az.ContainerInstance</span></span>
- <span data-ttu-id="07f67-1945">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1945">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="07f67-1946">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="07f67-1946">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="07f67-1947">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1947">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="07f67-1948">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-1948">Az.DataLakeStore</span></span>
- <span data-ttu-id="07f67-1949">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1949">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="07f67-1950">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="07f67-1950">Az.Monitor</span></span>
- <span data-ttu-id="07f67-1951">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1951">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="07f67-1952">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07f67-1952">Az.KeyVault</span></span>
- <span data-ttu-id="07f67-1953">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="07f67-1953">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="07f67-1954">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="07f67-1954">Az.MachineLearning</span></span>
- <span data-ttu-id="07f67-1955">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="07f67-1955">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="07f67-1956">Az.Media</span><span class="sxs-lookup"><span data-stu-id="07f67-1956">Az.Media</span></span>
- <span data-ttu-id="07f67-1957">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1957">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="07f67-1958">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-1958">Az.Network</span></span>
<span data-ttu-id="07f67-1959">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1959">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="07f67-1960">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1960">New cmdlets added:</span></span>
        - <span data-ttu-id="07f67-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07f67-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="07f67-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07f67-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="07f67-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07f67-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="07f67-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07f67-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="07f67-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07f67-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="07f67-1966">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="07f67-1966">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="07f67-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="07f67-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="07f67-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="07f67-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="07f67-1969">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07f67-1969">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="07f67-1970">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07f67-1970">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="07f67-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="07f67-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="07f67-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="07f67-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="07f67-1973">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-1973">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="07f67-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="07f67-1975">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-1975">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="07f67-1976">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="07f67-1976">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="07f67-1977">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="07f67-1977">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="07f67-1978">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="07f67-1978">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="07f67-1979">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="07f67-1979">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="07f67-1980">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="07f67-1980">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="07f67-1981">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1981">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="07f67-1982">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-1982">Az.OperationalInsights</span></span>
- <span data-ttu-id="07f67-1983">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1983">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="07f67-1984">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="07f67-1984">Az.Profile</span></span>
- <span data-ttu-id="07f67-1985">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="07f67-1985">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-1986">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-1986">Az.RecoveryServices</span></span>
- <span data-ttu-id="07f67-1987">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="07f67-1988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-1988">Az.Resources</span></span>
- <span data-ttu-id="07f67-1989">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1989">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="07f67-1990">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07f67-1990">Az.ServiceFabric</span></span>
- <span data-ttu-id="07f67-1991">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-1991">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="07f67-1992">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1992">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="07f67-1993">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="07f67-1993">Az.SIgnalR</span></span>
- <span data-ttu-id="07f67-1994">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="07f67-1994">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="07f67-1995">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-1995">Az.Sql</span></span>
- <span data-ttu-id="07f67-1996">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-1996">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="07f67-1997">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-1997">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="07f67-1998">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-1998">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="07f67-1999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-1999">Az.Storage</span></span>
- <span data-ttu-id="07f67-2000">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-2000">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="07f67-2001">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-2001">Az.Websites</span></span>
- <span data-ttu-id="07f67-2002">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07f67-2002">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="07f67-2003">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="07f67-2003">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="07f67-2004">일반</span><span class="sxs-lookup"><span data-stu-id="07f67-2004">General</span></span>

* <span data-ttu-id="07f67-2005">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="07f67-2005">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="07f67-2006">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-2006">Az.Compute</span></span>

* <span data-ttu-id="07f67-2007">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2007">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="07f67-2008">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-2008">Az.DataLakeStore</span></span>

* <span data-ttu-id="07f67-2009">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2009">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="07f67-2010">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="07f67-2010">Az.FrontDoor</span></span>

* <span data-ttu-id="07f67-2011">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2011">Fixed some broken links</span></span>
    - <span data-ttu-id="07f67-2012">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2012">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="07f67-2013">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2013">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="07f67-2014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07f67-2014">Az.RecoveryServices</span></span>

* <span data-ttu-id="07f67-2015">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2015">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="07f67-2016">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2016">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="07f67-2017">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-2017">Az.Resources</span></span>

* <span data-ttu-id="07f67-2018"> https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2018">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="07f67-2019">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2019">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="07f67-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-2020">Az.Sql</span></span>

* <span data-ttu-id="07f67-2021">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="07f67-2021">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="07f67-2022">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="07f67-2022">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="07f67-2023">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2023">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="07f67-2024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-2024">Az.Storage</span></span>

* <span data-ttu-id="07f67-2025">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2025">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="07f67-2026">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2026">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="07f67-2027">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="07f67-2027">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="07f67-2028">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="07f67-2028">Support Static Website configuration</span></span>
    - <span data-ttu-id="07f67-2029">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="07f67-2029">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="07f67-2030">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="07f67-2030">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="07f67-2031">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-2031">Az.Websites</span></span>

* <span data-ttu-id="07f67-2032">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="07f67-2032">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="07f67-2033">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2033">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="07f67-2034">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2034">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="07f67-2035">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="07f67-2035">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="07f67-2036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07f67-2036">Az.ApiManagement</span></span>
* <span data-ttu-id="07f67-2037">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-2037">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="07f67-2038">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="07f67-2038">Az.Automation</span></span>
* <span data-ttu-id="07f67-2039">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="07f67-2039">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="07f67-2040">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2040">Added Update Management cmdlets</span></span>
* <span data-ttu-id="07f67-2041">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2041">Added Source Control cmdlets</span></span>
* <span data-ttu-id="07f67-2042">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2042">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="07f67-2043">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2043">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="07f67-2044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-2044">Az.Compute</span></span>
* <span data-ttu-id="07f67-2045">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2045">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="07f67-2046">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-2046">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="07f67-2047">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="07f67-2047">Az.ContainerInstance</span></span>
* <span data-ttu-id="07f67-2048">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-2048">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="07f67-2049">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="07f67-2049">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="07f67-2050">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-2050">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="07f67-2051">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-2051">Az.Network</span></span>
* <span data-ttu-id="07f67-2052">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2052">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="07f67-2053">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2053">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="07f67-2054">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2054">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="07f67-2055">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="07f67-2055">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="07f67-2056">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="07f67-2056">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="07f67-2057">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2057">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="07f67-2058">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2058">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="07f67-2059">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="07f67-2059">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="07f67-2060">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="07f67-2060">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="07f67-2061">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-2061">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="07f67-2062">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="07f67-2062">Az.Relay</span></span>
* <span data-ttu-id="07f67-2063">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2063">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="07f67-2064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-2064">Az.Resources</span></span>
* <span data-ttu-id="07f67-2065">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="07f67-2065">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="07f67-2066">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2066">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="07f67-2067">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="07f67-2067">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="07f67-2068">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07f67-2068">Az.ServiceFabric</span></span>
* <span data-ttu-id="07f67-2069">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2069">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="07f67-2070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-2070">Az.Sql</span></span>
* <span data-ttu-id="07f67-2071">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2071">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="07f67-2072">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="07f67-2072">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="07f67-2073">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="07f67-2073">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="07f67-2074">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="07f67-2074">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="07f67-2075">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="07f67-2075">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="07f67-2076">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="07f67-2076">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="07f67-2077">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="07f67-2077">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="07f67-2078">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="07f67-2078">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="07f67-2079">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="07f67-2079">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="07f67-2080">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2080">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="07f67-2081">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2081">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="07f67-2082">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2082">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="07f67-2083">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="07f67-2083">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="07f67-2084">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="07f67-2084">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="07f67-2085">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="07f67-2085">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="07f67-2086">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="07f67-2086">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="07f67-2087">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="07f67-2087">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="07f67-2088">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="07f67-2088">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="07f67-2089">일반</span><span class="sxs-lookup"><span data-stu-id="07f67-2089">General</span></span>
* <span data-ttu-id="07f67-2090">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2090">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="07f67-2091">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="07f67-2091">Az.Profile</span></span>
* <span data-ttu-id="07f67-2092">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2092">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="07f67-2093">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="07f67-2093">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="07f67-2094">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="07f67-2094">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="07f67-2095">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2095">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="07f67-2096">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2096">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="07f67-2097">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2097">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="07f67-2098">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2098">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="07f67-2099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="07f67-2099">Az.CognitiveServices</span></span>
* <span data-ttu-id="07f67-2100">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2100">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-2101">Az.Compute</span></span>
* <span data-ttu-id="07f67-2102">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="07f67-2102">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="07f67-2103">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="07f67-2103">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="07f67-2104">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2104">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-2106">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2106">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="07f67-2107">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2107">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="07f67-2108">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="07f67-2108">Az.Insights</span></span>
* <span data-ttu-id="07f67-2109">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="07f67-2109">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="07f67-2110">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="07f67-2110">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="07f67-2111">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="07f67-2111">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="07f67-2112">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="07f67-2112">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-2113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-2113">Az.Network</span></span>
* <span data-ttu-id="07f67-2114">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2114">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="07f67-2115">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="07f67-2115">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="07f67-2116">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="07f67-2116">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="07f67-2117">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="07f67-2117">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="07f67-2118">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="07f67-2118">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="07f67-2119">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="07f67-2119">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="07f67-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="07f67-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="07f67-2121">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="07f67-2121">Az.PolicyInsights</span></span>
* <span data-ttu-id="07f67-2122">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="07f67-2122">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-2123">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-2123">Az.Resources</span></span>
* <span data-ttu-id="07f67-2124"> https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2124">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="07f67-2125">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="07f67-2125">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="07f67-2126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07f67-2126">Az.ServiceBus</span></span>
* <span data-ttu-id="07f67-2127">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="07f67-2127">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="07f67-2128">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07f67-2128">Az.ServiceFabric</span></span>
* <span data-ttu-id="07f67-2129">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="07f67-2129">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="07f67-2130">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2130">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="07f67-2131">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="07f67-2131">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="07f67-2132">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="07f67-2132">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="07f67-2133">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="07f67-2133">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="07f67-2134">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="07f67-2134">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="07f67-2135">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="07f67-2135">Az.Profile</span></span>
* <span data-ttu-id="07f67-2136">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2136">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="07f67-2137">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2137">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-2138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-2138">Az.Compute</span></span>
* <span data-ttu-id="07f67-2139">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2139">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="07f67-2140">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2140">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="07f67-2141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07f67-2141">Az.DataLakeStore</span></span>
* <span data-ttu-id="07f67-2142">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2142">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="07f67-2143">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2143">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="07f67-2144">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2144">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="07f67-2145">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2145">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="07f67-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-2147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-2147">Az.Network</span></span>
* <span data-ttu-id="07f67-2148">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2148">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="07f67-2149">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2149">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-2150">Az.Resources</span></span>
* <span data-ttu-id="07f67-2151">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2151">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="07f67-2152">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2152">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="07f67-2153">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="07f67-2153">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="07f67-2154">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="07f67-2154">Azure.Storage</span></span>
* <span data-ttu-id="07f67-2155">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2155">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="07f67-2156">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="07f67-2156">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="07f67-2157">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="07f67-2157">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="07f67-2158">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2158">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="07f67-2159">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="07f67-2159">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="07f67-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="07f67-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="07f67-2161">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2161">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="07f67-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="07f67-2162">Az.Compute</span></span>
* <span data-ttu-id="07f67-2163">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2163">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="07f67-2164">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="07f67-2164">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="07f67-2165">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2165">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="07f67-2166">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="07f67-2166">Az.DataFactoryV2</span></span>
* <span data-ttu-id="07f67-2167">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="07f67-2167">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="07f67-2168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="07f67-2168">Az.Network</span></span>
* <span data-ttu-id="07f67-2169">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2169">Added NetworkProfile functionality.</span></span> <span data-ttu-id="07f67-2170">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2170">new cmdlets added</span></span>
    - <span data-ttu-id="07f67-2171">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="07f67-2171">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="07f67-2172">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="07f67-2172">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="07f67-2173">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="07f67-2173">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="07f67-2174">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="07f67-2174">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="07f67-2175">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-2175">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="07f67-2176">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="07f67-2176">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="07f67-2177">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2177">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="07f67-2178">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2178">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="07f67-2179">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2179">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="07f67-2180">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="07f67-2180">Az.RedisCache</span></span>
* <span data-ttu-id="07f67-2181">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="07f67-2181">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="07f67-2182">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2182">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="07f67-2183">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="07f67-2183">Az.Resources</span></span>
* <span data-ttu-id="07f67-2184">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="07f67-2184">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="07f67-2185">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="07f67-2185">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="07f67-2186">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="07f67-2186">Az.Sql</span></span>
* <span data-ttu-id="07f67-2187">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="07f67-2187">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="07f67-2188">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="07f67-2188">Az.Websites</span></span>
* <span data-ttu-id="07f67-2189">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2189">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="07f67-2190">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="07f67-2190">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="07f67-2191">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="07f67-2191">0.2.0 - September 2018</span></span>
 <span data-ttu-id="07f67-2192">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="07f67-2192">Initial Release</span></span>