---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: b454f77bc3ad00ddf604e13672d61a7445c44fed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524328"
---
# <span data-ttu-id="19cbb-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="19cbb-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="19cbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="19cbb-103">백업 항목에 대 한 데이터 및 구성을 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19cbb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19cbb-104">SYNTAX</span></span>

### <span data-ttu-id="19cbb-105">AzureVMParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="19cbb-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19cbb-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="19cbb-106">AzureFileParameterSet</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 -ResolveConflict <RestoreFSResolveConfictOption> [-SourceFilePath <String>] [-SourceFileType <SourceFileType>]
 [-TargetStorageAccountName <String>] [-TargetFileShareName <String>] [-TargetFolder <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19cbb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="19cbb-107">DESCRIPTION</span></span>
<span data-ttu-id="19cbb-108">**AzureRmRecoveryServicesBackupItem** Cmdlet은 Azure 백업 항목에 대 한 데이터 및 구성을 지정 된 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-108">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="19cbb-109">이 cmdlet은 복구 서비스 자격 증명 모음에서 고객의 저장소 계정으로 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-109">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="19cbb-110">복원 작업을 수행 해도 전체 가상 컴퓨터는 복원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-110">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="19cbb-111">디스크 데이터 및 구성 정보를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-111">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="19cbb-112">복원 작업이 완료 되 면 가상 컴퓨터를 만들어 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-112">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="19cbb-113">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-113">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="19cbb-114">예제의</span><span class="sxs-lookup"><span data-stu-id="19cbb-114">EXAMPLES</span></span>

### <span data-ttu-id="19cbb-115">예제 1: 복구 시점으로 항목 복원</span><span class="sxs-lookup"><span data-stu-id="19cbb-115">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="19cbb-116">첫 번째 명령은 Add-azurevm 유형의 백업 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-116">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="19cbb-117">두 번째 명령은 $Container에서 V2VM 이라는 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-117">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="19cbb-118">세 번째 명령은 7 일 이전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-118">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="19cbb-119">네 번째 명령은 현재 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-119">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="19cbb-120">다섯 번째 명령은 $StartDate 및 $EndDate 필터링 한 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-120">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="19cbb-121">지정 된 날짜 범위가 지난 7 일입니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-121">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="19cbb-122">마지막 명령은 디스크를 DestRG 리소스 그룹의 대상 저장소 계정 DestAccount로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-122">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="19cbb-123">변수</span><span class="sxs-lookup"><span data-stu-id="19cbb-123">PARAMETERS</span></span>

### <span data-ttu-id="19cbb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19cbb-124">-DefaultProfile</span></span>
<span data-ttu-id="19cbb-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19cbb-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="19cbb-126">-RecoveryPoint</span></span>
<span data-ttu-id="19cbb-127">가상 컴퓨터를 복원할 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-127">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="19cbb-128">**AzureRmRecoveryServicesBackupRecoveryPoint** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-128">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19cbb-129">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="19cbb-129">-ResolveConflict</span></span>
<span data-ttu-id="19cbb-130">복원 된 항목이 대상에도 있는 경우이를 사용 하 여 덮어쓸지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-130">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConfictOption
Parameter Sets: AzureFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cbb-131">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="19cbb-131">-SourceFilePath</span></span>
<span data-ttu-id="19cbb-132">파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-132">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="19cbb-133">파일 공유 내에서 복원할 항목의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-133">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="19cbb-134">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="19cbb-134">-SourceFileType</span></span>
<span data-ttu-id="19cbb-135">파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-135">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="19cbb-136">파일 공유 내에서 복원할 항목의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-136">The path of the item to be restored within the file share.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cbb-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="19cbb-137">-StorageAccountName</span></span>
<span data-ttu-id="19cbb-138">구독에 있는 대상 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-138">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="19cbb-139">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-139">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cbb-140">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19cbb-140">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="19cbb-141">구독에서 대상 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-141">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="19cbb-142">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-142">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cbb-143">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="19cbb-143">-TargetFileShareName</span></span>
<span data-ttu-id="19cbb-144">파일 공유를 복원할 파일 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-144">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="19cbb-145">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="19cbb-145">-TargetFolder</span></span>
<span data-ttu-id="19cbb-146">TargetFileShareName 내에서 파일 공유를 복원 해야 하는 폴더입니다. 변수를 비워 두어 루트 폴더 아래에 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-146">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="19cbb-147">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19cbb-147">-TargetResourceGroupName</span></span>
<span data-ttu-id="19cbb-148">관리 디스크가 복원 되는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-148">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="19cbb-149">관리 디스크가 있는 VM의 백업에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="19cbb-149">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="19cbb-150">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="19cbb-150">-TargetStorageAccountName</span></span>
<span data-ttu-id="19cbb-151">파일 공유를 복원할 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-151">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="19cbb-152">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19cbb-152">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="19cbb-153">복구 지점의 디스크가 원래 저장소 계정으로 복원 되는 경우이 스위치를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-153">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="19cbb-154">-VaultId</span><span class="sxs-lookup"><span data-stu-id="19cbb-154">-VaultId</span></span>
<span data-ttu-id="19cbb-155">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-155">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="19cbb-156">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="19cbb-156">-VaultLocation</span></span>
<span data-ttu-id="19cbb-157">복구 서비스 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-157">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="19cbb-158">-확인</span><span class="sxs-lookup"><span data-stu-id="19cbb-158">-Confirm</span></span>
<span data-ttu-id="19cbb-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19cbb-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19cbb-160">-WhatIf</span></span>
<span data-ttu-id="19cbb-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19cbb-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19cbb-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19cbb-163">CommonParameters</span></span>
<span data-ttu-id="19cbb-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cbb-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19cbb-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19cbb-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19cbb-166">입력</span><span class="sxs-lookup"><span data-stu-id="19cbb-166">INPUTS</span></span>

### <span data-ttu-id="19cbb-167">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="19cbb-167">System.String</span></span>
<span data-ttu-id="19cbb-168">매개 변수: VaultId (ByValue), VaultLocation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="19cbb-168">Parameters: VaultId (ByValue), VaultLocation (ByValue)</span></span>

### <span data-ttu-id="19cbb-169">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="19cbb-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="19cbb-170">매개 변수: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="19cbb-170">Parameters: RecoveryPoint (ByValue)</span></span>

## <span data-ttu-id="19cbb-171">출력</span><span class="sxs-lookup"><span data-stu-id="19cbb-171">OUTPUTS</span></span>

### <span data-ttu-id="19cbb-172">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="19cbb-172">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="19cbb-173">상속자</span><span class="sxs-lookup"><span data-stu-id="19cbb-173">NOTES</span></span>

## <span data-ttu-id="19cbb-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19cbb-174">RELATED LINKS</span></span>

[<span data-ttu-id="19cbb-175">백업-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="19cbb-175">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="19cbb-176">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="19cbb-176">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="19cbb-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="19cbb-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


