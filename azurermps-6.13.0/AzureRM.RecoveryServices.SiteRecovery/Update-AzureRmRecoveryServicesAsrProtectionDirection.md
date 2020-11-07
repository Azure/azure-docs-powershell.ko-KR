---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 48647fcc0382dd23f012d64aa70af364355c60e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702095"
---
# <span data-ttu-id="64f59-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="64f59-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="64f59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64f59-102">SYNOPSIS</span></span>
<span data-ttu-id="64f59-103">지정 된 복제 보호 항목 또는 복구 계획에 대 한 복제 방향을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="64f59-104">복제 된 항목 또는 복구 계획을 통해 장애를 다시 방지 하거나 역 복제 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64f59-105">구문과</span><span class="sxs-lookup"><span data-stu-id="64f59-105">SYNTAX</span></span>

### <span data-ttu-id="64f59-106">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="64f59-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64f59-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="64f59-107">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64f59-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="64f59-108">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64f59-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="64f59-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64f59-110">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="64f59-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64f59-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="64f59-111">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64f59-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="64f59-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64f59-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="64f59-113">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64f59-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="64f59-114">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64f59-115">설명은</span><span class="sxs-lookup"><span data-stu-id="64f59-115">DESCRIPTION</span></span>
<span data-ttu-id="64f59-116">**AzureRmRecoveryServicesAsrProtectionDirection** cmdlet은 커밋 장애 조치 작업이 완료 된 후 지정 된 Azure Site Recovery 개체의 복제 방향을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-116">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="64f59-117">예제의</span><span class="sxs-lookup"><span data-stu-id="64f59-117">EXAMPLES</span></span>

### <span data-ttu-id="64f59-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="64f59-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="64f59-119">지정 된 복구 계획에 대 한 방향 업데이트 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="64f59-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="64f59-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="64f59-121">보호 컨테이너 매핑과 동일한 지역에서 캐시 저장소를 사용 하 여 대상 azure 지역에서 지정 된 복제 보호 항목에 대 한 방향 업데이트 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="64f59-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="64f59-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="64f59-123">보호 컨테이너 매핑과 제공 된 디스크 복제 구성에 정의 된 대상 azure 지역에서 지정 된 복제 보호 항목에 대 한 방향 업데이트 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="64f59-124">변수</span><span class="sxs-lookup"><span data-stu-id="64f59-124">PARAMETERS</span></span>

### <span data-ttu-id="64f59-125">-계정</span><span class="sxs-lookup"><span data-stu-id="64f59-125">-Account</span></span>
<span data-ttu-id="64f59-126">필요한 경우 모바일 서비스를 강제 설치 하는 데 사용할 실행 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="64f59-127">ASR 패브릭의 실행 계정 목록에서 1 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="64f59-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="64f59-128">-AzureToAzure</span></span>
<span data-ttu-id="64f59-129">두 Azure 지역 간에 복제 된 Azure 가상 컴퓨터에 대 한 복제 방향을 업데이트 하도록 지정 하는 Switch 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-129">Switch parameter specifying that the replication direction being updated for replicated Azure virtual machines between two Azure regions.</span></span>

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

### <span data-ttu-id="64f59-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="64f59-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="64f59-131">복제 될 가상 컴퓨터 디스크 목록과 디스크를 복제 하는 데 사용할 캐시 저장소 계정 및 복구 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-131">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

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

### <span data-ttu-id="64f59-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="64f59-132">-AzureToVMware</span></span>
<span data-ttu-id="64f59-133">Azure에서 Vmware로 복제 방향을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-133">Update replication direction from Azure to Vmware.</span></span>

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

