---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 32218fdb966a17cedcb51a2838acae1ae79d9f54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043516"
---
# <span data-ttu-id="6fac7-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="6fac7-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="6fac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fac7-102">SYNOPSIS</span></span>
<span data-ttu-id="6fac7-103">지정 된 복제 보호 항목 또는 복구 계획에 대 한 복제 방향을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="6fac7-104">복제 된 항목 또는 복구 계획을 통해 장애를 다시 방지 하거나 역 복제 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="6fac7-105">구문과</span><span class="sxs-lookup"><span data-stu-id="6fac7-105">SYNTAX</span></span>

### <span data-ttu-id="6fac7-106">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="6fac7-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fac7-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="6fac7-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fac7-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="6fac7-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fac7-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="6fac7-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fac7-110">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="6fac7-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fac7-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6fac7-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fac7-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6fac7-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fac7-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="6fac7-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fac7-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="6fac7-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fac7-115">설명은</span><span class="sxs-lookup"><span data-stu-id="6fac7-115">DESCRIPTION</span></span>
<span data-ttu-id="6fac7-116">**AzRecoveryServicesAsrProtectionDirection** cmdlet은 커밋 장애 조치 작업이 완료 된 후 지정 된 Azure Site Recovery 개체의 복제 방향을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="6fac7-117">예제의</span><span class="sxs-lookup"><span data-stu-id="6fac7-117">EXAMPLES</span></span>

### <span data-ttu-id="6fac7-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="6fac7-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="6fac7-119">지정 된 복구 계획에 대 한 방향 업데이트 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="6fac7-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="6fac7-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="6fac7-121">보호 컨테이너 매핑과 동일한 지역에서 캐시 저장소를 사용 하 여 대상 azure 지역에서 지정 된 복제 보호 항목에 대 한 방향 업데이트 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="6fac7-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="6fac7-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="6fac7-123">보호 컨테이너 매핑과 제공 된 디스크 복제 구성에 정의 된 대상 azure 지역에서 지정 된 복제 보호 항목에 대 한 방향 업데이트 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="6fac7-124">예제 4</span><span class="sxs-lookup"><span data-stu-id="6fac7-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="6fac7-125">보호 컨테이너 매핑과 제공 된 디스크 복제 구성에 정의 된 대상 azure 지역에서 지정 된 암호화 된 복제 항목에 대 한 방향 업데이트 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="6fac7-126">변수</span><span class="sxs-lookup"><span data-stu-id="6fac7-126">PARAMETERS</span></span>

### <span data-ttu-id="6fac7-127">-계정</span><span class="sxs-lookup"><span data-stu-id="6fac7-127">-Account</span></span>
<span data-ttu-id="6fac7-128">필요한 경우 모바일 서비스를 강제 설치 하는 데 사용할 실행 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-128">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="6fac7-129">ASR 패브릭의 실행 계정 목록에서 1 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-129">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="6fac7-130">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6fac7-130">-AzureToAzure</span></span>
<span data-ttu-id="6fac7-131">Azure에서 Azure 재해 복구를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-131">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="6fac7-132">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fac7-132">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="6fac7-133">재해 복구용 디스크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-133">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="6fac7-134">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="6fac7-134">-AzureToVMware</span></span>
<span data-ttu-id="6fac7-135">Azure에서 vMWare로 전환 시나리오를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-135">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="6fac7-136">-데이터 스토어</span><span class="sxs-lookup"><span data-stu-id="6fac7-136">-DataStore</span></span>
<span data-ttu-id="6fac7-137">Vmdisk에 사용 되는 VMware 데이터 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-137">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="6fac7-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fac7-138">-DefaultProfile</span></span>
<span data-ttu-id="6fac7-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6fac7-140">방향</span><span class="sxs-lookup"><span data-stu-id="6fac7-140">-Direction</span></span>
<span data-ttu-id="6fac7-141">업데이트 작업에 대해 장애 조치를 게시 하는 데 사용할 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-141">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="6fac7-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6fac7-143">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="6fac7-143">PrimaryToRecovery</span></span>
- <span data-ttu-id="6fac7-144">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="6fac7-144">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="6fac7-145">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="6fac7-145">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="6fac7-146">장애 조치 후 복구 VM으로 사용할 버전 (Azure 디스크 암호화)이 포함 된 디스크 암호화 비밀 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-146">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6fac7-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="6fac7-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="6fac7-148">장애 조치 후 복구 VM으로 사용할 디스크 암호화 비밀 자격 증명 모음 ID (Azure 디스크 암호화)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6fac7-149">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="6fac7-149">-HyperVToAzure</span></span>
<span data-ttu-id="6fac7-150">장애 복구 후 Hyper-v 가상 컴퓨터를 다시 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-150">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="6fac7-151">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="6fac7-151">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="6fac7-152">장애 조치 후 복구 VM으로 사용할 디스크 암호화 키 URL (Azure 디스크 암호화)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-152">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6fac7-153">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="6fac7-153">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="6fac7-154">장애 조치 후 복구 VM으로 사용할 디스크 암호화 키 keyVault ID (Azure 디스크 암호화)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-154">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6fac7-155">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6fac7-155">-LogStorageAccountId</span></span>
<span data-ttu-id="6fac7-156">Vm의 복제 로그를 저장할 저장소 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-156">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="6fac7-157">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="6fac7-157">-MasterTarget</span></span>
<span data-ttu-id="6fac7-158">마스터 대상 서버 세부 정보.</span><span class="sxs-lookup"><span data-stu-id="6fac7-158">Master Target Server Details.</span></span>

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

