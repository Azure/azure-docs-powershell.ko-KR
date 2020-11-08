---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 52e4a9b76adc8c8980ab20951278435894a303bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217212"
---
# <span data-ttu-id="17437-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="17437-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="17437-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17437-102">SYNOPSIS</span></span>

<span data-ttu-id="17437-103">백업 항목에 대 한 데이터 및 구성을 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="17437-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17437-104">SYNTAX</span></span>

### <span data-ttu-id="17437-105">AzureVMParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="17437-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17437-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="17437-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17437-107">AzureVMRestoreAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="17437-107">AzureVMRestoreAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17437-108">AzureVMTargetRGParameterSet</span><span class="sxs-lookup"><span data-stu-id="17437-108">AzureVMTargetRGParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17437-109">AzureVMUseOSAParameterSet</span><span class="sxs-lookup"><span data-stu-id="17437-109">AzureVMUseOSAParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17437-110">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="17437-110">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17437-111">설명은</span><span class="sxs-lookup"><span data-stu-id="17437-111">DESCRIPTION</span></span>

<span data-ttu-id="17437-112">**AzRecoveryServicesBackupItem** Cmdlet은 Azure 백업 항목에 대 한 데이터 및 구성을 지정 된 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-112">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="17437-113">이 cmdlet은 복구 서비스 자격 증명 모음에서 고객의 저장소 계정으로 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-113">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="17437-114">복원 작업을 수행 해도 전체 가상 컴퓨터는 복원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17437-114">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="17437-115">관리 디스크를 대상 리소스 그룹으로 복원 하 고 구성 정보를 고객 저장소 계정으로 복원 작업을 완료 한 후에는 가상 컴퓨터를 만들고 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-115">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="17437-116">자세한 내용은 다른 가능한 매개 변수 집합 및 매개 변수 텍스트를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="17437-116">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="17437-117">-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-117">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="17437-118">참고:-VaultId 매개 변수 외에도이 cmdlet을 실행 하려면-VaultLocation 매개 변수를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-118">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="17437-119">예제의</span><span class="sxs-lookup"><span data-stu-id="17437-119">EXAMPLES</span></span>

### <span data-ttu-id="17437-120">예제 1: 복구 시점으로 항목 복원</span><span class="sxs-lookup"><span data-stu-id="17437-120">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="17437-121">첫 번째 명령은 RecoveryServices 자격 증명 모음을 가져와 $vault 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-121">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="17437-122">두 번째 명령은 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-122">The second command gets the Backup items and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="17437-123">세 번째 명령은 7 일 이전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-123">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="17437-124">네 번째 명령은 현재 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-124">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="17437-125">다섯 번째 명령은 $StartDate 및 $EndDate 필터링 한 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17437-125">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="17437-126">여섯 번째 명령은 복구 시점에서 복원할 디스크를 지정 하 $restoreDiskLUNs 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-126">The sixth command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="17437-127">마지막 명령은 디스크를 DestRG 리소스 그룹의 대상 저장소 계정 DestAccount로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-127">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="17437-128">예제 2: AzureFileShare 항목의 여러 파일 복원</span><span class="sxs-lookup"><span data-stu-id="17437-128">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="17437-129">첫 번째 명령은 Add-azurevm 유형의 백업 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-129">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="17437-130">두 번째 명령은 fileshareitem 이라는 백업 항목을 가져온 다음이를 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-130">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="17437-131">세 번째 명령은 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17437-131">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="17437-132">네 번째 명령은 복원할 파일을 spceifies $files 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-132">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="17437-133">마지막 명령은 지정 된 파일을 원래 위치로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-133">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="17437-134">예제 3</span><span class="sxs-lookup"><span data-stu-id="17437-134">Example 3</span></span>

