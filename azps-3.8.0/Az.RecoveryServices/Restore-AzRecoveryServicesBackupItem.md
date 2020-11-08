---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 69b115fab623d1a951fa2f77632a33fb437a3555
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043533"
---
# <span data-ttu-id="2d591-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2d591-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="2d591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d591-102">SYNOPSIS</span></span>

<span data-ttu-id="2d591-103">백업 항목에 대 한 데이터 및 구성을 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="2d591-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d591-104">SYNTAX</span></span>

### <span data-ttu-id="2d591-105">AzureVMParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2d591-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d591-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d591-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d591-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d591-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d591-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2d591-108">DESCRIPTION</span></span>

<span data-ttu-id="2d591-109">**AzRecoveryServicesBackupItem** Cmdlet은 Azure 백업 항목에 대 한 데이터 및 구성을 지정 된 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="2d591-110">이 cmdlet은 복구 서비스 자격 증명 모음에서 고객의 저장소 계정으로 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="2d591-111">복원 작업을 수행 해도 전체 가상 컴퓨터는 복원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="2d591-112">관리 디스크를 대상 리소스 그룹으로 복원 하 고 구성 정보를 고객 저장소 계정으로 복원 작업을 완료 한 후에는 가상 컴퓨터를 만들고 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="2d591-113">-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-113">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="2d591-114">참고:-VaultId 매개 변수 외에도이 cmdlet을 실행 하려면-VaultLocation 매개 변수를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-114">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="2d591-115">예제의</span><span class="sxs-lookup"><span data-stu-id="2d591-115">EXAMPLES</span></span>

### <span data-ttu-id="2d591-116">예제 1: 복구 시점으로 항목 복원</span><span class="sxs-lookup"><span data-stu-id="2d591-116">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetRG $ManagedDiskRG -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="2d591-117">첫 번째 명령은 Add-azurevm 유형의 백업 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2d591-118">두 번째 명령은 $Container에서 V2VM 이라는 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="2d591-119">세 번째 명령은 7 일 이전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="2d591-120">네 번째 명령은 현재 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="2d591-121">다섯 번째 명령은 $StartDate 및 $EndDate 필터링 한 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="2d591-122">지정 된 날짜 범위가 지난 7 일입니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="2d591-123">일곱 번째 명령은 복구 시점에서 복원할 디스크를 지정 하 $restoreDiskLUNs 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-123">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="2d591-124">마지막 명령은 디스크를 DestRG 리소스 그룹의 대상 저장소 계정 DestAccount로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="2d591-125">예제 2: AzureFileShare 항목의 여러 파일 복원</span><span class="sxs-lookup"><span data-stu-id="2d591-125">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="2d591-126">첫 번째 명령은 Add-azurevm 유형의 백업 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-126">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2d591-127">두 번째 명령은 fileshareitem 이라는 백업 항목을 가져온 다음이를 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-127">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="2d591-128">세 번째 명령은 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-128">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="2d591-129">네 번째 명령은 복원할 파일을 spceifies $files 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-129">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="2d591-130">마지막 명령은 지정 된 파일을 원래 위치로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-130">The last command restores the specified files to its original location.</span></span>

## <span data-ttu-id="2d591-131">변수</span><span class="sxs-lookup"><span data-stu-id="2d591-131">PARAMETERS</span></span>

### <span data-ttu-id="2d591-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d591-132">-DefaultProfile</span></span>

<span data-ttu-id="2d591-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d591-134">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="2d591-134">-MultipleSourceFilePath</span></span>
<span data-ttu-id="2d591-135">파일 공유에서 여러 파일을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-135">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="2d591-136">파일 공유 내에서 복원할 항목의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-136">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="2d591-137">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2d591-137">-RecoveryPoint</span></span>

<span data-ttu-id="2d591-138">가상 컴퓨터를 복원할 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-138">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="2d591-139">**AzureRmRecoveryServicesBackupRecoveryPoint** 개체를 얻으려면 **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-139">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d591-140">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="2d591-140">-ResolveConflict</span></span>

