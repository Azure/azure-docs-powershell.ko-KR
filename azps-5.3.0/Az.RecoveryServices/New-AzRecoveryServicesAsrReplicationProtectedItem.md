---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bde840903c53dae9ba47b9eb30634ce90f80ee9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492448"
---
# <span data-ttu-id="04bac-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="04bac-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="04bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04bac-102">SYNOPSIS</span></span>
<span data-ttu-id="04bac-103">복제 보호된 항목을 만들어 ASR 보호 가능한 항목에 대한 복제를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="04bac-104">구문</span><span class="sxs-lookup"><span data-stu-id="04bac-104">SYNTAX</span></span>

### <span data-ttu-id="04bac-105">EnterpriseToEnterprise(기본값)</span><span class="sxs-lookup"><span data-stu-id="04bac-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04bac-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="04bac-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04bac-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="04bac-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04bac-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="04bac-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04bac-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="04bac-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04bac-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="04bac-110">AzureToAzure</span></span>
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

### <span data-ttu-id="04bac-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="04bac-111">AzureToAzureWithoutDiskDetails</span></span>
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

## <span data-ttu-id="04bac-112">설명</span><span class="sxs-lookup"><span data-stu-id="04bac-112">DESCRIPTION</span></span>
<span data-ttu-id="04bac-113">**New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet은 새 복제 보호 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="04bac-114">이 cmdlet을 사용하여 ASR 보호 가능한 항목에 대해 복제를 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="04bac-115">예제</span><span class="sxs-lookup"><span data-stu-id="04bac-115">EXAMPLES</span></span>

### <span data-ttu-id="04bac-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="04bac-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="04bac-117">지정된 ASR 보호 가능한 항목에 대한 복제 보호된 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="04bac-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="04bac-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="04bac-119">지정된 ASR 보호 가능한 항목에 대한 복제 보호된 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업(vmWare에서 Azure로 시나리오)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="04bac-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="04bac-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="04bac-121">지정된 ASR 보호 가능한 항목에 대한 복제 보호된 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업(Azure에서 Azure로 시나리오)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="04bac-122">예제 4</span><span class="sxs-lookup"><span data-stu-id="04bac-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="04bac-123">지정된 VmId에 대한 복제 보호된 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업(Azure에서 Azure로 시나리오)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="04bac-124">예제 5</span><span class="sxs-lookup"><span data-stu-id="04bac-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="04bac-125">선택적 디스크를 포함하여 지정된 ASR 보호 가능한 항목에 대한 복제 보호된 항목 만들기 작업을 시작하고 선택한 디스크를 사용하여 작업을 추적하는 데 사용되는 ASR 작업(vmWare에서 Azure로 시나리오)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="04bac-126">예제 6</span><span class="sxs-lookup"><span data-stu-id="04bac-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="04bac-127">예제 7</span><span class="sxs-lookup"><span data-stu-id="04bac-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="04bac-128">지정된 VmId에 대한 복제 보호된 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업(Azure에서 Azure로 시나리오)을 반환합니다. 암호화를 위해 cmdlet에 전달된 장애 조치(failover) VM 세부 정보가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="04bac-129">예제 8</span><span class="sxs-lookup"><span data-stu-id="04bac-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="04bac-130">근접 배치 그룹 내에서 Virtual Machine에 대한 복제 보호된 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업(Azure에서 Azure로 시나리오)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="04bac-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04bac-131">PARAMETERS</span></span>

### <span data-ttu-id="04bac-132">-Account</span><span class="sxs-lookup"><span data-stu-id="04bac-132">-Account</span></span>
<span data-ttu-id="04bac-133">필요한 경우 모바일 서비스를 푸시 설치하는 데 사용할 실행 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="04bac-134">ASR 패브릭의 실행 계정 목록에서 하나만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="04bac-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="04bac-135">-AzureToAzure</span></span>
<span data-ttu-id="04bac-136">스위치 매개 변수는 Azure에서 Azure 시나리오에 복제된 항목을 만드는 것이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

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