<span data-ttu-id="17437-135">백업 항목에 대 한 데이터 및 구성을 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-135">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="17437-136">생성</span><span class="sxs-lookup"><span data-stu-id="17437-136">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```
### <span data-ttu-id="17437-137">예제 4: 관리 되는 VM을 관리 디스크로 복원</span><span class="sxs-lookup"><span data-stu-id="17437-137">Example 4: Restore a managed VM as managed Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="17437-138">첫 번째 명령은 RecoveryServices 자격 증명 모음을 가져와 $vault 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-138">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="17437-139">두 번째 명령은 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-139">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="17437-140">세 번째 명령은 7 일 이전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-140">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="17437-141">네 번째 명령은 현재 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-141">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="17437-142">다섯 번째 명령은 $StartDate 및 $EndDate 필터링 한 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17437-142">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="17437-143">여섯째 명령은 지정 된 대상 리소스 그룹을 사용 하 여 디스크를 관리 되는 디스크로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-143">The sixth command restores the disks as managed disks with the given target resource group.</span></span>

### <span data-ttu-id="17437-144">예제 5: 관리 되는 VM을 관리 되지 않는 디스크로 복원</span><span class="sxs-lookup"><span data-stu-id="17437-144">Example 5: Restore a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="17437-145">첫 번째 명령은 RecoveryServices 자격 증명 모음을 가져와 $vault 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-145">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="17437-146">두 번째 명령은 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-146">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="17437-147">세 번째 명령은 7 일 이전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-147">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="17437-148">네 번째 명령은 현재 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-148">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="17437-149">다섯 번째 명령은 $StartDate 및 $EndDate 필터링 한 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17437-149">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="17437-150">여섯 번째 명령은 디스크를 관리 되지 않는 디스크로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-150">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="17437-151">예제 6: 원래 저장소 계정을 사용 하 여 관리 되지 않는 VM을 관리 되지 않는 디스크로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-151">Example 6: Restore an unmanaged VM as unmanaged Disks using original storage account.</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="17437-152">첫 번째 명령은 RecoveryServices 자격 증명 모음을 가져와 $vault 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="17437-153">두 번째 명령은 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="17437-154">세 번째 명령은 7 일 이전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="17437-155">네 번째 명령은 현재 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="17437-156">다섯 번째 명령은 $StartDate 및 $EndDate 필터링 한 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17437-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="17437-157">여섯 번째 명령은 VM의 원래 저장소 계정을 사용 하 여 디스크를 관리 되지 않는 디스크로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-157">The sixth command restores the disks as unmanaged disks using the original storage account of the VM.</span></span>

## <span data-ttu-id="17437-158">변수</span><span class="sxs-lookup"><span data-stu-id="17437-158">PARAMETERS</span></span>

### <span data-ttu-id="17437-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17437-159">-DefaultProfile</span></span>

<span data-ttu-id="17437-160">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17437-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17437-161">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="17437-161">-MultipleSourceFilePath</span></span>
<span data-ttu-id="17437-162">파일 공유에서 여러 파일을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17437-162">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="17437-163">파일 공유 내에서 복원할 항목의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="17437-163">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="17437-164">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="17437-164">-RecoveryPoint</span></span>

<span data-ttu-id="17437-165">백업 항목을 복원할 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-165">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="17437-166">**AzureRmRecoveryServicesBackupRecoveryPoint** 개체를 얻으려면 **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-166">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="17437-167">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="17437-167">-ResolveConflict</span></span>

