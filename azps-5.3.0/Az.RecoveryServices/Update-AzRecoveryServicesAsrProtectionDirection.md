---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494583"
---
# <span data-ttu-id="481d5-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="481d5-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="481d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="481d5-102">SYNOPSIS</span></span>
<span data-ttu-id="481d5-103">지정된 복제 보호 항목 또는 복구 계획에 대한 복제 방향을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="481d5-104">실패한 복제된 항목 또는 복구 계획을 다시 보호/역방향 복제하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="481d5-105">구문</span><span class="sxs-lookup"><span data-stu-id="481d5-105">SYNTAX</span></span>

### <span data-ttu-id="481d5-106">ByRPIObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="481d5-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="481d5-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="481d5-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="481d5-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="481d5-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="481d5-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="481d5-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="481d5-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="481d5-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="481d5-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="481d5-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="481d5-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="481d5-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="481d5-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="481d5-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="481d5-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="481d5-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="481d5-115">설명</span><span class="sxs-lookup"><span data-stu-id="481d5-115">DESCRIPTION</span></span>
<span data-ttu-id="481d5-116">**Update-AzRecoveryServicesAsrProtectionDirection** cmdlet은 커밋 장애 조치(failover) 작업이 완료된 후 지정된 Azure Site Recovery 개체에 대한 복제 방향을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="481d5-117">예제</span><span class="sxs-lookup"><span data-stu-id="481d5-117">EXAMPLES</span></span>

### <span data-ttu-id="481d5-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="481d5-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="481d5-119">지정된 복구 계획에 대한 업데이트 방향 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="481d5-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="481d5-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="481d5-121">보호 컨테이너 매핑 및 캐시 저장소(VM과 동일한 지역에 있는)를 사용하여 정의된 대상 Azure 지역에서 지정된 복제 보호 항목에 대한 업데이트 방향 작업을 시작하세요.</span><span class="sxs-lookup"><span data-stu-id="481d5-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="481d5-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="481d5-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="481d5-123">보호 컨테이너 매핑 및 제공된 디스크 복제 구성으로 정의된 대상 Azure 지역에서 지정된 복제 보호 항목에 대한 업데이트 방향 작업을 시작하세요.</span><span class="sxs-lookup"><span data-stu-id="481d5-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="481d5-124">예제 4</span><span class="sxs-lookup"><span data-stu-id="481d5-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="481d5-125">보호 컨테이너 매핑 및 제공된 디스크 복제 구성으로 정의된 대상 Azure 지역에서 지정된 암호화된 복제 보호 항목에 대한 업데이트 방향 작업을 시작하세요.</span><span class="sxs-lookup"><span data-stu-id="481d5-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="481d5-126">예제 5</span><span class="sxs-lookup"><span data-stu-id="481d5-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="481d5-127">보호 컨테이너 매핑 및 캐시 저장소(VM과 동일한 지역에 있는) 및 근접 배치 그룹을 사용하여 정의된 대상 Azure 지역에서 지정된 복제 보호 항목에 대한 업데이트 방향 작업을 시작하세요.</span><span class="sxs-lookup"><span data-stu-id="481d5-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="481d5-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="481d5-128">PARAMETERS</span></span>

