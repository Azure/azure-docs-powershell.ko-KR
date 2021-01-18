---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492960"
---
# <span data-ttu-id="554ee-101">Az.HDInsight 모듈</span><span class="sxs-lookup"><span data-stu-id="554ee-101">Az.HDInsight Module</span></span>
## <span data-ttu-id="554ee-102">설명</span><span class="sxs-lookup"><span data-stu-id="554ee-102">Description</span></span>
<span data-ttu-id="554ee-103">이 섹션의 항목에서는 Azure Resource Manager(ARM) 프레임워크의 Microsoft Azure HDInsight용 Azure PowerShell cmdlet을 ARM 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="554ee-104">이러한 cmdlet은 HDInsight 클러스터 및 해당 클러스터에서 실행되는 작업을 관리하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="554ee-105">cmdlet은 Microsoft.Azure.Commands.HDInsight 네임스페이스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="554ee-106">Az.HDInsight Cmdlet</span><span class="sxs-lookup"><span data-stu-id="554ee-106">Az.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="554ee-107">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="554ee-107">Add-AzHDInsightClusterIdentity</span></span>](Add-AzHDInsightClusterIdentity.md)
<span data-ttu-id="554ee-108">클러스터 구성 개체에 클러스터 ID를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="554ee-109">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="554ee-109">Add-AzHDInsightComponentVersion</span></span>](Add-AzHDInsightComponentVersion.md)
<span data-ttu-id="554ee-110">클러스터에서 실행되는 서비스에 대한 버전을 클러스터 구성 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="554ee-111">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="554ee-111">Add-AzHDInsightConfigValue</span></span>](Add-AzHDInsightConfigValue.md)
<span data-ttu-id="554ee-112">Hadoop 구성 값 사용자 지정 및/또는 Hive 공유 라이브러리 사용자 지정을 클러스터 구성 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="554ee-113">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="554ee-113">Add-AzHDInsightMetastore</span></span>](Add-AzHDInsightMetastore.md)
<span data-ttu-id="554ee-114">클러스터 구성 개체에 SQL Hive 또는 Oozie metastore 역할을 하는 SQL 데이터베이스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="554ee-115">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="554ee-115">Add-AzHDInsightScriptAction</span></span>](Add-AzHDInsightScriptAction.md)
<span data-ttu-id="554ee-116">클러스터 구성 개체에 스크립트 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="554ee-117">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="554ee-117">Add-AzHDInsightSecurityProfile</span></span>](Add-AzHDInsightSecurityProfile.md)
<span data-ttu-id="554ee-118">클러스터 구성 개체에 보안 프로필을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-118">Adds a security profile to a cluster configuration object.</span></span>

