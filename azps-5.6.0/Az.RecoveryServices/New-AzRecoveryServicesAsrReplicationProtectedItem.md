---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: d2178e4eaf417ff9db0b7c5b83aa22cc7e131f1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953408"
---
# <span data-ttu-id="6a955-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6a955-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="6a955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a955-102">SYNOPSIS</span></span>
<span data-ttu-id="6a955-103">복제 보호 항목을 만들어 ASR 보호 가능한 항목에 대해 복제를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="6a955-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a955-104">SYNTAX</span></span>

### <span data-ttu-id="6a955-105">EnterpriseToEnterprise(기본값)</span><span class="sxs-lookup"><span data-stu-id="6a955-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a955-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="6a955-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] -DiskType <String>
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a955-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="6a955-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a955-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6a955-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a955-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="6a955-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-UseManagedDisk <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a955-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6a955-110">AzureToAzure</span></span>
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

### <span data-ttu-id="6a955-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="6a955-111">AzureToAzureWithoutDiskDetails</span></span>
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

## <span data-ttu-id="6a955-112">설명</span><span class="sxs-lookup"><span data-stu-id="6a955-112">DESCRIPTION</span></span>
<span data-ttu-id="6a955-113">**New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet은 새 복제 보호 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="6a955-114">이 cmdlet을 사용하여 ASR 보호 가능한 항목에 대해 복제를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="6a955-115">예제</span><span class="sxs-lookup"><span data-stu-id="6a955-115">EXAMPLES</span></span>

### <span data-ttu-id="6a955-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="6a955-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="6a955-117">지정된 ASR 보호 가능한 항목에 대한 복제 보호 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="6a955-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="6a955-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="6a955-119">지정된 ASR 보호 가능한 항목에 대한 복제 보호 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업(vmWare에서 Azure 시나리오)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="6a955-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="6a955-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="6a955-121">지정된 ASR 보호 가능한 항목에 대한 복제 보호 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업(Azure에서 Azure 시나리오)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="6a955-122">예제 4</span><span class="sxs-lookup"><span data-stu-id="6a955-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="6a955-123">지정된 VmId에 대한 복제 보호된 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업(Azure에서 Azure 시나리오)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="6a955-124">예제 5</span><span class="sxs-lookup"><span data-stu-id="6a955-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="6a955-125">선택적 디스크를 포함하여 지정된 ASR 보호 항목에 대한 복제 보호 항목 만들기 작업을 시작하고 선택한 디스크를 사용하여 작업을 추적하는 데 사용되는 ASR 작업(vmWare에서 Azure 시나리오)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="6a955-126">예제 6</span><span class="sxs-lookup"><span data-stu-id="6a955-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="6a955-127">예제 7</span><span class="sxs-lookup"><span data-stu-id="6a955-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="6a955-128">지정된 VmId에 대한 복제 보호된 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업(Azure에서 Azure 시나리오)을 반환합니다. 암호화를 위해 cmdlet에 전달된 장애 조치(failover) VM 세부 정보가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="6a955-129">예제 8</span><span class="sxs-lookup"><span data-stu-id="6a955-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="6a955-130">근접 배치 그룹 내에서 Virtual Machine에 대한 복제 보호 항목 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업(Azure에서 Azure 시나리오)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="6a955-131">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6a955-131">PARAMETERS</span></span>

### <span data-ttu-id="6a955-132">-Account</span><span class="sxs-lookup"><span data-stu-id="6a955-132">-Account</span></span>
<span data-ttu-id="6a955-133">필요한 경우 모바일 서비스 설치를 푸시하는 데 사용할 계정으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="6a955-134">ASR 패브릭의 계정으로 실행 목록에서 하나만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="6a955-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6a955-135">-AzureToAzure</span></span>
<span data-ttu-id="6a955-136">스위치 매개 변수는 Azure에서 복제된 항목을 Azure 시나리오로 만드는 것이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

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

### <span data-ttu-id="6a955-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a955-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="6a955-138">Azure에서 Azure로의 Vm을 사용하는 디스크 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="6a955-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="6a955-139">-AzureVmId</span></span>
<span data-ttu-id="6a955-140">복구 지역에서 재해 복구 보호를 위해 Azure VM ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

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

