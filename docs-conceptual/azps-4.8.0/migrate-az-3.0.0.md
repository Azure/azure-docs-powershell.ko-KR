---
title: Az 3.0.0 마이그레이션 가이드
description: 이 마이그레이션 가이드에는 Az 버전 3.0 릴리스의 Azure PowerShell에 대한 호환성이 손상되는 변경 목록이 나와 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 641804fc0931d29f082ef7057f610beb75d7550a
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410488"
---
# <a name="migration-guide-for-az-300"></a><span data-ttu-id="6e5e5-103">Az 3.0.0 마이그레이션 가이드</span><span class="sxs-lookup"><span data-stu-id="6e5e5-103">Migration Guide for Az 3.0.0</span></span>

<span data-ttu-id="6e5e5-104">이 문서에서는 Az 2.0.0 및 3.0.0 버전 간의 변경 내용에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-104">This document describes the changes between the 2.0.0 and 3.0.0 versions of Az</span></span>

<!-- TOC -->

- [<span data-ttu-id="6e5e5-105">Az 3.0.0 마이그레이션 가이드</span><span class="sxs-lookup"><span data-stu-id="6e5e5-105">Migration Guide for Az 3.0.0</span></span>](#migration-guide-for-az-300)
  - [<span data-ttu-id="6e5e5-106">Batch</span><span class="sxs-lookup"><span data-stu-id="6e5e5-106">Batch</span></span>](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [<span data-ttu-id="6e5e5-107">`Az.Resources`의 이전 버전과 호환되지 않음</span><span class="sxs-lookup"><span data-stu-id="6e5e5-107">Incompatibility with previous versions of `Az.Resources`</span></span>](#previous-version-incompatibility-with-azresources-module)
  - [<span data-ttu-id="6e5e5-108">컴퓨팅</span><span class="sxs-lookup"><span data-stu-id="6e5e5-108">Compute</span></span>](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [<span data-ttu-id="6e5e5-109">HDInsight</span><span class="sxs-lookup"><span data-stu-id="6e5e5-109">HDInsight</span></span>](#hdinsight)
    - [`Get-AzHDInsightJobOutput`](#get-azhdinsightjoboutput)
    - [`Add-AzHDInsightConfigValues`](#add-azhdinsightconfigvalues)
    - [`Disable-AzHDInsightMonitoring`](#disable-azhdinsightmonitoring)
    - [`Enable-AzHDInsightMonitoring`](#enable-azhdinsightmonitoring)
    - [`Get-AzHDInsightMonitoring`](#get-azhdinsightmonitoring)
    - [`Get-AzHDInsightProperty`](#get-azhdinsightproperty)
    - [`Grant-AzHDInsightRdpServicesAccess`](#grant-azhdinsightrdpservicesaccess)
    - [`Remove-AzHDInsightCluster`](#remove-azhdinsightcluster)
    - [`Revoke-AzHDInsightRdpServicesAccess`](#revoke-azhdinsightrdpservicesaccess)
    - [`Set-AzHDInsightGatewayCredential`](#set-azhdinsightgatewaycredential)
  - [<span data-ttu-id="6e5e5-110">IotHub</span><span class="sxs-lookup"><span data-stu-id="6e5e5-110">IotHub</span></span>](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [<span data-ttu-id="6e5e5-111">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6e5e5-111">RecoveryServices</span></span>](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [<span data-ttu-id="6e5e5-112">리소스</span><span class="sxs-lookup"><span data-stu-id="6e5e5-112">Resources</span></span>](#resources)
    - [<span data-ttu-id="6e5e5-113">`Az.Batch`의 이전 버전과 호환되지 않음</span><span class="sxs-lookup"><span data-stu-id="6e5e5-113">Incompatibility with previous versions of `Az.Batch`</span></span>](#previous-version-incompatibility-with-azbatch-module)
  - [<span data-ttu-id="6e5e5-114">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6e5e5-114">ServiceFabric</span></span>](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [<span data-ttu-id="6e5e5-115">Sql</span><span class="sxs-lookup"><span data-stu-id="6e5e5-115">Sql</span></span>](#sql)
    - [`Get-AzSqlDatabaseSecureConnectionPolicy`](#get-azsqldatabasesecureconnectionpolicy)
    - [`Get-AzSqlDatabaseIndexRecommendations`](#get-azsqldatabaseindexrecommendations)
    - [`Get-AzSqlDatabaseRestorePoints`](#get-azsqldatabaserestorepoints)
    - [`Get-AzSqlDatabaseAuditing`](#get-azsqldatabaseauditing)
    - [`Set-AzSqlDatabaseAuditing`](#set-azsqldatabaseauditing)
    - [`Get-AzSqlServerAuditing`](#get-azsqlserverauditing)
    - [`Set-AzSqlServerAuditing`](#set-azsqlserverauditing)
    - [`Get-AzSqlServerAdvancedThreatProtectionSettings`](#get-azsqlserveradvancedthreatprotectionsettings)
    - [`Clear-AzSqlServerAdvancedThreatProtectionSettings`](#clear-azsqlserveradvancedthreatprotectionsettings)
    - [`Update-AzSqlServerAdvancedThreatProtectionSettings`](#update-azsqlserveradvancedthreatprotectionsettings)
    - [`Get-AzSqlDatabaseAdvancedThreatProtectionSettings`](#get-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseAdvancedThreatProtectionSettings`](#update-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`](#clear-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseVulnerabilityAssessmentSettings`](#update-azsqldatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlDatabaseVulnerabilityAssessmentSettings`](#get-azsqldatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`](#clear-azsqldatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#update-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#get-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#clear-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceVulnerabilityAssessmentSettings`](#update-azsqlinstancevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceVulnerabilityAssessmentSettings`](#get-azsqlinstancevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceVulnerabilityAssessmentSettings`](#clear-azsqlinstancevulnerabilityassessmentsettings)
    - [`Update-AzSqlServerVulnerabilityAssessmentSettings`](#update-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerVulnerabilityAssessmentSettings`](#get-azsqlservervulnerabilityassessmentsettings)
    - [`Clear-AzSqlServerVulnerabilityAssessmentSettings`](#clear-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerAdvancedThreatProtectionPolicy`](#get-azsqlserveradvancedthreatprotectionpolicy)
    - [`Get-AzSqlServerThreatDetectionPolicy`](#get-azsqlserverthreatdetectionpolicy)
    - [`Remove-AzSqlServerThreatDetectionPolicy`](#remove-azsqlserverthreatdetectionpolicy)
    - [`Set-AzSqlServerThreatDetectionPolicy`](#set-azsqlserverthreatdetectionpolicy)
    - [`Get-AzSqlDatabaseThreatDetectionPolicy`](#get-azsqldatabasethreatdetectionpolicy)
    - [`Set-AzSqlDatabaseThreatDetectionPolicy`](#set-azsqldatabasethreatdetectionpolicy)
    - [`Remove-AzSqlDatabaseThreatDetectionPolicy`](#remove-azsqldatabasethreatdetectionpolicy)

<!-- /TOC -->


## <a name="batch"></a><span data-ttu-id="6e5e5-116">Batch</span><span class="sxs-lookup"><span data-stu-id="6e5e5-116">Batch</span></span>

### `Get-AzBatchNodeAgentSku`
- <span data-ttu-id="6e5e5-117">`Get-AzBatchNodeAgentSku`가 제거되고 `Get-AzBatchSupportedImage`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-117">Removed `Get-AzBatchNodeAgentSku` and replaced it with  `Get-AzBatchSupportedImage`.</span></span>
- <span data-ttu-id="6e5e5-118">`Get-AzBatchSupportedImage`는 `Get-AzBatchNodeAgentSku`와 동일한 데이터를 더 친숙한 형식으로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-118">`Get-AzBatchSupportedImage` returns the same data as `Get-AzBatchNodeAgentSku` but in a more friendly format.</span></span>
- <span data-ttu-id="6e5e5-119">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-119">New non-verified images are also now returned.</span></span> <span data-ttu-id="6e5e5-120">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-120">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-121">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-121">Before</span></span>
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a><span data-ttu-id="6e5e5-122">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-122">After</span></span>
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a><span data-ttu-id="6e5e5-123">Az.Resources 모듈의 이전 버전과 호환되지 않음</span><span class="sxs-lookup"><span data-stu-id="6e5e5-123">Previous Version Incompatibility with Az.Resources Module</span></span>
<span data-ttu-id="6e5e5-124">'Az.Batch' 모듈의 버전 2.0.1은 'Az.Resources' 모듈의 이전 버전(버전 1.7.0 이하)과 호환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-124">Version 2.0.1 of the ‘Az.Batch’ module is incompatible with earlier versions (version 1.7.0 or earlier) of the ‘Az.Resources’ module.</span></span>  <span data-ttu-id="6e5e5-125">이로 인해 'Az.Batch' 모듈의 버전 2.0.1을 가져올 때 'Az.Resources' 모듈의 버전 1.7.0을 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-125">This will result in being unable to import  version 1.7.0 of the ‘Az.Resources’ module when version 2.0.1 of the ‘Az.Batch’ module is imported.</span></span>  <span data-ttu-id="6e5e5-126">이 문제를 해결하려면 'Az.Resources' 모듈을 버전 1.7.1 이상으로 업데이트하거나 'Az' 모듈의 최신 버전을 설치하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-126">To fix this issue, simply update the ‘Az.Resources’ module to version 1.7.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="compute"></a><span data-ttu-id="6e5e5-127">컴퓨팅</span><span class="sxs-lookup"><span data-stu-id="6e5e5-127">Compute</span></span>

### `New-AzDiskConfig`
<span data-ttu-id="6e5e5-128">CreateOption이 Upload인 경우 `New-AzDiskConfig`에 대해 `DiskSizeGB` 대신 `UploadSizeInBytes` 매개 변수가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-128">`UploadSizeInBytes` parameter is used instead of `DiskSizeGB` for `New-AzDiskConfig` when CreateOption is Upload</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-129">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-129">Before</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a><span data-ttu-id="6e5e5-130">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-130">After</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a><span data-ttu-id="6e5e5-131">HDInsight</span><span class="sxs-lookup"><span data-stu-id="6e5e5-131">HDInsight</span></span>

### `Get-AzHDInsightJobOutput`
- <span data-ttu-id="6e5e5-132">스토리지 키에 대한 세분화된 역할 기반 액세스를 지원하도록 `Get-AzHDInsightJobOutput` cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-132">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
- <span data-ttu-id="6e5e5-133">HDInsight 클러스터 운영자, 기여자 또는 소유자 역할이 있는 사용자는 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-133">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
- <span data-ttu-id="6e5e5-134">읽기 권한자 역할만 있는 사용자는 `DefaultStorageAccountKey` 매개 변수를 명시적으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-134">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-135">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-135">Before</span></span>
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a><span data-ttu-id="6e5e5-136">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-136">After</span></span>
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
<span data-ttu-id="6e5e5-137">`Add-AzHDInsightConfigValue` cmdlet에서 `Add-AzHDInsightConfigValues`에 대한 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-137">Cmdlet `Add-AzHDInsightConfigValue` removed alias to `Add-AzHDInsightConfigValues`.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-138">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-138">Before</span></span>
<span data-ttu-id="6e5e5-139">사용되지 않는 별칭을 사용했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-139">Using deprecated alias</span></span>
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a><span data-ttu-id="6e5e5-140">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-140">After</span></span>
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
<span data-ttu-id="6e5e5-141">새 `Disable-AzHDInsightMonitoring` cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-141">Added a new `Disable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="6e5e5-142">이 cmdlet을 사용하여 HDInsight 클러스터에서 모니터링을 사용하지 않도록 설정합니다(`Disable-AzHDInsightOperationsManagementSuite` 및 `Disable-AzHDInsightOMS` 대체).</span><span class="sxs-lookup"><span data-stu-id="6e5e5-142">Use this cmdlet to disable monitoring in a HDInsight cluster (replaces `Disable-AzHDInsightOperationsManagementSuite` and `Disable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-143">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-143">Before</span></span>
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="6e5e5-144">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-144">After</span></span>
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
<span data-ttu-id="6e5e5-145">새 `Enable-AzHDInsightMonitoring` cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-145">Added a new `Enable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="6e5e5-146">이 cmdlet을 사용하여 HDInsight 클러스터에서 모니터링을 사용하도록 설정합니다(`Enable-AzHDInsightOperationsManagementSuite` 및 `Enable-AzHDInsightOMS` 대체).</span><span class="sxs-lookup"><span data-stu-id="6e5e5-146">Use this cmdlet to enable monitoring in a HDInsight cluster (replaces `Enable-AzHDInsightOperationsManagementSuite` and `Enable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-147">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-147">Before</span></span>
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a><span data-ttu-id="6e5e5-148">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-148">After</span></span>
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
<span data-ttu-id="6e5e5-149">새 `Get-AzHDInsightMonitoring` cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-149">Added a new `Get-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="6e5e5-150">이 cmdlet을 사용하여 Azure HDInsight 클러스터에서 설치 모니터링 상태를 확인합니다(`Get-AzHDInsightOperationsManagementSuite` 및 `Get-AzHDInsightOMS` 대체).</span><span class="sxs-lookup"><span data-stu-id="6e5e5-150">Use this cmdlet to get the status of monitoring installation in an Azure HDInsight cluster (replaces `Get-AzHDInsightOperationsManagementSuite` and `Get-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-151">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-151">Before</span></span>
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="6e5e5-152">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-152">After</span></span>
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
<span data-ttu-id="6e5e5-153">`Get-HDInsightProperty` cmdlet에서 `Get-AzHDInsightProperties`에 대한 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-153">Cmdlet `Get-HDInsightProperty` removed alias to `Get-AzHDInsightProperties`.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-154">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-154">Before</span></span>
<span data-ttu-id="6e5e5-155">사용되지 않는 별칭을 사용했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-155">Using deprecated alias</span></span>
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-156">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-156">After</span></span>
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
<span data-ttu-id="6e5e5-157">`Grant-AzHDInsightRdpServicesAccess` 및 `Revoke-AzHDInsightRdpServicesAccess` cmdlet을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-157">Removed the `Grant-AzHDInsightRdpServicesAccess` and `Revoke-AzHDInsightRdpServicesAccess` cmdlets.</span></span> <span data-ttu-id="6e5e5-158">Windows OS 유형을 사용하는 클러스터를 지원하지 않으므로 더 이상 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-158">These are no longer necessary because clusters using Windows OS type are not supported.</span></span> <span data-ttu-id="6e5e5-159">대신 Linux OS 유형을 사용하여 클러스터를 만드세요.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-159">Please create a cluster using Linux OS type instead.</span></span>

### `Remove-AzHDInsightCluster`
<span data-ttu-id="6e5e5-160">`Remove-AzHDInsightCluster`의 출력 형식이 `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse`에서 `bool`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-160">The output type of `Remove-AzHDInsightCluster` changed from `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` to `bool`.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-161">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-161">Before</span></span>
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-162">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-162">After</span></span>
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
<span data-ttu-id="6e5e5-163">이 cmdlet은 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-163">The cmdlet is deprecated.</span></span> <span data-ttu-id="6e5e5-164">이를 대체하는 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-164">There is no replacement for it.</span></span>

### `Set-AzHDInsightGatewayCredential`
<span data-ttu-id="6e5e5-165">`Set-AzHDInsightGatewayCredential`의 출력 형식이 `HttpConnectivitySettings`에서 `AzureHDInsightGatewaySettings`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-165">The output type of `Set-AzHDInsightGatewayCredential` changed from `HttpConnectivitySettings` to `AzureHDInsightGatewaySettings`.</span></span>



## <a name="iothub"></a><span data-ttu-id="6e5e5-166">IotHub</span><span class="sxs-lookup"><span data-stu-id="6e5e5-166">IotHub</span></span>

### `New-AzIotHubImportDevices`
<span data-ttu-id="6e5e5-167">이 별칭은 제거되었습니다. 대신 `New-AzIotHubImportDevice`를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-167">This alias is removed, please use `New-AzIotHubImportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-168">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-168">Before</span></span>
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-169">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-169">After</span></span>
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
<span data-ttu-id="6e5e5-170">이 별칭은 제거되었습니다. 대신 `New-AzIotHubExportDevice`를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-170">This alias is removed, please use `New-AzIotHubExportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-171">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-171">Before</span></span>
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a><span data-ttu-id="6e5e5-172">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-172">After</span></span>
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="6e5e5-173">IotHub에는 시스템 및 디바이스 메시지를 처리할 수 있는 하나의 기본 제공 엔드포인트("events")만 제공되므로 `EventHubEndPointName` 매개 변수는 대체 매개 변수 없이 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-173">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-174">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-174">Before</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-175">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-175">After</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="6e5e5-176">IotHub에는 시스템 및 디바이스 메시지를 처리할 수 있는 하나의 기본 제공 엔드포인트("events")만 제공되므로 `EventHubEndPointName` 매개 변수는 대체 매개 변수 없이 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-176">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-177">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-177">Before</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-178">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-178">After</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="6e5e5-179">IotHub에는 시스템 및 디바이스 메시지를 처리할 수 있는 하나의 기본 제공 엔드포인트("events")만 제공되므로 `EventHubEndPointName` 매개 변수는 대체 매개 변수 없이 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-179">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-180">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-180">Before</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-181">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-181">After</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
<span data-ttu-id="6e5e5-182">IotHub에서 기본 제공 엔드포인트("operationsMonitoringEvents")를 더 이상 사용하지 않으므로 `OperationsMonitoringProperties` 매개 변수는 대체 매개 변수 없이 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-182">Parameter `OperationsMonitoringProperties` is deprecated without being replaced as IotHub is no longer using built-in endpoint("operationsMonitoringEvents").</span></span>



## <a name="recoveryservices"></a><span data-ttu-id="6e5e5-183">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6e5e5-183">RecoveryServices</span></span>

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="6e5e5-184">출력에서 `ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` 및 `ASRRecoveryPlanGroup.EndGroupActions`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `Get-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="6e5e5-185">출력에서 `ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` 및 `ASRRecoveryPlanGroup.EndGroupActions`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
<span data-ttu-id="6e5e5-186">IncludeDiskId 매개 변수는 Azure Site Recovery에서 관리 디스크에 직접 쓸 수 있도록 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-186">Parameter IncludeDiskId is changed to support directly writing to a managed disk in Azure Site Recovery.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-187">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-187">Before</span></span>
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a><span data-ttu-id="6e5e5-188">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-188">After</span></span>
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a><span data-ttu-id="6e5e5-189">리소스</span><span class="sxs-lookup"><span data-stu-id="6e5e5-189">Resources</span></span>

### <a name="previous-version-incompatibility-with-azbatch-module"></a><span data-ttu-id="6e5e5-190">Az.Batch 모듈의 이전 버전과 호환되지 않음</span><span class="sxs-lookup"><span data-stu-id="6e5e5-190">Previous Version Incompatibility with Az.Batch Module</span></span>
<span data-ttu-id="6e5e5-191">'Az.Resources' 모듈의 버전 1.7.1은 'Az.Batch' 모듈의 이전 버전(버전 1.1.2 이하)과 호환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-191">Version 1.7.1 of the ‘Az.Resources’ module is incompatible with earlier versions (version 1.1.2 or earlier) of the ‘Az.Batch’ module.</span></span>  <span data-ttu-id="6e5e5-192">이로 인해 'Az.Resources' 모듈의 버전 1.7.1을 가져올 때 'Az.Batch' 모듈의 버전 1.1.2를 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-192">This will result in being unable to import  version 1.1.2 of the ‘Az.Batch’ module when version 1.7.1 of the ‘Az.Resources’ module is imported.</span></span>  <span data-ttu-id="6e5e5-193">이 문제를 해결하려면 'Az.Batch' 모듈을 버전 2.0.1 이상으로 업데이트하거나 'Az' 모듈의 최신 버전을 설치하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-193">To fix this issue, update the ‘Az.Batch’ module to version 2.0.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="servicefabric"></a><span data-ttu-id="6e5e5-194">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6e5e5-194">ServiceFabric</span></span>

### `Add-ServiceFabricApplicationCertificate`
<span data-ttu-id="6e5e5-195">`Add-AzVmssSecret`에서 이 시나리오를 처리하므로 `Add-ServiceFabricApplicationCertificate`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-195">Removed `Add-ServiceFabricApplicationCertificate` as this scenario is covered by `Add-AzVmssSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-196">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-196">Before</span></span>
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-197">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-197">After</span></span>
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a><span data-ttu-id="6e5e5-198">Sql</span><span class="sxs-lookup"><span data-stu-id="6e5e5-198">Sql</span></span>

### `Get-AzSqlDatabaseSecureConnectionPolicy`
<span data-ttu-id="6e5e5-199">보안 연결이 더 이상 사용되지 않으므로 이 명령이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-199">Note that secure connection is deprecated and so command is removed.</span></span> <span data-ttu-id="6e5e5-200">Azure Portal의 SQL 데이터베이스 블레이드를 사용하여 연결 문자열을 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-200">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

### `Get-AzSqlDatabaseIndexRecommendations`
<span data-ttu-id="6e5e5-201">`Get-AzSqlDatabaseIndexRecommendations` 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-201">`Get-AzSqlDatabaseIndexRecommendations` alias is removed.</span></span> <span data-ttu-id="6e5e5-202">대신 `Get-AzSqlDatabaseIndexRecommendation`를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-202">Use `Get-AzSqlDatabaseIndexRecommendation` instead.</span></span>

### `Get-AzSqlDatabaseRestorePoints`
<span data-ttu-id="6e5e5-203">`Get-AzSqlDatabaseRestorePoints` 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-203">`Get-AzSqlDatabaseRestorePoints` alias is removed.</span></span> <span data-ttu-id="6e5e5-204">대신 `Get-AzSqlDatabaseRestorePoint`를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-204">Use `Get-AzSqlDatabaseRestorePoint` instead.</span></span>

### `Get-AzSqlDatabaseAuditing`
- <span data-ttu-id="6e5e5-205">이 cmdlet은 `Get-AzSqlDatabaseAudit` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-205">The cmdlet `Get-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="6e5e5-206">출력 형식이 기존 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 형식에서 새 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel' 형식으로 변경되었으며, `AuditState`, `StorageAccountName`</span><span class="sxs-lookup"><span data-stu-id="6e5e5-206">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removing properties `AuditState` and `StorageAccountName`.</span></span> <span data-ttu-id="6e5e5-207">및 `StorageAccountSubscriptionId` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-207">and `StorageAccountSubscriptionId`.</span></span>  <span data-ttu-id="6e5e5-208">스크립트는 새 `StorageAccountResourceId` 속성에서 스토리지 계정 정보를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-208">Scripts can retrieve storage account information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-209">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-209">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="6e5e5-210">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-210">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlDatabaseAuditing`
- <span data-ttu-id="6e5e5-211">이 cmdlet은 `Set-AzSqlDatabaseAudit` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-211">The cmdlet `Set-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="6e5e5-212">출력 형식이 기존 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 형식에서 새 'bool' 형식으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-212">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-213">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-213">Before</span></span>
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-214">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-214">After</span></span>
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- <span data-ttu-id="6e5e5-215">이 cmdlet은 `Get-AzSqlServerAudit` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-215">The cmdlet `Get-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="6e5e5-216">출력 형식이 기존 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 형식에서 새 'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel' 형식으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-216">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span></span>  <span data-ttu-id="6e5e5-217">`AuditState`, `StorageAccountName` 및 `StorageAccountSubscriptionId` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-217">Properties `AuditState`, `StorageAccountName`, and `StorageAccountSubscriptionId` are removed.</span></span>  <span data-ttu-id="6e5e5-218">`StorageAccountName` 및 `StorageAccountSubscriptionId` 속성을 사용하는 스크립트는 새 `StorageAccountResourceId` 속성에서 이 정보를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-218">Scripts that use `StorageAccountName` and `StorageAccountSubscriptionId` proeprties can retrieve this information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-219">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-219">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="6e5e5-220">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-220">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlServerAuditing`
- <span data-ttu-id="6e5e5-221">이 cmdlet은 `Set-AzSqlServerAudit` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-221">The cmdlet `Set-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="6e5e5-222">출력 형식이 기존 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 형식에서 새 'bool' 형식으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-222">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-223">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-223">Before</span></span>
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-224">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-224">After</span></span>
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="6e5e5-225">`Get-AzSqlServerAdvancedThreatProtectionSettings` cmdlet은 `Get-AzSqlServerAdvancedThreatProtectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-226">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-226">Before</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-227">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-227">After</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="6e5e5-228">`Clear-AzSqlServerAdvancedThreatProtectionSettings` cmdlet은 `Clear-AzSqlServerAdvancedThreatProtectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-229">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-229">Before</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-230">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-230">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="6e5e5-231">`Update-AzSqlServerAdvancedThreatProtectionSettings` cmdlet은 `Update-AzSqlServerAdvancedThreatProtectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Update-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-232">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-232">Before</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-233">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-233">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="6e5e5-234">`Get-AzSqlDatabaseAdvancedThreatProtectionSettings` cmdlet은 `Get-AzSqlDatabaseAdvancedThreatProtectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-235">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-235">Before</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-236">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-236">After</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="6e5e5-237">`Update-AzSqlDatabaseAdvancedThreatProtectionSettings` cmdlet은 `Update-AzSqlDatabaseAdvancedThreatProtectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-238">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-238">Before</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-239">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-239">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="6e5e5-240">`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` cmdlet은 `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-241">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-241">Before</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-242">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-242">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-243">`Update-AzSqlDatabaseVulnerabilityAssessmentSettings` cmdlet은 `Update-AzSqlDatabaseVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-244">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-244">Before</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="6e5e5-245">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-245">After</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```


### `Get-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-246">`Get-AzSqlDatabaseVulnerabilityAssessmentSettings` cmdlet은 `Get-AzSqlDatabaseVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-247">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-247">Before</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-248">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-248">After</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-249">`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` cmdlet은 `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-250">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-250">Before</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-251">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-251">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-252">`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` cmdlet은 `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-253">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-253">Before</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="6e5e5-254">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-254">After</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-255">`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` cmdlet은 `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-256">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-256">Before</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-257">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-257">After</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-258">`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` cmdlet은 `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-259">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-259">Before</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-260">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-260">After</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-261">`Update-AzSqlInstanceVulnerabilityAssessmentSettings` cmdlet은 `Update-AzSqlInstanceVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-262">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-262">Before</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="6e5e5-263">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-263">After</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-264">`Get-AzSqlInstanceVulnerabilityAssessmentSettings` cmdlet은 `Get-AzSqlInstanceVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-265">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-265">Before</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-266">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-266">After</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-267">`Clear-AzSqlInstanceVulnerabilityAssessmentSettings` cmdlet은 `Clear-AzSqlInstanceVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-268">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-268">Before</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-269">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-269">After</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-270">`Update-AzSqlServerVulnerabilityAssessmentSettings` cmdlet은 `Update-AzSqlServerVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-271">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-271">Before</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="6e5e5-272">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-272">After</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-273">`Get-AzSqlServerVulnerabilityAssessmentSettings` cmdlet은 `Get-AzSqlServerVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-274">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-274">Before</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-275">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-275">After</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="6e5e5-276">`Clear-AzSqlServerVulnerabilityAssessmentSettings` cmdlet은 `Clear-AzSqlServerVulnerabilityAssessmentSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-277">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-277">Before</span></span>
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-278">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-278">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
<span data-ttu-id="6e5e5-279">`Get-AzSqlServerAdvancedThreatProtectionPolicy` cmdlet은 삭제되었고, 이를 대체하는 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` is deleted and no cmdlet is repleaced it</span></span>

### `Get-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="6e5e5-280">`Get-AzSqlServerThreatDetectionPolicy` cmdlet은 `Get-AzSqlServerThreatDetectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` is repleaced by `Get-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-281">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-281">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="6e5e5-282">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-282">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Remove-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="6e5e5-283">`Remove-AzSqlServerThreatDetectionPolicy` cmdlet은 `Clear-AzSqlServerThreatDetectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` is repleaced by `Clear-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-284">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-284">Before</span></span>
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-285">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-285">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="6e5e5-286">`Set-AzSqlServerThreatDetectionPolicy` cmdlet은 `Update-AzSqlServerThreatDetectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` is repleaced by `Update-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-287">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-287">Before</span></span>
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-288">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-288">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="6e5e5-289">`Get-AzSqlDatabaseThreatDetectionPolicy` cmdlet은 `Get-AzSqlDatabaseThreatDetectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Get-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-290">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-290">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName   "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="6e5e5-291">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-291">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"   -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Set-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="6e5e5-292">`Set-AzSqlDatabaseThreatDetectionPolicy` cmdlet은 `Update-AzSqlDatabaseThreatDetectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Update-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-293">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-293">Before</span></span>
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-294">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-294">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="6e5e5-295">`Remove-AzSqlDatabaseThreatDetectionPolicy` cmdlet은 `Clear-AzSqlDatabaseThreatDetectionSetting` cmdlet으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5e5-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Clear-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="6e5e5-296">이전</span><span class="sxs-lookup"><span data-stu-id="6e5e5-296">Before</span></span>
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="6e5e5-297">After</span><span class="sxs-lookup"><span data-stu-id="6e5e5-297">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```
