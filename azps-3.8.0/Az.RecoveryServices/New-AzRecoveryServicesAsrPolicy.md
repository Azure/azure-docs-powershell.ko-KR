---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: d120054a7eef5afd27101d84911a1a57a0b4819a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044701"
---
# <span data-ttu-id="3bd0f-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="3bd0f-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="3bd0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bd0f-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd0f-103">Azure Site Recovery 복제 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="3bd0f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3bd0f-104">SYNTAX</span></span>

### <span data-ttu-id="3bd0f-105">HyperVToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="3bd0f-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bd0f-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="3bd0f-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bd0f-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="3bd0f-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bd0f-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3bd0f-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd0f-109">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="3bd0f-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd0f-110">설명은</span><span class="sxs-lookup"><span data-stu-id="3bd0f-110">DESCRIPTION</span></span>
<span data-ttu-id="3bd0f-111">**새 AzRecoveryServicesAsrPolicy** Cmdlet은 Azure Site Recovery 복제 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="3bd0f-112">복제 정책은 복제 빈도 및 복구 지점 수와 같은 복제 설정을 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="3bd0f-113">예제의</span><span class="sxs-lookup"><span data-stu-id="3bd0f-113">EXAMPLES</span></span>

### <span data-ttu-id="3bd0f-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="3bd0f-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="3bd0f-115">지정 된 매개 변수를 사용 하 여 복제 정책 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="3bd0f-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="3bd0f-116">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

