---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 2255a2397c7096ec1a7b5f45dc4fa699649b071a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005819"
---
# <span data-ttu-id="f0770-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f0770-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="f0770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0770-102">SYNOPSIS</span></span>
<span data-ttu-id="f0770-103">Azure Site Recovery 복제 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="f0770-104">구문</span><span class="sxs-lookup"><span data-stu-id="f0770-104">SYNTAX</span></span>

### <span data-ttu-id="f0770-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="f0770-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0770-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="f0770-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0770-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f0770-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0770-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="f0770-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0770-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="f0770-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0770-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="f0770-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0770-111">설명</span><span class="sxs-lookup"><span data-stu-id="f0770-111">DESCRIPTION</span></span>
<span data-ttu-id="f0770-112">**Update-AzRecoveryServicesAsrPolicy** cmdlet은 지정된 Azure Site Recovery 복제 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="f0770-113">예제</span><span class="sxs-lookup"><span data-stu-id="f0770-113">EXAMPLES</span></span>

### <span data-ttu-id="f0770-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0770-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="f0770-115">지정된 매개 변수를 사용하여 업데이트 복제 정책 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f0770-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="f0770-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="f0770-117">지정된 매개 변수를 사용하여 Azure 복제 정책 작업에 대한 업데이트를 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f0770-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="f0770-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="f0770-119">지정된 매개 변수를 사용하여 Azure 복제 정책에 대한 업데이트를 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f0770-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f0770-120">PARAMETERS</span></span>

### <span data-ttu-id="f0770-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="f0770-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="f0770-122">애플리케이션 일관된 복구 지점을 만들 빈도(시간)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="f0770-123">-Authentication</span><span class="sxs-lookup"><span data-stu-id="f0770-123">-Authentication</span></span>
<span data-ttu-id="f0770-124">사용되는 인증 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f0770-125">-AzureToAzure</span></span>
<span data-ttu-id="f0770-126">Azure에서 Azure로의 재해 복구를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-126">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="f0770-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="f0770-127">-AzureToVMware</span></span>
<span data-ttu-id="f0770-128">vMWare 재해 복구에 Azure를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-128">Specifies the Azure to vMWare disaster recovery.</span></span>

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

### <span data-ttu-id="f0770-129">-압축</span><span class="sxs-lookup"><span data-stu-id="f0770-129">-Compression</span></span>
<span data-ttu-id="f0770-130">압축을 사용하도록 설정해야 하는지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0770-131">-DefaultProfile</span></span>
<span data-ttu-id="f0770-132">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f0770-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="f0770-133">-HyperVToAzure</span></span>
<span data-ttu-id="f0770-134">지정된 정책이 Azure에 가상 머신을 복제하는 데 Hyper-V 매개 변수를 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0770-135">-InputObject</span></span>
<span data-ttu-id="f0770-136">cmdlet의 입력 개체: 업데이트할 복제 정책에 해당하는 ASR 복제 정책 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="f0770-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="f0770-138">정책에 대한 다중Vm 동기화 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-138">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="f0770-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="f0770-140">보존할 수 있는 복구 지점을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-140">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f0770-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f0770-142">복제 대상의 Azure Storage 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="f0770-143">복제 cmdlet을 사용하여 복제를 사용하도록 설정하는 동안 대체가 제공되지 않은 경우 복제를 위한 대상 New-AzRecoveryServicesASRReplicationProtectedItem 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="f0770-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="f0770-145">생성 후 복구 지점을 유지하는 시간(시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-145">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="f0770-146">-ReplicaDeletion</span></span>
<span data-ttu-id="f0770-147">VMM 관리 사이트에서 다른 사이트로 복제를 사용할 수 없는 경우 복제본 가상 머신을 삭제해야 하는지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="f0770-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="f0770-149">복제 빈도 간격을 초 단위로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="f0770-150">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="f0770-150">Valid values are:</span></span>

- <span data-ttu-id="f0770-151">30</span><span class="sxs-lookup"><span data-stu-id="f0770-151">30</span></span>
- <span data-ttu-id="f0770-152">300</span><span class="sxs-lookup"><span data-stu-id="f0770-152">300</span></span>
- <span data-ttu-id="f0770-153">900</span><span class="sxs-lookup"><span data-stu-id="f0770-153">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="f0770-154">-ReplicationMethod</span></span>
<span data-ttu-id="f0770-155">복제 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-155">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-156">-복제포트</span><span class="sxs-lookup"><span data-stu-id="f0770-156">-ReplicationPort</span></span>
<span data-ttu-id="f0770-157">복제에 사용되는 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-157">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="f0770-158">-ReplicationStartTime</span></span>
<span data-ttu-id="f0770-159">복제 시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-159">Specifies the replication start time.</span></span>
<span data-ttu-id="f0770-160">작업 시작부터 24시간이 지난 후에야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-160">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="f0770-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="f0770-162">경고하기 위해 몇 분 만에 RPO 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-162">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="f0770-163">-VmmToVmm</span></span>
<span data-ttu-id="f0770-164">지정된 정책이 두 사이트 간에 VMM 관리되는 가상 머신을 Hyper-V 나타내는 스위치 매개 변수를 Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="f0770-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0770-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="f0770-165">-VMwareToAzure</span></span>
<span data-ttu-id="f0770-166">지정된 정책이 VMware 가상 머신을 Azure로 복제하는 데 사용되었음을 나타내는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="f0770-167">-확인</span><span class="sxs-lookup"><span data-stu-id="f0770-167">-Confirm</span></span>
<span data-ttu-id="f0770-168">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0770-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0770-169">-WhatIf</span></span>
<span data-ttu-id="f0770-170">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0770-171">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0770-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0770-172">CommonParameters</span></span>
<span data-ttu-id="f0770-173">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f0770-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0770-174">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0770-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0770-175">입력</span><span class="sxs-lookup"><span data-stu-id="f0770-175">INPUTS</span></span>

### <span data-ttu-id="f0770-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="f0770-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="f0770-177">출력</span><span class="sxs-lookup"><span data-stu-id="f0770-177">OUTPUTS</span></span>

### <span data-ttu-id="f0770-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="f0770-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f0770-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f0770-179">NOTES</span></span>

## <span data-ttu-id="f0770-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0770-180">RELATED LINKS</span></span>