### <span data-ttu-id="6a955-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a955-141">-DefaultProfile</span></span>
<span data-ttu-id="6a955-142">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6a955-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="6a955-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="6a955-144">장애 조치(failover) 후 복구 VM으로 사용할 버전(Azure 디스크 암호화)을 사용하여 디스크 암호화 비밀 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6a955-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="6a955-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="6a955-146">관리 디스크의 암호화에 사용할 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="6a955-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="6a955-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="6a955-148">장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 비밀 자격 증명 모음 ID(Azure Disk Encryption)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6a955-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="6a955-149">-DiskType</span></span>
<span data-ttu-id="6a955-150">Recovery VM 관리 디스크 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-150">Specifies the Recovery VM managed disk type.</span></span>

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

### <span data-ttu-id="6a955-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="6a955-151">-HyperVToAzure</span></span>
<span data-ttu-id="6a955-152">복제된 항목을 지정하는 스위치 매개 변수는 Azure에 Hyper-V 가상 머신입니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="6a955-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="6a955-153">-IncludeDiskId</span></span>
<span data-ttu-id="6a955-154">복제에 포함할 디스크 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-154">The list of disks to include for replication.</span></span> <span data-ttu-id="6a955-155">기본적으로 모든 디스크가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-155">By default all disks are included.</span></span>

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

### <span data-ttu-id="6a955-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="6a955-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="6a955-157">지정된 보호 가능한 항목으로부터 보호하기 위해 vMWare 디스크 ID에 대한 디스크 구성 입력을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

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

### <span data-ttu-id="6a955-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="6a955-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="6a955-159">장애 조치(failover) 후 복구 VM으로 사용할 버전(Azure 디스크 암호화)을 사용하여 디스크 암호화 키 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6a955-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="6a955-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="6a955-161">장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 키-자격 증명 모음 ID(Azure 디스크 암호화)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6a955-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6a955-162">-LogStorageAccountId</span></span>
<span data-ttu-id="6a955-163">복제 로그를 저장하는 데 사용할 로그 또는 캐시 저장소 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="6a955-164">-Name</span><span class="sxs-lookup"><span data-stu-id="6a955-164">-Name</span></span>
<span data-ttu-id="6a955-165">ASR 복제 보호 항목에 대한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="6a955-166">이름은 자격 증명 모음 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="6a955-167">-OS</span><span class="sxs-lookup"><span data-stu-id="6a955-167">-OS</span></span>
<span data-ttu-id="6a955-168">운영 체제 패밀리를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-168">Specifies the operating system family.</span></span>
<span data-ttu-id="6a955-169">이 매개 변수에 대해 허용되는 값은 Windows 또는 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="6a955-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="6a955-170">-OSDiskName</span></span>
<span data-ttu-id="6a955-171">운영 체제 디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-171">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="6a955-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="6a955-172">-ProcessServer</span></span>
<span data-ttu-id="6a955-173">이 머신을 복제하는 데 사용할 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="6a955-174">구성 서버에 해당하는 ASR 패브릭의 프로세스 서버 목록을 사용하여 하나를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

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

### <span data-ttu-id="6a955-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6a955-175">-ProtectableItem</span></span>
<span data-ttu-id="6a955-176">복제를 사용하도록 설정하는 ASR 보호 가능한 항목 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

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

### <span data-ttu-id="6a955-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6a955-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="6a955-178">복제에 사용할 복제 정책에 해당하는 ASR 보호 컨테이너 매핑 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="6a955-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="6a955-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="6a955-180">장애 조치(failover)가 발생하면 머신을 복구하는 AvailabilitySet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="6a955-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="6a955-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="6a955-182">장애 조치(failover) 후 복구 VM 가용성 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-182">Specifies the recovery VM availability zone after failover.</span></span>


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