Name             : 1c609a5b-324e-461c-866f-ad58f944df25
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/1c609a5b-324e-461c-866f-ad58f944df25
Type             :
JobType          : AddProtectionProfile
DisplayName      : Create replication policy
ClientRequestId  : b10c83ee-fee2-42d4-ad1d-dfc3e166faab ActivityId: 67e8453c-fae0-465f-801c-dfa2e6e6ee23
State            : Succeeded
StateDescription : Completed
StartTime        : 8/29/2017 10:18:10 AM
EndTime          : 8/29/2017 10:18:11 AM
TargetObjectId   : bb8e8c57-221d-5668-9d82-b15a3e19a6a3
TargetObjectType : ProtectionProfile
TargetObjectName : abc122
AllowedActions   :
Tasks            : {Prerequisites check for creating the replication policy, Creating the replication policy}
Errors           : {}
```

<span data-ttu-id="3bd0f-117">지정 된 매개 변수를 사용 하 여 복제 정책 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="3bd0f-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="3bd0f-118">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
Name             : ed69e451-878b-4f19-9c0f-73184be05eaf
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/ed69e451-878b-4f19-9c0f-73184be05eaf
Type             :
JobType          :
DisplayName      :
ClientRequestId  : d8922fa2-303c-4eb4-b556-e07969ea6fba ActivityId: 9e946cdf-2351-44c2-9aef-70ef2eab29b4
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

### <span data-ttu-id="3bd0f-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="3bd0f-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="3bd0f-120">지정 된 매개 변수를 사용 하 여 복제 정책 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3bd0f-121">변수</span><span class="sxs-lookup"><span data-stu-id="3bd0f-121">PARAMETERS</span></span>

### <span data-ttu-id="3bd0f-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="3bd0f-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="3bd0f-123">응용 프로그램 일치 복구 지점을 만들 빈도 (시간)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-124">-인증</span><span class="sxs-lookup"><span data-stu-id="3bd0f-124">-Authentication</span></span>
<span data-ttu-id="3bd0f-125">사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="3bd0f-126">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-126">Valid values are:</span></span>

- <span data-ttu-id="3bd0f-127">인증</span><span class="sxs-lookup"><span data-stu-id="3bd0f-127">Certificate</span></span>
-  <span data-ttu-id="3bd0f-128">커버로스</span><span class="sxs-lookup"><span data-stu-id="3bd0f-128">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3bd0f-129">-AzureToAzure</span></span>
<span data-ttu-id="3bd0f-130">Switch 매개 변수 azure에서 azure 정책 만들기에 대 한 시나리오를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-130">Switch parameter specifies the scenario for azure to azure policy creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="3bd0f-131">-AzureToVMware</span></span>
<span data-ttu-id="3bd0f-132">Switch 매개 변수 azure에서 vMWare 정책 만들기에 대 한 시나리오를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-132">Switch parameter specifies the scenario for azure to vMWare policy creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-133">-압축</span><span class="sxs-lookup"><span data-stu-id="3bd0f-133">-Compression</span></span>
<span data-ttu-id="3bd0f-134">압축을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd0f-135">-DefaultProfile</span></span>
<span data-ttu-id="3bd0f-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="3bd0f-137">-HyperVToAzure</span></span>
<span data-ttu-id="3bd0f-138">Hyper-v 가상 컴퓨터를 Azure로 복제 하는 데 정책을 지정 하는 스위치 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="3bd0f-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="3bd0f-140">정책에 대 한 multiVm 동기화 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-140">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-141">-이름</span><span class="sxs-lookup"><span data-stu-id="3bd0f-141">-Name</span></span>
<span data-ttu-id="3bd0f-142">ASR 복제 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-142">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="3bd0f-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="3bd0f-144">유지할 번호 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3bd0f-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="3bd0f-146">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="3bd0f-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="3bd0f-148">주어진 시간에 대 한 복구 지점을 시간 단위로 보존 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-148">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="3bd0f-149">-ReplicaDeletion</span></span>
<span data-ttu-id="3bd0f-150">VMM 관리 사이트에서 다른 복제를 사용 하지 않도록 설정할 때 복제 가상 컴퓨터를 삭제할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="3bd0f-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="3bd0f-152">복제 빈도 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="3bd0f-153">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-153">Valid values are:</span></span>

- <span data-ttu-id="3bd0f-154">30</span><span class="sxs-lookup"><span data-stu-id="3bd0f-154">30</span></span>
- <span data-ttu-id="3bd0f-155">300</span><span class="sxs-lookup"><span data-stu-id="3bd0f-155">300</span></span>
- <span data-ttu-id="3bd0f-156">900</span><span class="sxs-lookup"><span data-stu-id="3bd0f-156">900</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="3bd0f-157">-ReplicationMethod</span></span>
<span data-ttu-id="3bd0f-158">복제 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-158">Specifies the replication method.</span></span>
<span data-ttu-id="3bd0f-159">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-159">Valid values are:</span></span>

- <span data-ttu-id="3bd0f-160">온라인</span><span class="sxs-lookup"><span data-stu-id="3bd0f-160">Online</span></span>
- <span data-ttu-id="3bd0f-161">이거나</span><span class="sxs-lookup"><span data-stu-id="3bd0f-161">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="3bd0f-162">-ReplicationPort</span></span>
<span data-ttu-id="3bd0f-163">복제에 사용 되는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-163">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="3bd0f-164">-ReplicationProvider</span></span>
<span data-ttu-id="3bd0f-165">정책에 대 한 복제 공급자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-165">Specifies the replication provider for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="3bd0f-166">-ReplicationStartTime</span></span>
<span data-ttu-id="3bd0f-167">복제 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-167">Specifies the replication start time.</span></span>
<span data-ttu-id="3bd0f-168">작업의 시작 부분에서 24 시간 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-168">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="3bd0f-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="3bd0f-170">경고가 표시 되는 RPO 임계값 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-170">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="3bd0f-171">-VmmToVmm</span></span>
<span data-ttu-id="3bd0f-172">정책 지정을 위한 스위치 매개 변수는 VMM 서버에서 관리 하는 Hyper-v 사이트 간에 복제 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="3bd0f-173">-VMwareToAzure</span></span>
<span data-ttu-id="3bd0f-174">생성 되는 복제 정책이 VMware 가상 머신 및/또는 실제 서버를 Azure로 복제 하는 데 사용 됨을 지정 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-175">-확인</span><span class="sxs-lookup"><span data-stu-id="3bd0f-175">-Confirm</span></span>
<span data-ttu-id="3bd0f-176">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd0f-177">-WhatIf</span></span>
<span data-ttu-id="3bd0f-178">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bd0f-179">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-179">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd0f-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd0f-180">CommonParameters</span></span>
<span data-ttu-id="3bd0f-181">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd0f-182">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3bd0f-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd0f-183">입력</span><span class="sxs-lookup"><span data-stu-id="3bd0f-183">INPUTS</span></span>

### <span data-ttu-id="3bd0f-184">않아야</span><span class="sxs-lookup"><span data-stu-id="3bd0f-184">None</span></span>

## <span data-ttu-id="3bd0f-185">출력</span><span class="sxs-lookup"><span data-stu-id="3bd0f-185">OUTPUTS</span></span>

### <span data-ttu-id="3bd0f-186">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="3bd0f-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3bd0f-187">상속자</span><span class="sxs-lookup"><span data-stu-id="3bd0f-187">NOTES</span></span>

## <span data-ttu-id="3bd0f-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3bd0f-188">RELATED LINKS</span></span>

[<span data-ttu-id="3bd0f-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="3bd0f-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="3bd0f-190">제거-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="3bd0f-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