<span data-ttu-id="17437-168">복원 된 항목이 대상에도 있는 경우이를 사용 하 여 덮어쓸지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="17437-168">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="17437-169">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="17437-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="17437-170">덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="17437-170">Overwrite</span></span>
- <span data-ttu-id="17437-171">[</span><span class="sxs-lookup"><span data-stu-id="17437-171">Skip</span></span>

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

### <span data-ttu-id="17437-172">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="17437-172">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="17437-173">이 스위치를 사용 하 여 관리 되지 않는 디스크로 복원을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-173">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="17437-174">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="17437-174">-RestoreDiskList</span></span>
<span data-ttu-id="17437-175">백업 된 VM을 복구할 디스크 지정</span><span class="sxs-lookup"><span data-stu-id="17437-175">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="17437-176">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="17437-176">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="17437-177">이 스위치를 사용 하 여 백업 된 VM의 OS 디스크만 복원</span><span class="sxs-lookup"><span data-stu-id="17437-177">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="17437-178">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="17437-178">-SourceFilePath</span></span>

<span data-ttu-id="17437-179">파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17437-179">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="17437-180">파일 공유 내에서 복원할 항목의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="17437-180">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="17437-181">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="17437-181">-SourceFileType</span></span>

<span data-ttu-id="17437-182">파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17437-182">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="17437-183">파일 공유 내에서 복원할 항목의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="17437-183">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="17437-184">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="17437-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="17437-185">파일</span><span class="sxs-lookup"><span data-stu-id="17437-185">File</span></span>
- <span data-ttu-id="17437-186">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="17437-186">Directory</span></span>

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

### <span data-ttu-id="17437-187">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="17437-187">-StorageAccountName</span></span>

<span data-ttu-id="17437-188">구독에 있는 대상 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-188">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="17437-189">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-189">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="17437-190">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17437-190">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="17437-191">구독에서 대상 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-191">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="17437-192">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-192">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="17437-193">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="17437-193">-TargetFileShareName</span></span>

<span data-ttu-id="17437-194">파일 공유를 복원할 파일 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="17437-194">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="17437-195">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="17437-195">-TargetFolder</span></span>

<span data-ttu-id="17437-196">TargetFileShareName 내에서 파일 공유를 복원 해야 하는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="17437-196">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="17437-197">백업 된 콘텐츠를 루트 폴더로 복원 하는 경우 대상 폴더 값을 빈 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-197">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="17437-198">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17437-198">-TargetResourceGroupName</span></span>

<span data-ttu-id="17437-199">관리 디스크가 복원 되는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="17437-199">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="17437-200">관리 디스크가 있는 VM의 백업에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="17437-200">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="17437-201">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="17437-201">-TargetStorageAccountName</span></span>

<span data-ttu-id="17437-202">파일 공유를 복원할 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="17437-202">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="17437-203">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17437-203">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="17437-204">복구 지점의 디스크가 원래 저장소 계정으로 복원 되는 경우이 스위치를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-204">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="17437-205">-VaultId</span><span class="sxs-lookup"><span data-stu-id="17437-205">-VaultId</span></span>

<span data-ttu-id="17437-206">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="17437-206">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="17437-207">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="17437-207">-VaultLocation</span></span>

<span data-ttu-id="17437-208">복구 서비스 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="17437-208">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="17437-209">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="17437-209">-WLRecoveryConfig</span></span>

<span data-ttu-id="17437-210">복구 구성</span><span class="sxs-lookup"><span data-stu-id="17437-210">Recovery config</span></span>

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

### <span data-ttu-id="17437-211">-확인</span><span class="sxs-lookup"><span data-stu-id="17437-211">-Confirm</span></span>

<span data-ttu-id="17437-212">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17437-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17437-213">-WhatIf</span></span>

<span data-ttu-id="17437-214">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="17437-214">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="17437-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17437-215">CommonParameters</span></span>
<span data-ttu-id="17437-216">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17437-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17437-217">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="17437-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17437-218">입력</span><span class="sxs-lookup"><span data-stu-id="17437-218">INPUTS</span></span>

### <span data-ttu-id="17437-219">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="17437-219">System.String</span></span>

### <span data-ttu-id="17437-220">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="17437-220">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="17437-221">출력</span><span class="sxs-lookup"><span data-stu-id="17437-221">OUTPUTS</span></span>

### <span data-ttu-id="17437-222">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="17437-222">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="17437-223">상속자</span><span class="sxs-lookup"><span data-stu-id="17437-223">NOTES</span></span>

## <span data-ttu-id="17437-224">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17437-224">RELATED LINKS</span></span>

[<span data-ttu-id="17437-225">백업-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="17437-225">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="17437-226">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="17437-226">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="17437-227">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="17437-227">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
