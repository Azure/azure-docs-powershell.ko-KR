---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 3d3cbb196a287e24837c0e7b0e61b16eaa06ce95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997509"
---
# <span data-ttu-id="bc185-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bc185-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="bc185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc185-102">SYNOPSIS</span></span>

<span data-ttu-id="bc185-103">백업 항목에 대한 데이터 및 구성을 지정된 복구 지점으로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="bc185-104">필요한 매개 변수는 백업 항목 유형에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="bc185-105">동일한 명령은 Azure Virtual machines, Azure Virtual Machines 내에서 실행되는 데이터베이스 및 Azure 파일 공유를 복원하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="bc185-106">구문</span><span class="sxs-lookup"><span data-stu-id="bc185-106">SYNTAX</span></span>

### <span data-ttu-id="bc185-107">AzureVMParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bc185-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc185-108">AzureVMManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc185-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc185-109">AzureVMRestoreManagedAsUn 관리</span><span class="sxs-lookup"><span data-stu-id="bc185-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc185-110">AzureVMUnManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc185-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc185-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc185-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc185-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc185-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc185-113">설명</span><span class="sxs-lookup"><span data-stu-id="bc185-113">DESCRIPTION</span></span>

<span data-ttu-id="bc185-114">**Restore-AzRecoveryServicesBackupItem** cmdlet은 Azure Backup 항목에 대한 데이터 및 구성을 지정된 복구 지점으로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="bc185-115">**Azure VM 백업의 경우**</span><span class="sxs-lookup"><span data-stu-id="bc185-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="bc185-116">이 명령을 사용하여 Azure 가상 머신을 백업하고 디스크를 복원(관리 및 비 관리 모두)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="bc185-117">복원 작업은 전체 가상 머신을 복원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="bc185-118">관리 디스크 VM인 경우 복원된 디스크가 유지되는 대상 리소스 그룹을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="bc185-119">대상 리소스 그룹을 지정하면 백업 정책에 지정된 리소스 그룹에 스냅숏이 있는 경우 복원 작업은 즉시 수행됩니다. 로컬 스냅숏에서 디스크를 만들어 대상 리소스 그룹에 보관합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="bc185-120">관리되지 않는 디스크로 복원하는 옵션도 있지만 Azure Recovery Services 자격 증명 모음에 있는 데이터를 활용하면 속도가 느려질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="bc185-121">복원된 디스크에서 VM을 만드는 데 사용할 수 있는 VM 및 배포 템플릿의 구성이 지정된 저장소 계정에 다운로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="bc185-122">관리되지 않는 디스크 VM인 경우 스냅숏이 디스크의 원래 저장소 계정 및/또는 복구 서비스 자격 증명 모음에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="bc185-123">사용자가 원본 저장소 계정을 사용하여 복원할 수 있는 옵션을 제공하는 경우 즉시 복원을 제공 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="bc185-124">그렇지 않으면 Azure Recovery 서비스 자격 증명 모음에서 데이터를 페치하고 디스크는 VM 및 배포 템플릿의 구성과 함께 지정된 저장소 계정에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc185-125">기본적으로 Azure VM 백업은 모든 디스크를 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="bc185-126">Enable-Backup 중에 제외 목록 또는 InclusionList 매개 변수를 사용하여 관련 디스크를 선택적으로 백업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="bc185-127">디스크를 선택적으로 복원하는 옵션은 디스크를 선택적으로 백업한 경우만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="bc185-128">자세한 내용은 가능한 다른 매개 변수 집합 및 매개 변수 텍스트를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bc185-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="bc185-129">-VaultId 매개 변수를 사용하는 경우 -VaultLocation 매개 변수도 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="bc185-130">**Azure 파일 공유 백업의 경우**</span><span class="sxs-lookup"><span data-stu-id="bc185-130">**For Azure File share backup**</span></span>