<span data-ttu-id="2d591-141">복원 된 항목이 대상에도 있는 경우이를 사용 하 여 덮어쓸지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-141">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="2d591-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2d591-143">덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="2d591-143">Overwrite</span></span>
- <span data-ttu-id="2d591-144">[</span><span class="sxs-lookup"><span data-stu-id="2d591-144">Skip</span></span>

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

### <span data-ttu-id="2d591-145">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="2d591-145">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="2d591-146">이 스위치를 사용 하 여 관리 되지 않는 디스크로 복원을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-146">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d591-147">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="2d591-147">-RestoreDiskList</span></span>
<span data-ttu-id="2d591-148">백업 된 VM을 복구할 디스크 지정</span><span class="sxs-lookup"><span data-stu-id="2d591-148">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d591-149">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="2d591-149">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="2d591-150">이 스위치를 사용 하 여 백업 된 VM의 OS 디스크만 복원</span><span class="sxs-lookup"><span data-stu-id="2d591-150">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d591-151">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="2d591-151">-SourceFilePath</span></span>

<span data-ttu-id="2d591-152">파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-152">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="2d591-153">파일 공유 내에서 복원할 항목의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-153">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="2d591-154">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="2d591-154">-SourceFileType</span></span>

<span data-ttu-id="2d591-155">파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-155">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="2d591-156">파일 공유 내에서 복원할 항목의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-156">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="2d591-157">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2d591-158">파일</span><span class="sxs-lookup"><span data-stu-id="2d591-158">File</span></span>
- <span data-ttu-id="2d591-159">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="2d591-159">Directory</span></span>

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

### <span data-ttu-id="2d591-160">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2d591-160">-StorageAccountName</span></span>

<span data-ttu-id="2d591-161">구독에 있는 대상 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-161">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="2d591-162">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-162">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d591-163">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d591-163">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="2d591-164">구독에서 대상 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-164">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="2d591-165">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-165">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d591-166">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="2d591-166">-TargetFileShareName</span></span>

<span data-ttu-id="2d591-167">파일 공유를 복원할 파일 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-167">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="2d591-168">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="2d591-168">-TargetFolder</span></span>

<span data-ttu-id="2d591-169">TargetFileShareName 내에서 파일 공유를 복원 해야 하는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-169">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="2d591-170">백업 된 콘텐츠를 루트 폴더로 복원 하는 경우 대상 폴더 값을 빈 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-170">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="2d591-171">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d591-171">-TargetResourceGroupName</span></span>

<span data-ttu-id="2d591-172">관리 디스크가 복원 되는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-172">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="2d591-173">관리 디스크가 있는 VM의 백업에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="2d591-173">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d591-174">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2d591-174">-TargetStorageAccountName</span></span>

<span data-ttu-id="2d591-175">파일 공유를 복원할 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-175">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="2d591-176">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d591-176">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="2d591-177">복구 지점의 디스크가 원래 저장소 계정으로 복원 되는 경우이 스위치를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-177">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d591-178">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2d591-178">-VaultId</span></span>

<span data-ttu-id="2d591-179">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-179">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2d591-180">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="2d591-180">-VaultLocation</span></span>

<span data-ttu-id="2d591-181">복구 서비스 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-181">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2d591-182">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="2d591-182">-WLRecoveryConfig</span></span>

<span data-ttu-id="2d591-183">복구 구성</span><span class="sxs-lookup"><span data-stu-id="2d591-183">Recovery config</span></span>

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

### <span data-ttu-id="2d591-184">-확인</span><span class="sxs-lookup"><span data-stu-id="2d591-184">-Confirm</span></span>

<span data-ttu-id="2d591-185">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d591-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d591-186">-WhatIf</span></span>

<span data-ttu-id="2d591-187">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d591-188">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d591-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d591-189">CommonParameters</span></span>
<span data-ttu-id="2d591-190">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d591-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d591-191">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2d591-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d591-192">입력</span><span class="sxs-lookup"><span data-stu-id="2d591-192">INPUTS</span></span>

### <span data-ttu-id="2d591-193">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d591-193">System.String</span></span>

### <span data-ttu-id="2d591-194">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="2d591-194">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="2d591-195">출력</span><span class="sxs-lookup"><span data-stu-id="2d591-195">OUTPUTS</span></span>

### <span data-ttu-id="2d591-196">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="2d591-196">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2d591-197">상속자</span><span class="sxs-lookup"><span data-stu-id="2d591-197">NOTES</span></span>

## <span data-ttu-id="2d591-198">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d591-198">RELATED LINKS</span></span>

[<span data-ttu-id="2d591-199">백업-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2d591-199">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="2d591-200">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2d591-200">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="2d591-201">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2d591-201">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
