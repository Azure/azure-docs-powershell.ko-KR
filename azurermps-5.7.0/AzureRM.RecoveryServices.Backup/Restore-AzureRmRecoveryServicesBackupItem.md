---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 6013531367f5996924da1776c0062ebb5ad02b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526684"
---
# <span data-ttu-id="aef6f-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="aef6f-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="aef6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aef6f-102">SYNOPSIS</span></span>
<span data-ttu-id="aef6f-103">백업 항목에 대 한 데이터 및 구성을 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aef6f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aef6f-104">SYNTAX</span></span>

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aef6f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aef6f-105">DESCRIPTION</span></span>
<span data-ttu-id="aef6f-106">**AzureRmRecoveryServicesBackupItem** Cmdlet은 Azure 백업 항목에 대 한 데이터 및 구성을 지정 된 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-106">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="aef6f-107">이 cmdlet은 복구 서비스 자격 증명 모음에서 고객의 저장소 계정으로 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-107">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>

<span data-ttu-id="aef6f-108">복원 작업을 수행 해도 전체 가상 컴퓨터는 복원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="aef6f-109">디스크 데이터 및 구성 정보를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="aef6f-110">복원 작업이 완료 되 면 가상 컴퓨터를 만들어 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-110">After the restore operation is finished, you must create the virtual machine and start it.</span></span>

<span data-ttu-id="aef6f-111">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="aef6f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="aef6f-112">EXAMPLES</span></span>

### <span data-ttu-id="aef6f-113">예제 1: 복구 시점으로 항목 복원</span><span class="sxs-lookup"><span data-stu-id="aef6f-113">Example 1: Restore an item to a recovery point</span></span>
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

<span data-ttu-id="aef6f-114">첫 번째 명령은 Add-azurevm 유형의 백업 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-114">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="aef6f-115">두 번째 명령은 $Container에서 V2VM 이라는 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-115">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="aef6f-116">세 번째 명령은 7 일 이전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-116">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="aef6f-117">네 번째 명령은 현재 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-117">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="aef6f-118">다섯 번째 명령은 $StartDate 및 $EndDate 필터링 한 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-118">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="aef6f-119">지정 된 날짜 범위가 지난 7 일입니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-119">The date range specified is the last 7 days.</span></span>

<span data-ttu-id="aef6f-120">마지막 명령은 디스크를 DestRG 리소스 그룹의 대상 저장소 계정 DestAccount로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-120">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="aef6f-121">변수</span><span class="sxs-lookup"><span data-stu-id="aef6f-121">PARAMETERS</span></span>

### <span data-ttu-id="aef6f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef6f-122">-DefaultProfile</span></span>
<span data-ttu-id="aef6f-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef6f-124">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="aef6f-124">-RecoveryPoint</span></span>
<span data-ttu-id="aef6f-125">가상 컴퓨터를 복원할 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-125">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="aef6f-126">**AzureRmRecoveryServicesBackupRecoveryPoint** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-126">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aef6f-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aef6f-127">-StorageAccountName</span></span>
<span data-ttu-id="aef6f-128">구독에 있는 대상 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-128">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="aef6f-129">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-129">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef6f-130">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aef6f-130">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="aef6f-131">구독에서 대상 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-131">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="aef6f-132">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-132">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef6f-133">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aef6f-133">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="aef6f-134">복구 지점의 디스크가 원래 저장소 계정으로 복원 되는 경우이 스위치를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-134">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef6f-135">-확인</span><span class="sxs-lookup"><span data-stu-id="aef6f-135">-Confirm</span></span>
<span data-ttu-id="aef6f-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef6f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aef6f-137">-WhatIf</span></span>
<span data-ttu-id="aef6f-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aef6f-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef6f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef6f-140">CommonParameters</span></span>
<span data-ttu-id="aef6f-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef6f-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aef6f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef6f-143">입력</span><span class="sxs-lookup"><span data-stu-id="aef6f-143">INPUTS</span></span>

### <span data-ttu-id="aef6f-144">RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="aef6f-144">RecoveryPointBase</span></span>
<span data-ttu-id="aef6f-145">' RecoveryPoint ' 매개 변수는 파이프라인에서 ' RecoveryPointBase ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef6f-145">Parameter 'RecoveryPoint' accepts value of type 'RecoveryPointBase' from the pipeline</span></span>

## <span data-ttu-id="aef6f-146">출력</span><span class="sxs-lookup"><span data-stu-id="aef6f-146">OUTPUTS</span></span>

### <span data-ttu-id="aef6f-147">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="aef6f-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="aef6f-148">상속자</span><span class="sxs-lookup"><span data-stu-id="aef6f-148">NOTES</span></span>

## <span data-ttu-id="aef6f-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aef6f-149">RELATED LINKS</span></span>

[<span data-ttu-id="aef6f-150">백업-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="aef6f-150">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="aef6f-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="aef6f-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="aef6f-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="aef6f-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