<span data-ttu-id="bc185-131">공유에서 전체 파일 공유 또는 특정/여러 파일/폴더를 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="bc185-132">원래 위치 또는 대체 위치로 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="bc185-133">**Azure 워크로드의 경우**</span><span class="sxs-lookup"><span data-stu-id="bc185-133">**For Azure Workloads**</span></span>

<span data-ttu-id="bc185-134">Azure VM 내에서 SQL DB를 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="bc185-135">예제</span><span class="sxs-lookup"><span data-stu-id="bc185-135">EXAMPLES</span></span>

### <span data-ttu-id="bc185-136">예제 1: 주어진 복구 지점에서 백업된 Managed Disk Azure VM의 디스크 복원</span><span class="sxs-lookup"><span data-stu-id="bc185-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="bc185-137">첫 번째 명령은 Recovery Services 자격 증명 모음을 얻게 하여 $vault 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="bc185-138">두 번째 명령은 "V2VM"의 AzureVM 형식의 Backup 항목을 $BackupItem 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="bc185-139">세 번째 명령은 7일 이전의 날짜를 얻은 다음, $StartDate 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="bc185-140">네 번째 명령은 현재 날짜를 얻은 다음, $EndDate 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="bc185-141">다섯 번째 명령은 특정 백업 항목에 대한 복구 지점 목록을 $StartDate 및 $EndDate.</span><span class="sxs-lookup"><span data-stu-id="bc185-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="bc185-142">마지막 명령은 모든 디스크를 대상 리소스 그룹으로 복원하고 Target_RG DestRG 리소스 그룹의 저장소 계정 DestAccount에서 VM 구성 정보와 배포 템플릿을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="bc185-143">예제 2: 지정된 복구 지점에서 백업된 Managed Disk Azure VM의 지정된 디스크 복원</span><span class="sxs-lookup"><span data-stu-id="bc185-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="bc185-144">첫 번째 명령은 Recovery Services 자격 증명 모음을 얻게 하여 $vault 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="bc185-145">두 번째 명령은 "V2VM"의 AzureVM 형식의 Backup 항목을 $BackupItem 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="bc185-146">세 번째 명령은 7일 이전의 날짜를 얻은 다음, $StartDate 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="bc185-147">네 번째 명령은 현재 날짜를 얻은 다음, $EndDate 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="bc185-148">다섯 번째 명령은 특정 백업 항목에 대한 복구 지점 목록을 $StartDate 및 $EndDate.</span><span class="sxs-lookup"><span data-stu-id="bc185-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="bc185-149">여섯 번째 명령은 restoreDiskLUN 변수에 복원할 디스크 목록을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="bc185-150">마지막 명령은 지정된 LUNS의 지정된 디스크를 대상 리소스 그룹 Target_RG 복원한 다음 DestRG 리소스 그룹의 저장소 계정 DestAccount에서 VM 구성 정보와 배포 템플릿을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="bc185-151">예제 3: 관리되는 VM의 디스크를 관리되지 않는 디스크로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="bc185-152">첫 번째 명령은 RecoveryServices 자격 증명 모음을 얻게 하여 변수에 $vault 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="bc185-153">두 번째 명령은 Backup 항목을 얻은 다음, 해당 항목을 $BackupItem 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="bc185-154">세 번째 명령은 7일 이전의 날짜를 얻은 다음, $StartDate 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="bc185-155">네 번째 명령은 현재 날짜를 얻은 다음, $EndDate 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="bc185-156">다섯 번째 명령은 특정 백업 항목에 대한 복구 지점 목록을 $StartDate 및 $EndDate.</span><span class="sxs-lookup"><span data-stu-id="bc185-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="bc185-157">여섯 번째 명령은 디스크를 관리되지 않는 디스크로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="bc185-158">예제 4: 원래 저장소 계정을 사용하여 관리되지 않는 VM을 관리되지 않는 디스크로 복원</span><span class="sxs-lookup"><span data-stu-id="bc185-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="bc185-159">첫 번째 명령은 RecoveryServices 자격 증명 모음을 얻게 하여 변수에 $vault 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="bc185-160">두 번째 명령은 Backup 항목을 얻은 다음, 해당 항목을 $BackupItem 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="bc185-161">세 번째 명령은 7일 이전의 날짜를 얻은 다음, $StartDate 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="bc185-162">네 번째 명령은 현재 날짜를 얻은 다음, $EndDate 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="bc185-163">다섯 번째 명령은 특정 백업 항목에 대한 복구 지점 목록을 $StartDate 및 $EndDate.</span><span class="sxs-lookup"><span data-stu-id="bc185-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="bc185-164">여섯 번째 명령은 디스크를 원래 저장소 계정에 관리되지 않는 디스크로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="bc185-165">예제 5: AzureFileShare 항목의 여러 파일 복원</span><span class="sxs-lookup"><span data-stu-id="bc185-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="bc185-166">첫 번째 명령은 Recovery Services 자격 증명 모음을 얻게 하여 $vault 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="bc185-167">두 번째 명령은 fileshareitem이라는 Backup 항목을 얻은 다음, $BackupItem 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="bc185-168">세 번째 명령은 특정 백업 항목에 대한 복구 지점 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="bc185-169">네 번째 명령은 복원할 파일을 지정하고 변수에 $files 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="bc185-170">마지막 명령은 지정된 파일을 원래 위치로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="bc185-171">예제 6: Azure VM 내의 SQL DB를 다른 대상 VM에 복원하여 고유한 전체 복구 지점</span><span class="sxs-lookup"><span data-stu-id="bc185-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### <span data-ttu-id="bc185-172">예제 7: Azure VM 내의 SQL DB를 로그 복구 지점에 대한 다른 대상 VM으로 복원</span><span class="sxs-lookup"><span data-stu-id="bc185-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

