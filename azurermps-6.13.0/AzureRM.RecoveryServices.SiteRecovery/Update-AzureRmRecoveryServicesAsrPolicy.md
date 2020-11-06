---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 805e421aedbb06b6f9a821b3f575b8a5035c86d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526103"
---
# <span data-ttu-id="f397a-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f397a-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="f397a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f397a-102">SYNOPSIS</span></span>
<span data-ttu-id="f397a-103">Azure Site Recovery 복제 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f397a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f397a-104">SYNTAX</span></span>

### <span data-ttu-id="f397a-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f397a-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f397a-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="f397a-106">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f397a-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f397a-107">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f397a-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="f397a-108">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f397a-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="f397a-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f397a-110">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="f397a-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f397a-111">설명은</span><span class="sxs-lookup"><span data-stu-id="f397a-111">DESCRIPTION</span></span>
<span data-ttu-id="f397a-112">**업데이트 AzureRmRecoveryServicesAsrPolicy** cmdlet은 지정 된 Azure Site Recovery 복제 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-112">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="f397a-113">예제의</span><span class="sxs-lookup"><span data-stu-id="f397a-113">EXAMPLES</span></span>

### <span data-ttu-id="f397a-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="f397a-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="f397a-115">지정 된 매개 변수를 사용 하 여 복제 정책 업데이트 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f397a-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="f397a-116">Example 2</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="f397a-117">지정 된 매개 변수를 사용 하 여 azure to azure 복제 정책 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f397a-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="f397a-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="f397a-119">지정 된 매개 변수를 사용 하 여 azure to azure 복제 정책을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f397a-120">변수</span><span class="sxs-lookup"><span data-stu-id="f397a-120">PARAMETERS</span></span>

### <span data-ttu-id="f397a-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="f397a-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="f397a-122">응용 프로그램 일치 복구 지점을 만들 빈도 (시간)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="f397a-123">-인증</span><span class="sxs-lookup"><span data-stu-id="f397a-123">-Authentication</span></span>
<span data-ttu-id="f397a-124">사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-124">Specifies the type of authentication used.</span></span>

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

### <span data-ttu-id="f397a-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f397a-125">-AzureToAzure</span></span>
<span data-ttu-id="f397a-126">두 Azure 지역 간에 Azure 가상 머신을 복제 하는 데 사용 되는 복제 정책이 업데이트 되도록 지정 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-126">Switch parameter specifying that the replication policy used to replicate Azure virtual machines between two Azure regions will be updated.</span></span>

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