### <span data-ttu-id="481d5-129">-Account</span><span class="sxs-lookup"><span data-stu-id="481d5-129">-Account</span></span>
<span data-ttu-id="481d5-130">필요한 경우 모바일 서비스를 푸시 설치하는 데 사용할 실행 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="481d5-131">ASR 패브릭의 실행 계정 목록에서 하나만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="481d5-132">-AzureToAzure</span></span>
<span data-ttu-id="481d5-133">Azure에서 Azure로 재해 복구를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-133">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="481d5-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="481d5-135">재해 복구를 위한 디스크 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-135">Specifies the disk configuration for disaster recovery.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="481d5-136">-AzureToVMware</span></span>
<span data-ttu-id="481d5-137">Azure에서 vMWare로의 전환 시나리오를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="481d5-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="481d5-138">-DataStore</span></span>
<span data-ttu-id="481d5-139">vmdisk에 사용할 VMware 데이터 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-139">The VMware data-store to be used for the vmdisk's.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="481d5-140">-DefaultProfile</span></span>
<span data-ttu-id="481d5-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="481d5-142">-Direction</span><span class="sxs-lookup"><span data-stu-id="481d5-142">-Direction</span></span>
<span data-ttu-id="481d5-143">장애 조치(failover) 후 업데이트 작업에 사용할 방향을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="481d5-144">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="481d5-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="481d5-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="481d5-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="481d5-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="481d5-146">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="481d5-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="481d5-148">장애 조치(failover) 후 복구 VM으로 사용할 버전(Azure 디스크 암호화)을 사용하여 디스크 암호화 비밀 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="481d5-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="481d5-150">장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 비밀 자격 증명 모음 ID(Azure 디스크 암호화)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="481d5-151">-HyperVToAzure</span></span>
<span data-ttu-id="481d5-152">장애 조치(failback) 후 Hyper-V 가상 머신을 다시 보류합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="481d5-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="481d5-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="481d5-154">장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 키 URL(Azure 디스크 암호화)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="481d5-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="481d5-156">장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 keyVault ID(Azure Disk Encryption)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="481d5-157">-LogStorageAccountId</span></span>
<span data-ttu-id="481d5-158">VM의 복제 로그를 저장할 저장소 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="481d5-159">-MasterTarget</span></span>
<span data-ttu-id="481d5-160">마스터 대상 서버 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-160">Master Target Server Details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="481d5-161">-ProcessServer</span></span>
<span data-ttu-id="481d5-162">복제에 사용할 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-162">Process Server to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="481d5-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="481d5-164">복제에 사용할 보호 containerMapping입니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-164">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="481d5-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="481d5-166">장애 조치 시 가상 머신을 만들어야 하는 가용성 집합</span><span class="sxs-lookup"><span data-stu-id="481d5-166">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="481d5-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="481d5-168">복제할 Azure 저장소 계정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="481d5-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="481d5-170">복구 Azure VM에 대한 부팅 진단을 위한 저장소 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="481d5-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="481d5-172">이 가상 머신을 장애 조치(failover)할 복구 클라우드 서비스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="481d5-173">-RecoveryPlan</span></span>
<span data-ttu-id="481d5-174">ASR 복구 계획 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-174">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="481d5-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="481d5-176">이 가상 머신을 장애 조치할 복구 근접 배치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="481d5-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="481d5-178">보호된 VM에 대한 복구 resourceGroup ID입니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-178">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="481d5-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="481d5-180">ASR 복제 보호 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-180">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="481d5-181">-RetentionVolume</span></span>
<span data-ttu-id="481d5-182">사용할 마스터 대상 서버의 보존 볼륨입니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-182">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481d5-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="481d5-183">-VmmToVmm</span></span>
<span data-ttu-id="481d5-184">두 VMM 관리 Hyper-V 사이트 간에 보호되는 실패한 Hyper-V 가상 머신에 대한 복제 방향을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="481d5-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="481d5-185">-VMwareToAzure</span></span>
<span data-ttu-id="481d5-186">VMware에서 Azure로 복제 방향을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="481d5-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="481d5-187">-Confirm</span></span>
<span data-ttu-id="481d5-188">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="481d5-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="481d5-189">-WhatIf</span></span>
<span data-ttu-id="481d5-190">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="481d5-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="481d5-191">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="481d5-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="481d5-192">CommonParameters</span></span>
<span data-ttu-id="481d5-193">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="481d5-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="481d5-194">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="481d5-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="481d5-195">입력</span><span class="sxs-lookup"><span data-stu-id="481d5-195">INPUTS</span></span>

### <span data-ttu-id="481d5-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="481d5-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="481d5-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="481d5-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="481d5-198">출력</span><span class="sxs-lookup"><span data-stu-id="481d5-198">OUTPUTS</span></span>

### <span data-ttu-id="481d5-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="481d5-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="481d5-200">참고 사항</span><span class="sxs-lookup"><span data-stu-id="481d5-200">NOTES</span></span>

## <span data-ttu-id="481d5-201">관련 링크</span><span class="sxs-lookup"><span data-stu-id="481d5-201">RELATED LINKS</span></span>
