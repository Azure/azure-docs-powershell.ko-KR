---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: eb54d22f74216dc883726d34df204ce80c711a22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699621"
---
# <span data-ttu-id="68a23-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="68a23-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="68a23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68a23-102">SYNOPSIS</span></span>
<span data-ttu-id="68a23-103">백업 항목에 대 한 데이터 및 구성을 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="68a23-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68a23-104">SYNTAX</span></span>

### <span data-ttu-id="68a23-105">AzureVMParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="68a23-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68a23-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="68a23-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68a23-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="68a23-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68a23-108">설명은</span><span class="sxs-lookup"><span data-stu-id="68a23-108">DESCRIPTION</span></span>
<span data-ttu-id="68a23-109">**AzRecoveryServicesBackupItem** Cmdlet은 Azure 백업 항목에 대 한 데이터 및 구성을 지정 된 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="68a23-110">이 cmdlet은 복구 서비스 자격 증명 모음에서 고객의 저장소 계정으로 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="68a23-111">복원 작업을 수행 해도 전체 가상 컴퓨터는 복원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="68a23-112">디스크 데이터 및 구성 정보를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="68a23-113">복원 작업이 완료 되 면 가상 컴퓨터를 만들어 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="68a23-114">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-114">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="68a23-115">예제의</span><span class="sxs-lookup"><span data-stu-id="68a23-115">EXAMPLES</span></span>

### <span data-ttu-id="68a23-116">예제 1: 복구 시점으로 항목 복원</span><span class="sxs-lookup"><span data-stu-id="68a23-116">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="68a23-117">첫 번째 명령은 Add-azurevm 유형의 백업 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="68a23-118">두 번째 명령은 $Container에서 V2VM 이라는 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="68a23-119">세 번째 명령은 7 일 이전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="68a23-120">네 번째 명령은 현재 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="68a23-121">다섯 번째 명령은 $StartDate 및 $EndDate 필터링 한 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="68a23-122">지정 된 날짜 범위가 지난 7 일입니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="68a23-123">마지막 명령은 디스크를 DestRG 리소스 그룹의 대상 저장소 계정 DestAccount로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-123">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="68a23-124">변수</span><span class="sxs-lookup"><span data-stu-id="68a23-124">PARAMETERS</span></span>

### <span data-ttu-id="68a23-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a23-125">-DefaultProfile</span></span>
<span data-ttu-id="68a23-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68a23-127">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="68a23-127">-RecoveryPoint</span></span>
<span data-ttu-id="68a23-128">가상 컴퓨터를 복원할 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-128">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="68a23-129">**AzureRmRecoveryServicesBackupRecoveryPoint** 개체를 가져오려면 Get-AzRecoveryServicesBackupRecoveryPoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-129">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

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

### <span data-ttu-id="68a23-130">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="68a23-130">-ResolveConflict</span></span>
<span data-ttu-id="68a23-131">복원 된 항목이 대상에도 있는 경우이를 사용 하 여 덮어쓸지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-131">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

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

### <span data-ttu-id="68a23-132">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="68a23-132">-SourceFilePath</span></span>
<span data-ttu-id="68a23-133">파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-133">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="68a23-134">파일 공유 내에서 복원할 항목의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-134">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="68a23-135">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="68a23-135">-SourceFileType</span></span>
<span data-ttu-id="68a23-136">파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-136">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="68a23-137">파일 공유 내에서 복원할 항목의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-137">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="68a23-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="68a23-138">-StorageAccountName</span></span>
<span data-ttu-id="68a23-139">구독에 있는 대상 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-139">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="68a23-140">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-140">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="68a23-141">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a23-141">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="68a23-142">구독에서 대상 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-142">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="68a23-143">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-143">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="68a23-144">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="68a23-144">-TargetFileShareName</span></span>
<span data-ttu-id="68a23-145">파일 공유를 복원할 파일 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-145">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="68a23-146">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="68a23-146">-TargetFolder</span></span>
<span data-ttu-id="68a23-147">TargetFileShareName 내에서 파일 공유를 복원 해야 하는 폴더입니다. 변수를 비워 두어 루트 폴더 아래에 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-147">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="68a23-148">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a23-148">-TargetResourceGroupName</span></span>
<span data-ttu-id="68a23-149">관리 디스크가 복원 되는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-149">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="68a23-150">관리 디스크가 있는 VM의 백업에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="68a23-150">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="68a23-151">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="68a23-151">-TargetStorageAccountName</span></span>
<span data-ttu-id="68a23-152">파일 공유를 복원할 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-152">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="68a23-153">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68a23-153">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="68a23-154">복구 지점의 디스크가 원래 저장소 계정으로 복원 되는 경우이 스위치를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-154">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="68a23-155">-VaultId</span><span class="sxs-lookup"><span data-stu-id="68a23-155">-VaultId</span></span>
<span data-ttu-id="68a23-156">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-156">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="68a23-157">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="68a23-157">-VaultLocation</span></span>
<span data-ttu-id="68a23-158">복구 서비스 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-158">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="68a23-159">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="68a23-159">-WLRecoveryConfig</span></span>
<span data-ttu-id="68a23-160">복구 구성</span><span class="sxs-lookup"><span data-stu-id="68a23-160">Recovery config</span></span>

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

### <span data-ttu-id="68a23-161">-확인</span><span class="sxs-lookup"><span data-stu-id="68a23-161">-Confirm</span></span>
<span data-ttu-id="68a23-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68a23-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a23-163">-WhatIf</span></span>
<span data-ttu-id="68a23-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68a23-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68a23-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a23-166">CommonParameters</span></span>
<span data-ttu-id="68a23-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a23-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a23-168">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68a23-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a23-169">입력</span><span class="sxs-lookup"><span data-stu-id="68a23-169">INPUTS</span></span>

### <span data-ttu-id="68a23-170">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68a23-170">System.String</span></span>

### <span data-ttu-id="68a23-171">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="68a23-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="68a23-172">출력</span><span class="sxs-lookup"><span data-stu-id="68a23-172">OUTPUTS</span></span>

### <span data-ttu-id="68a23-173">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="68a23-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="68a23-174">상속자</span><span class="sxs-lookup"><span data-stu-id="68a23-174">NOTES</span></span>

## <span data-ttu-id="68a23-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68a23-175">RELATED LINKS</span></span>

[<span data-ttu-id="68a23-176">백업-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="68a23-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="68a23-177">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="68a23-177">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="68a23-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="68a23-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)