### <span data-ttu-id="6a955-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="6a955-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="6a955-184">장애 조치(failover)가 발생하면 머신을 복구하는 Azure 가상 네트워크의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="6a955-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6a955-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="6a955-186">복제할 Azure Storage 계정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="6a955-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="6a955-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="6a955-188">장애 조치(failover)의 경우 장애 조치(failover)를 통해 가상 머신을 연결해야 하는 복구 Azure 가상 네트워크 내의 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

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

### <span data-ttu-id="6a955-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6a955-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="6a955-190">복구 azure VM에 대한 부팅 진단에 대한 저장소 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="6a955-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="6a955-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="6a955-192">이 가상 머신에 장애 조치(failover)를 위해 복구 클라우드 서비스의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="6a955-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="6a955-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="6a955-194">대상 복구 지역의 장애 조치 Vm에서 사용할 근접 배치 그룹 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

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

### <span data-ttu-id="6a955-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="6a955-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="6a955-196">장애 조치(failover)ARM 가상 머신을 만들 리소스 그룹의 ARM 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

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

### <span data-ttu-id="6a955-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="6a955-197">-RecoveryVmName</span></span>
<span data-ttu-id="6a955-198">장애 조치(failover) 후에 만든 복구 Vm의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-198">Name of the recovery Vm created after failover.</span></span>

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

### <span data-ttu-id="6a955-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="6a955-199">-ReplicationGroupName</span></span>
<span data-ttu-id="6a955-200">다중 VM 일관성 복구 지점을 만드는 데 사용할 복제 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="6a955-201">기본적으로 각 복제 보호 항목은 자체 그룹에서 생성되고 다중 VM 일관성 복구 지점은 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="6a955-202">모든 컴퓨터를 동일한 복제 그룹으로 보호하여 컴퓨터 그룹 전체에서 다중 VM 일관된 복구 지점을 만들어야 하는 경우만 이 옵션을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

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

### <span data-ttu-id="6a955-203">-ManagedDisk 사용</span><span class="sxs-lookup"><span data-stu-id="6a955-203">-UseManagedDisk</span></span>
<span data-ttu-id="6a955-204">장애 조치(failover)에서 만든 Azure 가상 머신이 관리 디스크를 사용해야 하는지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-204">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span> <span data-ttu-id="6a955-205">True 또는 False를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-205">It Accepts either True or False.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a955-206">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="6a955-206">-VmmToVmm</span></span>
<span data-ttu-id="6a955-207">복제된 항목을 지정하는 스위치 매개 변수는 VMM 관리되는 Hyper-V 사이트 간에 복제되는 Hyper-V 가상 머신입니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-207">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="6a955-208">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="6a955-208">-VMwareToAzure</span></span>
<span data-ttu-id="6a955-209">복제된 항목을 지정하는 스위치 매개 변수는 Azure에 복제될 VMware 가상 머신 또는 물리적 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-209">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="6a955-210">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="6a955-210">-WaitForCompletion</span></span>
<span data-ttu-id="6a955-211">반환하기 전에 cmdlet이 작업이 완료될 때까지 기다려야 한다고 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-211">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="6a955-212">-확인</span><span class="sxs-lookup"><span data-stu-id="6a955-212">-Confirm</span></span>
<span data-ttu-id="6a955-213">작업을 시작하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-213">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="6a955-214">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a955-214">-WhatIf</span></span>
<span data-ttu-id="6a955-215">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-215">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a955-216">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-216">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a955-217">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a955-217">CommonParameters</span></span>
<span data-ttu-id="6a955-218">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a955-218">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a955-219">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a955-219">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a955-220">입력</span><span class="sxs-lookup"><span data-stu-id="6a955-220">INPUTS</span></span>

### <span data-ttu-id="6a955-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6a955-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="6a955-222">출력</span><span class="sxs-lookup"><span data-stu-id="6a955-222">OUTPUTS</span></span>

### <span data-ttu-id="6a955-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6a955-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6a955-224">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a955-224">NOTES</span></span>

## <span data-ttu-id="6a955-225">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a955-225">RELATED LINKS</span></span>

[<span data-ttu-id="6a955-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6a955-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6a955-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6a955-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6a955-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6a955-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
