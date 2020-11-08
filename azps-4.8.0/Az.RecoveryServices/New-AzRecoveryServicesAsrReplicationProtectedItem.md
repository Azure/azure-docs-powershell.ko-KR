---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bde840903c53dae9ba47b9eb30634ce90f80ee9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214264"
---
# <span data-ttu-id="e9d17-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e9d17-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="e9d17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9d17-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d17-103">복제 보호 항목을 만들어 ASR 보호 가능한 항목에 대 한 복제를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="e9d17-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9d17-104">SYNTAX</span></span>

### <span data-ttu-id="e9d17-105">EnterpriseToEnterprise (기본값)</span><span class="sxs-lookup"><span data-stu-id="e9d17-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d17-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="e9d17-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d17-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="e9d17-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d17-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="e9d17-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d17-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="e9d17-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d17-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="e9d17-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d17-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="e9d17-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9d17-112">설명은</span><span class="sxs-lookup"><span data-stu-id="e9d17-112">DESCRIPTION</span></span>
<span data-ttu-id="e9d17-113">**AzRecoveryServicesAsrReplicationProtectedItem** cmdlet은 새 복제 보호 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="e9d17-114">이 cmdlet을 사용 하 여 ASR 보호 가능한 항목에 대 한 복제를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="e9d17-115">예제의</span><span class="sxs-lookup"><span data-stu-id="e9d17-115">EXAMPLES</span></span>

### <span data-ttu-id="e9d17-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9d17-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="e9d17-117">지정 된 ASR 보호 가능한 항목에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="e9d17-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="e9d17-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="e9d17-119">지정 된 ASR 보호 가능한 항목에 대 한 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다 (vmWare에서 Azure 시나리오).</span><span class="sxs-lookup"><span data-stu-id="e9d17-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="e9d17-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="e9d17-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="e9d17-121">지정 된 ASR 보호 가능한 항목에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업 (Azure to Azure 시나리오)을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="e9d17-122">예제 4</span><span class="sxs-lookup"><span data-stu-id="e9d17-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="e9d17-123">지정 된 VmId에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다 (Azure to Azure 시나리오).</span><span class="sxs-lookup"><span data-stu-id="e9d17-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="e9d17-124">예제 5</span><span class="sxs-lookup"><span data-stu-id="e9d17-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="e9d17-125">선택적 디스크를 포함 하 여 지정 된 ASR 보호 항목 만들기 작업을 시작 하 고 선택한 디스크를 사용 하 여 작업을 추적 하는 데 사용 되는 ASR 작업 (vmWare to Azure 시나리오)을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="e9d17-126">예제 6</span><span class="sxs-lookup"><span data-stu-id="e9d17-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="e9d17-127">예제 7</span><span class="sxs-lookup"><span data-stu-id="e9d17-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="e9d17-128">지정 된 VmId에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다 (Azure to Azure 시나리오). 암호화를 위해 cmdlet에서 전달 되는 장애 조치 VM 세부 정보가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="e9d17-129">예제 8</span><span class="sxs-lookup"><span data-stu-id="e9d17-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="e9d17-130">근접 배치 그룹 내의 가상 컴퓨터에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업 (Azure to Azure 시나리오)을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="e9d17-131">변수</span><span class="sxs-lookup"><span data-stu-id="e9d17-131">PARAMETERS</span></span>

