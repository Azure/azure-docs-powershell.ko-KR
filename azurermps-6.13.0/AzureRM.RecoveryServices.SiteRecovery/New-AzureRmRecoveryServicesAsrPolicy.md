---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: e6145ee1773a0ecee3ebb1f8c9b5b9e2386cf229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524319"
---
# <span data-ttu-id="be2a2-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="be2a2-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="be2a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="be2a2-103">Azure Site Recovery 복제 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be2a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be2a2-104">SYNTAX</span></span>

### <span data-ttu-id="be2a2-105">HyperVToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="be2a2-105">HyperVToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be2a2-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="be2a2-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be2a2-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="be2a2-107">AzureToVMware</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be2a2-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="be2a2-108">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be2a2-109">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="be2a2-109">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be2a2-110">설명은</span><span class="sxs-lookup"><span data-stu-id="be2a2-110">DESCRIPTION</span></span>
<span data-ttu-id="be2a2-111">**새 AzureRmRecoveryServicesAsrPolicy** Cmdlet은 Azure Site Recovery 복제 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-111">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="be2a2-112">복제 정책은 복제 빈도 및 복구 지점 수와 같은 복제 설정을 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="be2a2-113">예제의</span><span class="sxs-lookup"><span data-stu-id="be2a2-113">EXAMPLES</span></span>

### <span data-ttu-id="be2a2-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="be2a2-114">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="be2a2-115">지정 된 매개 변수를 사용 하 여 복제 정책 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="be2a2-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="be2a2-116">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

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

<span data-ttu-id="be2a2-117">지정 된 매개 변수를 사용 하 여 복제 정책 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="be2a2-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="be2a2-118">Example 3</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
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

### <span data-ttu-id="be2a2-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="be2a2-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzureRmRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="be2a2-120">지정 된 매개 변수를 사용 하 여 복제 정책 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="be2a2-121">변수</span><span class="sxs-lookup"><span data-stu-id="be2a2-121">PARAMETERS</span></span>

### <span data-ttu-id="be2a2-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="be2a2-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="be2a2-123">응용 프로그램 일치 복구 지점을 만들 빈도 (시간)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="be2a2-124">-인증</span><span class="sxs-lookup"><span data-stu-id="be2a2-124">-Authentication</span></span>
<span data-ttu-id="be2a2-125">사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="be2a2-126">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-126">Valid values are:</span></span>

- <span data-ttu-id="be2a2-127">인증</span><span class="sxs-lookup"><span data-stu-id="be2a2-127">Certificate</span></span>
-  <span data-ttu-id="be2a2-128">커버로스</span><span class="sxs-lookup"><span data-stu-id="be2a2-128">Kerberos</span></span>

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

### <span data-ttu-id="be2a2-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="be2a2-129">-AzureToAzure</span></span>
<span data-ttu-id="be2a2-130">만드는 복제 정책이 두 Azure 지역 간에 Azure 가상 컴퓨터를 복제 하는 데 사용 됨을 지정 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-130">Switch parameter specifying that the replication policy being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

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