## <span data-ttu-id="bc185-173">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bc185-173">PARAMETERS</span></span>

### <span data-ttu-id="bc185-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc185-174">-DefaultProfile</span></span>

<span data-ttu-id="bc185-175">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc185-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="bc185-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="bc185-177">파일 공유에서 여러 파일 복원에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="bc185-178">파일 공유 내에서 복원할 항목의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-178">The paths of the items to be restored within the file share.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="bc185-179">-RecoveryPoint</span></span>

<span data-ttu-id="bc185-180">백업 항목을 복원할 복구 지점을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="bc185-181">**AzureRmRecoveryServicesBackupRecoveryPoint** 개체를 얻은 경우 **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="bc185-182">-ResolveConflict</span></span>

<span data-ttu-id="bc185-183">복원된 항목도 대상에 있는 경우 이 항목을 사용하여 덮어 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="bc185-184">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bc185-185">덮어 덮어 덮</span><span class="sxs-lookup"><span data-stu-id="bc185-185">Overwrite</span></span>
- <span data-ttu-id="bc185-186">건너뛰기</span><span class="sxs-lookup"><span data-stu-id="bc185-186">Skip</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-187">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="bc185-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="bc185-188">이 스위치를 사용하여 관리되지 않는 디스크로 복원을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-188">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-189">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="bc185-189">-RestoreDiskList</span></span>
<span data-ttu-id="bc185-190">백업된 VM을 복구할 디스크 지정</span><span class="sxs-lookup"><span data-stu-id="bc185-190">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-191">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="bc185-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="bc185-192">이 스위치를 사용하여 백업된 VM의 OS 디스크만 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-192">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="bc185-193">-SourceFilePath</span></span>

<span data-ttu-id="bc185-194">파일 공유에서 특정 항목 복원에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="bc185-195">파일 공유 내에서 복원할 항목의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-195">The path of the item to be restored within the file share.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="bc185-196">-SourceFileType</span></span>