### <span data-ttu-id="f397a-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="f397a-127">-AzureToVMware</span></span>
<span data-ttu-id="f397a-128">Azure에서 실행 되는 가상 컴퓨터를 통해 온-프레미스 VMware 사이트로 다시 복제 하는 데 지정한 정책이 사용 됨을 나타내는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-128">Switch parameter indicating that the specfied policy is used to replicate failed over virtual machines running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="f397a-129">-압축</span><span class="sxs-lookup"><span data-stu-id="f397a-129">-Compression</span></span>
<span data-ttu-id="f397a-130">압축을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-130">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="f397a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f397a-131">-DefaultProfile</span></span>
<span data-ttu-id="f397a-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f397a-133">-암호화</span><span class="sxs-lookup"><span data-stu-id="f397a-133">-Encryption</span></span>
<span data-ttu-id="f397a-134">{{암호화 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="f397a-134">{{Fill Encryption Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f397a-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="f397a-135">-HyperVToAzure</span></span>
<span data-ttu-id="f397a-136">지정한 정책이 Azure에 Hyper-v 가상 컴퓨터를 복제 하는 데 사용 됨을 나타내는 Switch 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-136">Switch parameter indicating that the specfied policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="f397a-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f397a-137">-InputObject</span></span>
<span data-ttu-id="f397a-138">Cmdlet에 대 한 Input 개체: 업데이트할 복제 정책에 해당 하는 ASR 복제 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-138">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="f397a-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="f397a-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="f397a-140">정책에 대 한 multiVm 동기화 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-140">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="f397a-141">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="f397a-141">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="f397a-142">유지할 번호 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-142">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="f397a-143">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f397a-143">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f397a-144">복제 대상의 Azure storage 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-144">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="f397a-145">New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet을 사용 하 여 복제를 사용 하도록 설정 하는 동안 대체가 제공 되지 않은 경우 복제 대상 저장소 계정으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-145">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


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

### <span data-ttu-id="f397a-146">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="f397a-146">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="f397a-147">생성 후 복구 지점을 유지 하는 시간 (시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-147">Time in hours to retain recovery points after creation.</span></span>

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

### <span data-ttu-id="f397a-148">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="f397a-148">-ReplicaDeletion</span></span>
<span data-ttu-id="f397a-149">VMM 관리 사이트에서 다른 복제를 사용 하지 않도록 설정할 때 복제 가상 컴퓨터를 삭제할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-149">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="f397a-150">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="f397a-150">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="f397a-151">복제 빈도 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-151">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="f397a-152">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-152">Valid values are:</span></span>

- <span data-ttu-id="f397a-153">30</span><span class="sxs-lookup"><span data-stu-id="f397a-153">30</span></span>
- <span data-ttu-id="f397a-154">300</span><span class="sxs-lookup"><span data-stu-id="f397a-154">300</span></span>
- <span data-ttu-id="f397a-155">900</span><span class="sxs-lookup"><span data-stu-id="f397a-155">900</span></span>

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

### <span data-ttu-id="f397a-156">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="f397a-156">-ReplicationMethod</span></span>
<span data-ttu-id="f397a-157">복제 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-157">Specifies the replication method.</span></span>

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

### <span data-ttu-id="f397a-158">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="f397a-158">-ReplicationPort</span></span>
<span data-ttu-id="f397a-159">복제에 사용 되는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-159">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="f397a-160">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="f397a-160">-ReplicationStartTime</span></span>
<span data-ttu-id="f397a-161">복제 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-161">Specifies the replication start time.</span></span>
<span data-ttu-id="f397a-162">작업의 시작 부분에서 24 시간 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-162">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="f397a-163">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="f397a-163">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="f397a-164">경고가 표시 되는 RPO 임계값 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-164">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="f397a-165">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="f397a-165">-VmmToVmm</span></span>
<span data-ttu-id="f397a-166">지정한 정책이 두 개의 Hyper-v 사이트 간에 VMM 관리 Hyper-v 가상 컴퓨터를 복제 하는 데 사용 됨을 나타내는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-166">Switch parameter indicating that the specfied policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="f397a-167">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="f397a-167">-VMwareToAzure</span></span>
<span data-ttu-id="f397a-168">지정한 정책이 Azure에 VMware 가상 머신을 복제 하는 데 사용 됨을 나타내는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-168">Switch parameter indicating that the specfied policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="f397a-169">-확인</span><span class="sxs-lookup"><span data-stu-id="f397a-169">-Confirm</span></span>
<span data-ttu-id="f397a-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f397a-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f397a-171">-WhatIf</span></span>
<span data-ttu-id="f397a-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f397a-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f397a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f397a-174">CommonParameters</span></span>
<span data-ttu-id="f397a-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f397a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f397a-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f397a-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f397a-177">입력</span><span class="sxs-lookup"><span data-stu-id="f397a-177">INPUTS</span></span>

### <span data-ttu-id="f397a-178">SiteRecovery. r i m g 정책</span><span class="sxs-lookup"><span data-stu-id="f397a-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="f397a-179">출력</span><span class="sxs-lookup"><span data-stu-id="f397a-179">OUTPUTS</span></span>

### <span data-ttu-id="f397a-180">System. 개체</span><span class="sxs-lookup"><span data-stu-id="f397a-180">System.Object</span></span>

## <span data-ttu-id="f397a-181">상속자</span><span class="sxs-lookup"><span data-stu-id="f397a-181">NOTES</span></span>

## <span data-ttu-id="f397a-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f397a-182">RELATED LINKS</span></span>