### <span data-ttu-id="6fac7-159">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="6fac7-159">-ProcessServer</span></span>
<span data-ttu-id="6fac7-160">복제에 사용할 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-160">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="6fac7-161">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6fac7-161">-ProtectionContainerMapping</span></span>
<span data-ttu-id="6fac7-162">복제에 사용할 보호 containerMapping.</span><span class="sxs-lookup"><span data-stu-id="6fac7-162">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="6fac7-163">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="6fac7-163">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="6fac7-164">장애 조치 시 가상 컴퓨터를 만들 가용성 집합</span><span class="sxs-lookup"><span data-stu-id="6fac7-164">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="6fac7-165">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6fac7-165">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="6fac7-166">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-166">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="6fac7-167">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6fac7-167">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="6fac7-168">복구 azure VM에 대 한 부팅 진단의 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-168">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="6fac7-169">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="6fac7-169">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="6fac7-170">이 가상 컴퓨터를 장애 조치 (failover) 할 복구 클라우드 서비스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-170">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="6fac7-171">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6fac7-171">-RecoveryPlan</span></span>
<span data-ttu-id="6fac7-172">ASR 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-172">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="6fac7-173">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="6fac7-173">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="6fac7-174">보호 된 Vm의 복구 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-174">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="6fac7-175">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6fac7-175">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6fac7-176">ASR 복제 보호 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-176">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="6fac7-177">-보존 볼륨</span><span class="sxs-lookup"><span data-stu-id="6fac7-177">-RetentionVolume</span></span>
<span data-ttu-id="6fac7-178">사용할 마스터 대상 서버의 보존 볼륨입니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-178">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="6fac7-179">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="6fac7-179">-VmmToVmm</span></span>
<span data-ttu-id="6fac7-180">두 개의 VMM 관리 Hyper-v 사이트 간에 보호 되는 Hyper-v 가상 컴퓨터 장애 조치에 대 한 복제 방향을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-180">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="6fac7-181">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="6fac7-181">-VMwareToAzure</span></span>
<span data-ttu-id="6fac7-182">VMware에서 Azure로 복제 방향을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-182">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="6fac7-183">-확인</span><span class="sxs-lookup"><span data-stu-id="6fac7-183">-Confirm</span></span>
<span data-ttu-id="6fac7-184">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fac7-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fac7-185">-WhatIf</span></span>
<span data-ttu-id="6fac7-186">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-186">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fac7-187">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fac7-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fac7-188">CommonParameters</span></span>
<span data-ttu-id="6fac7-189">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fac7-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fac7-190">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6fac7-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fac7-191">입력</span><span class="sxs-lookup"><span data-stu-id="6fac7-191">INPUTS</span></span>

### <span data-ttu-id="6fac7-192">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="6fac7-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="6fac7-193">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="6fac7-193">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6fac7-194">출력</span><span class="sxs-lookup"><span data-stu-id="6fac7-194">OUTPUTS</span></span>

### <span data-ttu-id="6fac7-195">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="6fac7-195">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6fac7-196">상속자</span><span class="sxs-lookup"><span data-stu-id="6fac7-196">NOTES</span></span>

## <span data-ttu-id="6fac7-197">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fac7-197">RELATED LINKS</span></span>