<span data-ttu-id="bc185-197">파일 공유에서 특정 항목 복원에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="bc185-198">파일 공유 내에서 복원할 항목의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="bc185-199">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bc185-200">파일</span><span class="sxs-lookup"><span data-stu-id="bc185-200">File</span></span>
- <span data-ttu-id="bc185-201">디렉터리</span><span class="sxs-lookup"><span data-stu-id="bc185-201">Directory</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bc185-202">-StorageAccountName</span></span>

<span data-ttu-id="bc185-203">구독에서 대상 Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="bc185-204">복원 프로세스의 일부로 이 cmdlet은 이 Storage 계정에 디스크 및 구성 정보를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc185-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="bc185-206">구독에 대상 Storage 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="bc185-207">복원 프로세스의 일부로 이 cmdlet은 이 Storage 계정에 디스크 및 구성 정보를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="bc185-208">-TargetFileShareName</span></span>

<span data-ttu-id="bc185-209">파일 공유를 복원해야 하는 파일 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-209">The File Share to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="bc185-210">-TargetFolder</span></span>

<span data-ttu-id="bc185-211">파일 공유가 TargetFileShareName 내에서 복원해야 하는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="bc185-212">백업된 콘텐츠를 루트 폴더로 복원하는 경우 대상 폴더 값을 빈 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc185-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="bc185-214">관리 디스크가 복원되는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="bc185-215">관리 디스크를 통해 VM의 백업에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-215">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bc185-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="bc185-217">파일 공유를 복원해야 하는 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-217">The storage account to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bc185-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="bc185-219">복구 지점의 디스크를 원래 저장소 계정으로 복원할 경우 이 스위치를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-220">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="bc185-220">-DiskEncryptionSetId</span></span> 

<span data-ttu-id="bc185-221">복원된 디스크를 암호화하는 DES ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-221">The DES ID to encrypt the restored disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMManagedDiskParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-222">-RestoreToSecondaryRegion</span><span class="sxs-lookup"><span data-stu-id="bc185-222">-RestoreToSecondaryRegion</span></span>

<span data-ttu-id="bc185-223">이 스위치를 사용하여 보조 지역으로의 교차 지역 복원을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-223">Use this switch to trigger the Cross region restore to secondary region.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIaasVM
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-224">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bc185-224">-VaultId</span></span>

<span data-ttu-id="bc185-225">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-225">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-226">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="bc185-226">-VaultLocation</span></span>

<span data-ttu-id="bc185-227">Recovery Services Vault의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-227">Location of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-228">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="bc185-228">-WLRecoveryConfig</span></span>

<span data-ttu-id="bc185-229">복구 구성</span><span class="sxs-lookup"><span data-stu-id="bc185-229">Recovery config</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc185-230">-확인</span><span class="sxs-lookup"><span data-stu-id="bc185-230">-Confirm</span></span>

<span data-ttu-id="bc185-231">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-231">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc185-232">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc185-232">-WhatIf</span></span>

<span data-ttu-id="bc185-233">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-233">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="bc185-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc185-234">CommonParameters</span></span>
<span data-ttu-id="bc185-235">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc185-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc185-236">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc185-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc185-237">입력</span><span class="sxs-lookup"><span data-stu-id="bc185-237">INPUTS</span></span>

### <span data-ttu-id="bc185-238">System.String</span><span class="sxs-lookup"><span data-stu-id="bc185-238">System.String</span></span>

### <span data-ttu-id="bc185-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="bc185-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="bc185-240">출력</span><span class="sxs-lookup"><span data-stu-id="bc185-240">OUTPUTS</span></span>

### <span data-ttu-id="bc185-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="bc185-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="bc185-242">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bc185-242">NOTES</span></span>

## <span data-ttu-id="bc185-243">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc185-243">RELATED LINKS</span></span>

[<span data-ttu-id="bc185-244">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bc185-244">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="bc185-245">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bc185-245">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="bc185-246">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="bc185-246">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