### <span data-ttu-id="04bac-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="04bac-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="04bac-138">Azure에서 Azure로 재해 복구 시나리오에 사용되는 VM에 대한 디스크 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="04bac-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="04bac-139">-AzureVmId</span></span>
<span data-ttu-id="04bac-140">복구 지역의 재해 복구 보호를 위한 Azure VM ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

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

### <span data-ttu-id="04bac-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04bac-141">-DefaultProfile</span></span>
<span data-ttu-id="04bac-142">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="04bac-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="04bac-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="04bac-144">장애 조치(failover) 후 복구 VM으로 사용할 버전(Azure 디스크 암호화)을 사용하여 디스크 암호화 비밀 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="04bac-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="04bac-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="04bac-146">관리 디스크의 암호화에 사용할 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="04bac-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="04bac-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="04bac-148">장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 비밀 자격 증명 모음 ID(Azure 디스크 암호화)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="04bac-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="04bac-149">-DiskType</span></span>
<span data-ttu-id="04bac-150">복구 VM 관리 디스크 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-150">Specifies the Recovery VM managed disk type.</span></span>

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

### <span data-ttu-id="04bac-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="04bac-151">-HyperVToAzure</span></span>
<span data-ttu-id="04bac-152">복제된 항목을 지정하는 스위치 매개 변수는 Azure에 복제되는 Hyper-V 가상 머신입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="04bac-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="04bac-153">-IncludeDiskId</span></span>
<span data-ttu-id="04bac-154">복제에 포함할 디스크 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-154">The list of disks to include for replication.</span></span> <span data-ttu-id="04bac-155">기본적으로 모든 디스크가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-155">By default all disks are included.</span></span>

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

### <span data-ttu-id="04bac-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="04bac-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="04bac-157">지정된 보호 가능한 항목으로부터 보호하기 위해 vMWare 디스크 ID에 대한 디스크 구성 입력을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

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

### <span data-ttu-id="04bac-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="04bac-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="04bac-159">장애 조치(failover) 후 복구 VM으로 사용할 버전(Azure 디스크 암호화)을 사용하여 디스크 암호화 키 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="04bac-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="04bac-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="04bac-161">장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 키-자격 증명 모음 ID(Azure 디스크 암호화)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="04bac-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="04bac-162">-LogStorageAccountId</span></span>
<span data-ttu-id="04bac-163">복제 로그를 저장하는 데 사용할 로그 또는 캐시 저장소 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="04bac-164">-Name</span><span class="sxs-lookup"><span data-stu-id="04bac-164">-Name</span></span>
<span data-ttu-id="04bac-165">ASR 복제 보호 항목의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="04bac-166">이름은 자격 증명 모음 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="04bac-167">-OS</span><span class="sxs-lookup"><span data-stu-id="04bac-167">-OS</span></span>
<span data-ttu-id="04bac-168">운영 체제 패밀리를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-168">Specifies the operating system family.</span></span>
<span data-ttu-id="04bac-169">이 매개 변수에 허용되는 값은 Windows 또는 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="04bac-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="04bac-170">-OSDiskName</span></span>
<span data-ttu-id="04bac-171">운영 체제 디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-171">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="04bac-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="04bac-172">-ProcessServer</span></span>
<span data-ttu-id="04bac-173">이 머신을 복제하는 데 사용할 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="04bac-174">구성 서버에 해당하는 ASR 패브릭의 프로세스 서버 목록을 사용하여 하나를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

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

### <span data-ttu-id="04bac-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="04bac-175">-ProtectableItem</span></span>
<span data-ttu-id="04bac-176">복제를 사용하도록 설정하는 ASR 보호 가능한 항목 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

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

### <span data-ttu-id="04bac-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="04bac-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="04bac-178">복제에 사용할 복제 정책에 해당하는 ASR 보호 컨테이너 매핑 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="04bac-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="04bac-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="04bac-180">장애 조치(failover) 시 머신을 복구할 AvailabilitySet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="04bac-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="04bac-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="04bac-182">장애 조치(failover) 후 복구 VM 가용성 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-182">Specifies the recovery VM availability zone after failover.</span></span>


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