### <span data-ttu-id="e9d17-132">-계정</span><span class="sxs-lookup"><span data-stu-id="e9d17-132">-Account</span></span>
<span data-ttu-id="e9d17-133">필요한 경우 모바일 서비스를 강제 설치 하는 데 사용할 실행 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="e9d17-134">ASR 패브릭의 실행 계정 목록에서 1 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="e9d17-135">-AzureToAzure</span></span>
<span data-ttu-id="e9d17-136">Switch 매개 변수 azure에서 azure로의 복제 된 항목 만들기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9d17-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="e9d17-138">Azure to Azure 재해 복구 시나리오에 사용 되는 Vm에 대 한 디스크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="e9d17-139">-AzureVmId</span></span>
<span data-ttu-id="e9d17-140">복구 영역에서 재해 복구 보호를 위한 Azure VM id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d17-141">-DefaultProfile</span></span>
<span data-ttu-id="e9d17-142">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e9d17-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="e9d17-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="e9d17-144">장애 조치 후 복구 VM으로 사용할 버전 (Azure 디스크 암호화)이 포함 된 디스크 암호화 비밀 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-145">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="e9d17-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e9d17-146">관리 되는 디스크의 암호화에 사용할 디스크 암호화 집합의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="e9d17-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="e9d17-148">장애 조치 후 복구 VM으로 사용할 디스크 암호화 비밀 자격 증명 모음 ID (Azure 디스크 암호화)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="e9d17-149">-DiskType</span></span>
<span data-ttu-id="e9d17-150">복구 VM 관리 디스크 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-150">Specifies the Recovery VM managed disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="e9d17-151">-HyperVToAzure</span></span>
<span data-ttu-id="e9d17-152">복제 된 항목을 Azure에 복제 되는 Hyper-v 가상 컴퓨터를 지정 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="e9d17-153">-IncludeDiskId</span></span>
<span data-ttu-id="e9d17-154">복제에 대해 포함할 디스크 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-154">The list of disks to include for replication.</span></span> <span data-ttu-id="e9d17-155">기본적으로 모든 디스크가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-155">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="e9d17-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="e9d17-157">VMWare 디스크 id에 대 한 디스크 구성 입력을 지정 하 여 보호 가능한 특정 항목에서 보호할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e9d17-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="e9d17-159">장애 조치 후 복구 VM으로 사용할 버전 (Azure 디스크 암호화)이 포함 된 디스크 암호화 키 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="e9d17-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="e9d17-161">장애 조치 후 복구 VM으로 사용할 디스크 암호화 키 키 보관소 ID (Azure 디스크 암호화)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e9d17-162">-LogStorageAccountId</span></span>
<span data-ttu-id="e9d17-163">복제 로그를 저장 하는 데 사용할 로그 또는 캐시 저장소 계정 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-164">-이름</span><span class="sxs-lookup"><span data-stu-id="e9d17-164">-Name</span></span>
<span data-ttu-id="e9d17-165">ASR 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="e9d17-166">이름은 자격 증명 모음 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="e9d17-167">-OS</span><span class="sxs-lookup"><span data-stu-id="e9d17-167">-OS</span></span>
<span data-ttu-id="e9d17-168">운영 체제 패밀리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-168">Specifies the operating system family.</span></span>
<span data-ttu-id="e9d17-169">이 매개 변수에 허용 되는 값은 Windows 또는 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="e9d17-170">-OSDiskName</span></span>
<span data-ttu-id="e9d17-171">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-171">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="e9d17-172">-ProcessServer</span></span>
<span data-ttu-id="e9d17-173">이 컴퓨터를 복제 하는 데 사용할 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="e9d17-174">구성 서버에 해당 하는 ASR 패브릭에 있는 프로세스 서버 목록을 사용 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e9d17-175">-ProtectableItem</span></span>
<span data-ttu-id="e9d17-176">복제를 사용할 수 있는 ASR 보호 가능한 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e9d17-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="e9d17-178">복제에 사용할 복제 정책에 해당 하는 ASR 보호 컨테이너 매핑 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="e9d17-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="e9d17-180">장애 조치 시 컴퓨터를 복구할 AvailabilitySet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="e9d17-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="e9d17-182">장애 조치 후 복구 VM의 가용성 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-182">Specifies the recovery VM availability zone after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="e9d17-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="e9d17-184">장애 조치 시 컴퓨터를 복구할 Azure 가상 네트워크의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e9d17-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e9d17-186">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="e9d17-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="e9d17-188">장애 조치 시 가상 머신이 실패 한 경우 복구 Azure 가상 네트워크 내의 서브넷이 연결 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e9d17-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="e9d17-190">복구 azure VM에 대 한 부팅 진단의 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="e9d17-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="e9d17-192">이 가상 컴퓨터를 장애 조치 (failover) 할 복구 클라우드 서비스의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="e9d17-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="e9d17-194">대상 복구 영역의 장애 조치 (failover) Vm에서 사용할 근접 배치 그룹 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e9d17-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="e9d17-196">장애 조치 시 가상 컴퓨터가 생성 될 리소스 그룹의 ARM 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="e9d17-197">-RecoveryVmName</span></span>
<span data-ttu-id="e9d17-198">장애 조치 이후 만든 복구 Vm의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-198">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d17-199">-ReplicationGroupName</span></span>
<span data-ttu-id="e9d17-200">여러 VM에서 일관 된 복구 지점을 만드는 데 사용할 복제 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="e9d17-201">기본적으로 각 복제 보호 항목은 자체 그룹에서 만들어지고, 다중 VM 일관성 복구 지점은 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="e9d17-202">모든 컴퓨터를 동일한 복제 그룹으로 보호 하 여 여러 컴퓨터에 걸친 VM의 일관 된 복구 지점을 만들어야 하는 경우에만이 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-203">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="e9d17-203">-VmmToVmm</span></span>
<span data-ttu-id="e9d17-204">복제 된 항목을 지정 하는 스위치 매개 변수는 VMM 관리 Hyper-v 사이트 간에 복제 되는 Hyper-v 가상 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-204">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="e9d17-205">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="e9d17-205">-VMwareToAzure</span></span>
<span data-ttu-id="e9d17-206">복제 된 항목을 지정 하는 스위치 매개 변수는 Azure에 복제 되는 VMware 가상 머신 또는 물리적 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-206">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-207">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e9d17-207">-WaitForCompletion</span></span>
<span data-ttu-id="e9d17-208">반환 하기 전에 cmdlet에서 작업이 완료 될 때까지 기다리도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-208">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d17-209">-확인</span><span class="sxs-lookup"><span data-stu-id="e9d17-209">-Confirm</span></span>
<span data-ttu-id="e9d17-210">작업을 시작 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-210">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="e9d17-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9d17-211">-WhatIf</span></span>
<span data-ttu-id="e9d17-212">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9d17-213">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9d17-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d17-214">CommonParameters</span></span>
<span data-ttu-id="e9d17-215">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d17-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d17-216">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e9d17-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d17-217">입력</span><span class="sxs-lookup"><span data-stu-id="e9d17-217">INPUTS</span></span>

### <span data-ttu-id="e9d17-218">SiteRecovery. ASRProtectableItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="e9d17-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="e9d17-219">출력</span><span class="sxs-lookup"><span data-stu-id="e9d17-219">OUTPUTS</span></span>

### <span data-ttu-id="e9d17-220">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="e9d17-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e9d17-221">상속자</span><span class="sxs-lookup"><span data-stu-id="e9d17-221">NOTES</span></span>

## <span data-ttu-id="e9d17-222">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9d17-222">RELATED LINKS</span></span>

[<span data-ttu-id="e9d17-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e9d17-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e9d17-224">제거-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e9d17-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e9d17-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e9d17-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