### <span data-ttu-id="be2a2-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="be2a2-131">-AzureToVMware</span></span>
<span data-ttu-id="be2a2-132">생성 되는 복제 정책이 VMware 가상 머신 및 Azure에서 실행 되는 실제 서버를 온-프레미스 VMware 사이트로 다시 복제 하는 데 사용 됨을 지정 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-132">Switch parameter specifying that the replication policy being created will be used to reverse replicate failed over VMware virtual machines and Physical servers running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="be2a2-133">-압축</span><span class="sxs-lookup"><span data-stu-id="be2a2-133">-Compression</span></span>
<span data-ttu-id="be2a2-134">압축을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-134">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="be2a2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be2a2-135">-DefaultProfile</span></span>
<span data-ttu-id="be2a2-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be2a2-137">-암호화</span><span class="sxs-lookup"><span data-stu-id="be2a2-137">-Encryption</span></span>
<span data-ttu-id="be2a2-138">{{암호화 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="be2a2-138">{{Fill Encryption Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be2a2-139">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="be2a2-139">-HyperVToAzure</span></span>
<span data-ttu-id="be2a2-140">Hyper-v 가상 컴퓨터를 Azure로 복제 하는 데 정책을 지정 하는 스위치 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-140">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

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

### <span data-ttu-id="be2a2-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="be2a2-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="be2a2-142">정책에 대 한 multiVm 동기화 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-142">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="be2a2-143">-이름</span><span class="sxs-lookup"><span data-stu-id="be2a2-143">-Name</span></span>
<span data-ttu-id="be2a2-144">ASR 복제 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-144">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="be2a2-145">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="be2a2-145">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="be2a2-146">유지할 번호 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-146">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="be2a2-147">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="be2a2-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="be2a2-148">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-148">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="be2a2-149">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="be2a2-149">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="be2a2-150">주어진 시간에 대 한 복구 지점을 시간 단위로 보존 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-150">Retain the recovery points for given time in hours.</span></span>

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

### <span data-ttu-id="be2a2-151">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="be2a2-151">-ReplicaDeletion</span></span>
<span data-ttu-id="be2a2-152">VMM 관리 사이트에서 다른 복제를 사용 하지 않도록 설정할 때 복제 가상 컴퓨터를 삭제할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-152">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="be2a2-153">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="be2a2-153">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="be2a2-154">복제 빈도 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-154">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="be2a2-155">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-155">Valid values are:</span></span>

- <span data-ttu-id="be2a2-156">30</span><span class="sxs-lookup"><span data-stu-id="be2a2-156">30</span></span>
- <span data-ttu-id="be2a2-157">300</span><span class="sxs-lookup"><span data-stu-id="be2a2-157">300</span></span>
- <span data-ttu-id="be2a2-158">900</span><span class="sxs-lookup"><span data-stu-id="be2a2-158">900</span></span>

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

### <span data-ttu-id="be2a2-159">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="be2a2-159">-ReplicationMethod</span></span>
<span data-ttu-id="be2a2-160">복제 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-160">Specifies the replication method.</span></span>
<span data-ttu-id="be2a2-161">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-161">Valid values are:</span></span>

- <span data-ttu-id="be2a2-162">온라인</span><span class="sxs-lookup"><span data-stu-id="be2a2-162">Online</span></span>
- <span data-ttu-id="be2a2-163">이거나</span><span class="sxs-lookup"><span data-stu-id="be2a2-163">Offline</span></span>

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

### <span data-ttu-id="be2a2-164">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="be2a2-164">-ReplicationPort</span></span>
<span data-ttu-id="be2a2-165">복제에 사용 되는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-165">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="be2a2-166">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="be2a2-166">-ReplicationProvider</span></span>
<span data-ttu-id="be2a2-167">정책에 대 한 복제 공급자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-167">Specifies the replication provider for the policy.</span></span>

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

### <span data-ttu-id="be2a2-168">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="be2a2-168">-ReplicationStartTime</span></span>
<span data-ttu-id="be2a2-169">복제 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-169">Specifies the replication start time.</span></span>
<span data-ttu-id="be2a2-170">작업의 시작 부분에서 24 시간 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-170">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="be2a2-171">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="be2a2-171">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="be2a2-172">경고가 표시 되는 RPO 임계값 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-172">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="be2a2-173">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="be2a2-173">-VmmToVmm</span></span>
<span data-ttu-id="be2a2-174">정책 지정을 위한 스위치 매개 변수는 VMM 서버에서 관리 하는 Hyper-v 사이트 간에 복제 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-174">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="be2a2-175">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="be2a2-175">-VMwareToAzure</span></span>
<span data-ttu-id="be2a2-176">생성 되는 복제 정책이 VMware 가상 머신 및/또는 실제 서버를 Azure로 복제 하는 데 사용 됨을 지정 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-176">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="be2a2-177">-확인</span><span class="sxs-lookup"><span data-stu-id="be2a2-177">-Confirm</span></span>
<span data-ttu-id="be2a2-178">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be2a2-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be2a2-179">-WhatIf</span></span>
<span data-ttu-id="be2a2-180">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-180">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be2a2-181">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be2a2-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be2a2-182">CommonParameters</span></span>
<span data-ttu-id="be2a2-183">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be2a2-184">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be2a2-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be2a2-185">입력</span><span class="sxs-lookup"><span data-stu-id="be2a2-185">INPUTS</span></span>

### <span data-ttu-id="be2a2-186">않아야</span><span class="sxs-lookup"><span data-stu-id="be2a2-186">None</span></span>

## <span data-ttu-id="be2a2-187">출력</span><span class="sxs-lookup"><span data-stu-id="be2a2-187">OUTPUTS</span></span>

### <span data-ttu-id="be2a2-188">System. 개체</span><span class="sxs-lookup"><span data-stu-id="be2a2-188">System.Object</span></span>

## <span data-ttu-id="be2a2-189">상속자</span><span class="sxs-lookup"><span data-stu-id="be2a2-189">NOTES</span></span>

## <span data-ttu-id="be2a2-190">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be2a2-190">RELATED LINKS</span></span>

[<span data-ttu-id="be2a2-191">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="be2a2-191">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="be2a2-192">제거-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="be2a2-192">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