### [<span data-ttu-id="554ee-119">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="554ee-119">Add-AzHDInsightStorage</span></span>](Add-AzHDInsightStorage.md)
<span data-ttu-id="554ee-120">클러스터 구성 개체에 Azure Storage 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="554ee-121">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="554ee-121">Disable-AzHDInsightMonitoring</span></span>](Disable-AzHDInsightMonitoring.md)
<span data-ttu-id="554ee-122">HDInsight 클러스터에서 모니터링을 사용하지 않도록 설정하면 관련 로그가 활성화 중에 지정된 모니터링 작업 영역으로 흐르는 것을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-122">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="554ee-123">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="554ee-123">Enable-AzHDInsightMonitoring</span></span>](Enable-AzHDInsightMonitoring.md)
<span data-ttu-id="554ee-124">HDInsight 클러스터에서 모니터링을 사용하도록 설정하면 사용하도록 설정하는 동안 지정된 모니터링 작업 영역으로 관련 로그가 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-124">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="554ee-125">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="554ee-125">Get-AzHDInsightCluster</span></span>](Get-AzHDInsightCluster.md)
<span data-ttu-id="554ee-126">현재 구독 또는 지정된 리소스 그룹과 연결된 모든 Azure HDInsight 클러스터를 가져온 후 나열하거나 특정 클러스터를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="554ee-127">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="554ee-127">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>](Get-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="554ee-128">HDInsight 클러스터의 자동 조정 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-128">Gets the autoscale configuration of HDInsight cluster.</span></span>

### [<span data-ttu-id="554ee-129">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="554ee-129">Get-AzHDInsightHost</span></span>](Get-AzHDInsightHost.md)
<span data-ttu-id="554ee-130">HDInsight 클러스터의 호스트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-130">Lists the hosts of the HDInsight cluster.</span></span>

### [<span data-ttu-id="554ee-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="554ee-131">Get-AzHDInsightJob</span></span>](Get-AzHDInsightJob.md)
<span data-ttu-id="554ee-132">클러스터에서 작업 목록을 가져온 후 역순으로 나열하거나 특정 작업을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-132">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="554ee-133">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="554ee-133">Get-AzHDInsightJobOutput</span></span>](Get-AzHDInsightJobOutput.md)
<span data-ttu-id="554ee-134">지정된 클러스터와 연결된 저장소 계정에서 작업의 로그 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-134">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="554ee-135">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="554ee-135">Get-AzHDInsightMonitoring</span></span>](Get-AzHDInsightMonitoring.md)
<span data-ttu-id="554ee-136">클러스터의 모니터링 설치 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-136">Gets the status of monitoring installation on the cluster.</span></span>

### [<span data-ttu-id="554ee-137">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="554ee-137">Get-AzHDInsightPersistedScriptAction</span></span>](Get-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="554ee-138">클러스터에 대한 지속형 스크립트 작업을 얻거나 시간 순서로 나열하거나 지정된 지속형 스크립트 동작에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-138">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="554ee-139">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="554ee-139">Get-AzHDInsightProperty</span></span>](Get-AzHDInsightProperty.md)
<span data-ttu-id="554ee-140">사용 가능한 위치 및 용량과 같은 HDInsight 서비스에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-140">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="554ee-141">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="554ee-141">Get-AzHDInsightScriptActionHistory</span></span>](Get-AzHDInsightScriptActionHistory.md)
<span data-ttu-id="554ee-142">클러스터에 대한 스크립트 작업 기록을 얻거나 역순으로 나열하거나 이전에 실행한 스크립트 동작의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-142">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="554ee-143">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="554ee-143">Invoke-AzHDInsightHiveJob</span></span>](Invoke-AzHDInsightHiveJob.md)
<span data-ttu-id="554ee-144">HDInsight 클러스터에 Hive 쿼리를 제출하고 쿼리 결과를 한 번의 작업으로 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="554ee-145">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="554ee-145">New-AzHDInsightCluster</span></span>](New-AzHDInsightCluster.md)
<span data-ttu-id="554ee-146">현재 구독에 대해 지정된 리소스 그룹에 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="554ee-147">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="554ee-147">New-AzHDInsightClusterAutoscaleConfiguration</span></span>](New-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="554ee-148">Azure HDInsight 클러스터의 자동 조정 구성을 설명하는 지속되지 않는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-148">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="554ee-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="554ee-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
<span data-ttu-id="554ee-150">일정 기반 자동 조정 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-150">Creates Schedule-based autoscale condition.</span></span>

### [<span data-ttu-id="554ee-151">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="554ee-151">New-AzHDInsightClusterConfig</span></span>](New-AzHDInsightClusterConfig.md)
<span data-ttu-id="554ee-152">Azure HDInsight 클러스터 구성을 설명하는 비 지속형 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-152">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="554ee-153">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="554ee-153">New-AzHDInsightHiveJobDefinition</span></span>](New-AzHDInsightHiveJobDefinition.md)
<span data-ttu-id="554ee-154">Hive 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-154">Creates a Hive job object.</span></span>

### [<span data-ttu-id="554ee-155">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="554ee-155">New-AzHDInsightMapReduceJobDefinition</span></span>](New-AzHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="554ee-156">MapReduce 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-156">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="554ee-157">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="554ee-157">New-AzHDInsightPigJobDefinition</span></span>](New-AzHDInsightPigJobDefinition.md)
<span data-ttu-id="554ee-158">Pig 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-158">Creates a Pig job object.</span></span>

### [<span data-ttu-id="554ee-159">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="554ee-159">New-AzHDInsightSqoopJobDefinition</span></span>](New-AzHDInsightSqoopJobDefinition.md)
<span data-ttu-id="554ee-160">Sqoop 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-160">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="554ee-161">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="554ee-161">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="554ee-162">Streaming MapReduce 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-162">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="554ee-163">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="554ee-163">Remove-AzHDInsightCluster</span></span>](Remove-AzHDInsightCluster.md)
<span data-ttu-id="554ee-164">현재 구독에서 지정된 HDInsight 클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-164">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="554ee-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="554ee-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="554ee-166">HDInsight 클러스터의 자동 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-166">Removes the autoscale configuration of the HDInsight cluster.</span></span>