### <span data-ttu-id="64f59-134">-데이터 스토어</span><span class="sxs-lookup"><span data-stu-id="64f59-134">-DataStore</span></span>
<span data-ttu-id="64f59-135">Vmdisk에 사용 되는 VMware 데이터 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-135">The VMware datastore to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="64f59-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f59-136">-DefaultProfile</span></span>
<span data-ttu-id="64f59-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="64f59-138">방향</span><span class="sxs-lookup"><span data-stu-id="64f59-138">-Direction</span></span>
<span data-ttu-id="64f59-139">업데이트 작업에 대해 장애 조치를 게시 하는 데 사용할 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-139">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="64f59-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64f59-141">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="64f59-141">PrimaryToRecovery</span></span>
- <span data-ttu-id="64f59-142">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="64f59-142">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="64f59-143">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="64f59-143">-HyperVToAzure</span></span>
<span data-ttu-id="64f59-144">장애 복구 후 Hyper-v 가상 컴퓨터를 다시 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-144">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="64f59-145">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="64f59-145">-LogStorageAccountId</span></span>
<span data-ttu-id="64f59-146">Vm의 복제 로그를 저장할 저장소 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-146">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="64f59-147">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="64f59-147">-MasterTarget</span></span>
<span data-ttu-id="64f59-148">마스터 대상 서버 세부 정보.</span><span class="sxs-lookup"><span data-stu-id="64f59-148">Master Target Server Details.</span></span>

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

### <span data-ttu-id="64f59-149">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="64f59-149">-ProcessServer</span></span>
<span data-ttu-id="64f59-150">복제에 사용할 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-150">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="64f59-151">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="64f59-151">-ProtectionContainerMapping</span></span>
<span data-ttu-id="64f59-152">복제에 사용할 보호 containerMapping.</span><span class="sxs-lookup"><span data-stu-id="64f59-152">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="64f59-153">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="64f59-153">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="64f59-154">장애 조치 시 가상 컴퓨터를 만들 가용성 집합</span><span class="sxs-lookup"><span data-stu-id="64f59-154">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="64f59-155">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="64f59-155">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="64f59-156">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-156">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="64f59-157">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="64f59-157">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="64f59-158">복구 azure VM에 대 한 부팅 진단의 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-158">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="64f59-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="64f59-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="64f59-160">이 가상 컴퓨터를 장애 조치 (failover) 할 복구 클라우드 서비스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="64f59-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64f59-161">-RecoveryPlan</span></span>
<span data-ttu-id="64f59-162">ASR 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-162">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="64f59-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="64f59-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="64f59-164">보호 된 Vm의 복구 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-164">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="64f59-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="64f59-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="64f59-166">ASR 복제 보호 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-166">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="64f59-167">-보존 볼륨</span><span class="sxs-lookup"><span data-stu-id="64f59-167">-RetentionVolume</span></span>
<span data-ttu-id="64f59-168">사용할 마스터 대상 서버의 보존 볼륨입니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-168">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="64f59-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="64f59-169">-VmmToVmm</span></span>
<span data-ttu-id="64f59-170">두 개의 VMM 관리 Hyper-v 사이트 간에 보호 되는 Hyper-v 가상 컴퓨터 장애 조치에 대 한 복제 방향을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-170">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="64f59-171">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="64f59-171">-VMwareToAzure</span></span>
<span data-ttu-id="64f59-172">VMware에서 Azure로 복제 방향을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-172">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="64f59-173">-확인</span><span class="sxs-lookup"><span data-stu-id="64f59-173">-Confirm</span></span>
<span data-ttu-id="64f59-174">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64f59-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64f59-175">-WhatIf</span></span>
<span data-ttu-id="64f59-176">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64f59-177">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64f59-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f59-178">CommonParameters</span></span>
<span data-ttu-id="64f59-179">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f59-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f59-180">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f59-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f59-181">입력</span><span class="sxs-lookup"><span data-stu-id="64f59-181">INPUTS</span></span>

### <span data-ttu-id="64f59-182">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="64f59-182">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="64f59-183">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="64f59-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="64f59-184">출력</span><span class="sxs-lookup"><span data-stu-id="64f59-184">OUTPUTS</span></span>

### <span data-ttu-id="64f59-185">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="64f59-185">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="64f59-186">상속자</span><span class="sxs-lookup"><span data-stu-id="64f59-186">NOTES</span></span>

## <span data-ttu-id="64f59-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64f59-187">RELATED LINKS</span></span>