### <span data-ttu-id="04bac-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="04bac-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="04bac-184">장애 조치(failover) 시 머신을 복구할 Azure 가상 네트워크의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="04bac-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="04bac-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="04bac-186">복제할 Azure 저장소 계정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="04bac-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="04bac-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="04bac-188">장애 조치(failover) 시 장애 조치된 가상 머신을 연결해야 하는 복구 Azure 가상 네트워크 내의 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

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

### <span data-ttu-id="04bac-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="04bac-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="04bac-190">복구 Azure VM에 대한 부팅 진단을 위한 저장소 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="04bac-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="04bac-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="04bac-192">이 가상 머신을 장애 조치(failover)할 복구 클라우드 서비스의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="04bac-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="04bac-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="04bac-194">대상 복구 지역의 장애 조치(failover) VM에서 사용할 근접 배치 그룹 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

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

### <span data-ttu-id="04bac-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="04bac-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="04bac-196">장애 조치(failover) ARM 가상 머신을 만들 리소스 그룹의 리소스 그룹 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

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

### <span data-ttu-id="04bac-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="04bac-197">-RecoveryVmName</span></span>
<span data-ttu-id="04bac-198">장애 조치(failover) 후 만든 복구 VM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-198">Name of the recovery Vm created after failover.</span></span>

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

### <span data-ttu-id="04bac-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="04bac-199">-ReplicationGroupName</span></span>
<span data-ttu-id="04bac-200">다중 VM 일치 복구 지점을 만드는 데 사용할 복제 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="04bac-201">기본적으로 각 복제 보호된 항목은 자체 그룹에서 만들어지며 다중 VM 일치 복구 지점은 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="04bac-202">모든 컴퓨터를 동일한 복제 그룹에 보호하여 컴퓨터 그룹에서 다중 VM 일관성 복구 지점을 만들어야 하는 경우 이 옵션을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

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

### <span data-ttu-id="04bac-203">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="04bac-203">-VmmToVmm</span></span>
<span data-ttu-id="04bac-204">복제된 항목을 지정하는 스위치 매개 변수는 VMM 관리 Hyper-V 사이트 간에 복제되는 Hyper-V 가상 머신입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-204">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="04bac-205">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="04bac-205">-VMwareToAzure</span></span>
<span data-ttu-id="04bac-206">복제된 항목을 지정하는 스위치 매개 변수는 Azure에 복제할 VMware 가상 머신 또는 물리적 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-206">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="04bac-207">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="04bac-207">-WaitForCompletion</span></span>
<span data-ttu-id="04bac-208">cmdlet이 반환하기 전에 작업이 완료될 때까지 기다려야 한다고 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-208">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="04bac-209">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04bac-209">-Confirm</span></span>
<span data-ttu-id="04bac-210">작업을 시작하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-210">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="04bac-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04bac-211">-WhatIf</span></span>
<span data-ttu-id="04bac-212">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="04bac-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04bac-213">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04bac-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04bac-214">CommonParameters</span></span>
<span data-ttu-id="04bac-215">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04bac-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04bac-216">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04bac-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04bac-217">입력</span><span class="sxs-lookup"><span data-stu-id="04bac-217">INPUTS</span></span>

### <span data-ttu-id="04bac-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="04bac-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="04bac-219">출력</span><span class="sxs-lookup"><span data-stu-id="04bac-219">OUTPUTS</span></span>

### <span data-ttu-id="04bac-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="04bac-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="04bac-221">참고 사항</span><span class="sxs-lookup"><span data-stu-id="04bac-221">NOTES</span></span>

## <span data-ttu-id="04bac-222">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04bac-222">RELATED LINKS</span></span>

[<span data-ttu-id="04bac-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="04bac-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="04bac-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="04bac-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="04bac-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="04bac-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
