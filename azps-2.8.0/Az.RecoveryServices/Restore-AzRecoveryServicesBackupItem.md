---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 87051d6e8c5dabe5a5e5c5138e06eda0de961219
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872598"
---
# <span data-ttu-id="125c8-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="125c8-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="125c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="125c8-102">SYNOPSIS</span></span>

<span data-ttu-id="125c8-103">백업 항목에 대 한 데이터 및 구성을 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="125c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="125c8-104">SYNTAX</span></span>

### <span data-ttu-id="125c8-105">AzureVMParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="125c8-105">AzureVMParameterSet (Default)</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="125c8-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="125c8-106">AzureFileParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="125c8-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="125c8-107">AzureWorkloadParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="125c8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="125c8-108">DESCRIPTION</span></span>

<span data-ttu-id="125c8-109">**AzRecoveryServicesBackupItem** Cmdlet은 Azure 백업 항목에 대 한 데이터 및 구성을 지정 된 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="125c8-110">이 cmdlet은 복구 서비스 자격 증명 모음에서 고객의 저장소 계정으로 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="125c8-111">복원 작업을 수행 해도 전체 가상 컴퓨터는 복원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="125c8-112">디스크 데이터 및 구성 정보를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="125c8-113">복원 작업이 완료 되 면 가상 컴퓨터를 만들어 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="125c8-114">-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="125c8-115">참고:-VaultId 매개 변수 외에도이 cmdlet을 실행 하려면-VaultLocation 매개 변수를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="125c8-116">예제의</span><span class="sxs-lookup"><span data-stu-id="125c8-116">EXAMPLES</span></span>

### <span data-ttu-id="125c8-117">예제 1: 복구 시점으로 항목 복원</span><span class="sxs-lookup"><span data-stu-id="125c8-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="125c8-118">첫 번째 명령은 Add-azurevm 유형의 백업 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="125c8-119">두 번째 명령은 $Container에서 V2VM 이라는 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="125c8-120">세 번째 명령은 7 일 이전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="125c8-121">네 번째 명령은 현재 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="125c8-122">다섯 번째 명령은 $StartDate 및 $EndDate 필터링 한 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="125c8-123">지정 된 날짜 범위가 지난 7 일입니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="125c8-124">마지막 명령은 디스크를 DestRG 리소스 그룹의 대상 저장소 계정 DestAccount로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="125c8-125">변수</span><span class="sxs-lookup"><span data-stu-id="125c8-125">PARAMETERS</span></span>

### <span data-ttu-id="125c8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="125c8-126">-DefaultProfile</span></span>

<span data-ttu-id="125c8-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="125c8-128">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="125c8-128">-RecoveryPoint</span></span>

<span data-ttu-id="125c8-129">가상 컴퓨터를 복원할 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-129">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="125c8-130">**AzureRmRecoveryServicesBackupRecoveryPoint** 개체를 얻으려면 **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-130">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="125c8-131">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="125c8-131">-ResolveConflict</span></span>

<span data-ttu-id="125c8-132">복원 된 항목이 대상에도 있는 경우이를 사용 하 여 덮어쓸지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-132">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="125c8-133">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="125c8-134">덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="125c8-134">Overwrite</span></span>
- <span data-ttu-id="125c8-135">[</span><span class="sxs-lookup"><span data-stu-id="125c8-135">Skip</span></span>

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

### <span data-ttu-id="125c8-136">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="125c8-136">-SourceFilePath</span></span>

<span data-ttu-id="125c8-137">파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-137">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="125c8-138">파일 공유 내에서 복원할 항목의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-138">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="125c8-139">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="125c8-139">-SourceFileType</span></span>

<span data-ttu-id="125c8-140">파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-140">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="125c8-141">파일 공유 내에서 복원할 항목의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-141">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="125c8-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="125c8-143">파일</span><span class="sxs-lookup"><span data-stu-id="125c8-143">File</span></span>
- <span data-ttu-id="125c8-144">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="125c8-144">Directory</span></span>

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

### <span data-ttu-id="125c8-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="125c8-145">-StorageAccountName</span></span>

<span data-ttu-id="125c8-146">구독에 있는 대상 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-146">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="125c8-147">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-147">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="125c8-148">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="125c8-148">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="125c8-149">구독에서 대상 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-149">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="125c8-150">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-150">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="125c8-151">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="125c8-151">-TargetFileShareName</span></span>

<span data-ttu-id="125c8-152">파일 공유를 복원할 파일 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-152">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="125c8-153">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="125c8-153">-TargetFolder</span></span>

<span data-ttu-id="125c8-154">TargetFileShareName 내에서 파일 공유를 복원 해야 하는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-154">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="125c8-155">백업 된 콘텐츠를 루트 폴더로 복원 하는 경우 대상 폴더 값을 빈 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-155">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="125c8-156">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="125c8-156">-TargetResourceGroupName</span></span>

<span data-ttu-id="125c8-157">관리 디스크가 복원 되는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-157">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="125c8-158">관리 디스크가 있는 VM의 백업에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="125c8-158">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="125c8-159">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="125c8-159">-TargetStorageAccountName</span></span>

<span data-ttu-id="125c8-160">파일 공유를 복원할 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-160">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="125c8-161">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="125c8-161">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="125c8-162">복구 지점의 디스크가 원래 저장소 계정으로 복원 되는 경우이 스위치를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-162">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="125c8-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="125c8-163">-VaultId</span></span>

<span data-ttu-id="125c8-164">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="125c8-165">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="125c8-165">-VaultLocation</span></span>

<span data-ttu-id="125c8-166">복구 서비스 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-166">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="125c8-167">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="125c8-167">-WLRecoveryConfig</span></span>

<span data-ttu-id="125c8-168">복구 구성</span><span class="sxs-lookup"><span data-stu-id="125c8-168">Recovery config</span></span>

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

### <span data-ttu-id="125c8-169">-확인</span><span class="sxs-lookup"><span data-stu-id="125c8-169">-Confirm</span></span>

<span data-ttu-id="125c8-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="125c8-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="125c8-171">-WhatIf</span></span>

<span data-ttu-id="125c8-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="125c8-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="125c8-174">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="125c8-174">-CommonParameters</span></span>

<span data-ttu-id="125c8-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="125c8-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="125c8-176">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="125c8-176">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="125c8-177">입력</span><span class="sxs-lookup"><span data-stu-id="125c8-177">INPUTS</span></span>

### <span data-ttu-id="125c8-178">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="125c8-178">System.String</span></span>

### <span data-ttu-id="125c8-179">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="125c8-179">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="125c8-180">출력</span><span class="sxs-lookup"><span data-stu-id="125c8-180">OUTPUTS</span></span>

### <span data-ttu-id="125c8-181">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="125c8-181">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="125c8-182">상속자</span><span class="sxs-lookup"><span data-stu-id="125c8-182">NOTES</span></span>

## <span data-ttu-id="125c8-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="125c8-183">RELATED LINKS</span></span>

[<span data-ttu-id="125c8-184">백업-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="125c8-184">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="125c8-185">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="125c8-185">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="125c8-186">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="125c8-186">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