### [<span data-ttu-id="554ee-167">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="554ee-167">Remove-AzHDInsightPersistedScriptAction</span></span>](Remove-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="554ee-168">HDInsight 클러스터에서 지속된 스크립트 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-168">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="554ee-169">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="554ee-169">Restart-AzHDInsightHost</span></span>](Restart-AzHDInsightHost.md)
<span data-ttu-id="554ee-170">HDInsight 클러스터의 특정 호스트를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-170">Restarts the specific hosts of HDInsight cluster.</span></span>

### [<span data-ttu-id="554ee-171">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="554ee-171">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>](Set-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="554ee-172">Azure HDInsight 클러스터의 자동 조정 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-172">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="554ee-173">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="554ee-173">Set-AzHDInsightClusterDiskEncryptionKey</span></span>](Set-AzHDInsightClusterDiskEncryptionKey.md)
<span data-ttu-id="554ee-174">지정된 HDInsight 클러스터의 디스크 암호화 키를 회전합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-174">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

### [<span data-ttu-id="554ee-175">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="554ee-175">Set-AzHDInsightClusterSize</span></span>](Set-AzHDInsightClusterSize.md)
<span data-ttu-id="554ee-176">지정된 클러스터의 Worker 노드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-176">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="554ee-177">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="554ee-177">Set-AzHDInsightDefaultStorage</span></span>](Set-AzHDInsightDefaultStorage.md)
<span data-ttu-id="554ee-178">클러스터 구성 개체에서 기본 Storage 계정 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-178">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="554ee-179">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="554ee-179">Set-AzHDInsightGatewayCredential</span></span>](Set-AzHDInsightGatewayCredential.md)
<span data-ttu-id="554ee-180">Azure HDInsight 클러스터의 게이트웨이 HTTP 자격 증명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-180">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="554ee-181">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="554ee-181">Set-AzHDInsightPersistedScriptAction</span></span>](Set-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="554ee-182">이전에 실행한 스크립트 작업을 지속형 스크립트 동작으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-182">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="554ee-183">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="554ee-183">Start-AzHDInsightJob</span></span>](Start-AzHDInsightJob.md)
<span data-ttu-id="554ee-184">지정된 클러스터에서 정의된 Azure HDInsight 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-184">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="554ee-185">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="554ee-185">Stop-AzHDInsightJob</span></span>](Stop-AzHDInsightJob.md)
<span data-ttu-id="554ee-186">클러스터에서 지정된 실행 중인 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-186">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="554ee-187">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="554ee-187">Submit-AzHDInsightScriptAction</span></span>](Submit-AzHDInsightScriptAction.md)
<span data-ttu-id="554ee-188">Azure HDInsight 클러스터에 새 스크립트 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-188">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="554ee-189">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="554ee-189">Use-AzHDInsightCluster</span></span>](Use-AzHDInsightCluster.md)
<span data-ttu-id="554ee-190">클러스터 cmdlet과 함께 사용할 Invoke-RmAzureHDInsightHiveJob 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-190">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="554ee-191">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="554ee-191">Wait-AzHDInsightJob</span></span>](Wait-AzHDInsightJob.md)
<span data-ttu-id="554ee-192">지정된 작업의 완료 또는 실패를 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="554ee-192">Waits for the completion or failure of a specified job.</span></span>

