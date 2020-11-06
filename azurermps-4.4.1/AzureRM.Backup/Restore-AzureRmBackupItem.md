---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: b449b96417f0ac05fa857a48a10143a285ed888f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528279"
---
# <span data-ttu-id="d1b90-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="d1b90-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="d1b90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1b90-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b90-103">백업 항목에 대 한 데이터 및 구성을 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1b90-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1b90-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1b90-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d1b90-105">DESCRIPTION</span></span>
<span data-ttu-id="d1b90-106">**AzureRmBackupItem** Cmdlet은 Azure 백업 항목에 대 한 데이터 및 구성을 지정 된 복구 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="d1b90-107">이 cmdlet은 백업 자격 증명 모음에서 계정으로 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>

<span data-ttu-id="d1b90-108">복원 작업을 수행 해도 전체 가상 컴퓨터는 복원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="d1b90-109">디스크 데이터 및 구성 정보를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="d1b90-110">복원 작업이 완료 되 면 가상 컴퓨터를 만들어 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="d1b90-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d1b90-111">EXAMPLES</span></span>

### <span data-ttu-id="d1b90-112">예제 1: 가상 컴퓨터를 복구 시점으로 복원</span><span class="sxs-lookup"><span data-stu-id="d1b90-112">Example 1: Restore a virtual machine to a recovery point</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="d1b90-113">첫 번째 명령은 Get-AzureRmBackupVault cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="d1b90-114">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="d1b90-115">두 번째 명령은 **AzureRmBackupContainer** cmdlet을 사용 하 여 $Vault의 자격 증명 모음에서 지정 된 이름을 가진 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="d1b90-116">명령이 $Container 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-116">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="d1b90-117">세 번째 명령은 **AzureRmBackupItem** cmdlet을 사용 하 여 $Container의 컨테이너에 있는 백업 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="d1b90-118">명령이 $BackupItem 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-118">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="d1b90-119">네 번째 명령은 $BackupItem 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="d1b90-120">명령이 $RecoveryPoint 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-120">The command stores that object in the $RecoveryPoint variable.</span></span>

<span data-ttu-id="d1b90-121">마지막 명령은 이름이 DestinationAccount 인 계정에 대 한 $RecoveryPoint 복구 지점을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="d1b90-122">변수</span><span class="sxs-lookup"><span data-stu-id="d1b90-122">PARAMETERS</span></span>

### <span data-ttu-id="d1b90-123">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d1b90-123">-RecoveryPoint</span></span>
<span data-ttu-id="d1b90-124">가상 컴퓨터를 복원할 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-124">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="d1b90-125">**AzureRmBackupRecoveryPoint** 을 얻으려면 Get-AzureRmBackupRecoveryPoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-125">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1b90-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d1b90-126">-StorageAccountName</span></span>
<span data-ttu-id="d1b90-127">구독에 있는 대상 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-127">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="d1b90-128">복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-128">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

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

### <span data-ttu-id="d1b90-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b90-129">-DefaultProfile</span></span>
<span data-ttu-id="d1b90-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1b90-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b90-131">CommonParameters</span></span>
<span data-ttu-id="d1b90-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b90-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b90-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b90-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b90-134">입력</span><span class="sxs-lookup"><span data-stu-id="d1b90-134">INPUTS</span></span>

### <span data-ttu-id="d1b90-135">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d1b90-135">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="d1b90-136">출력</span><span class="sxs-lookup"><span data-stu-id="d1b90-136">OUTPUTS</span></span>

### <span data-ttu-id="d1b90-137">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="d1b90-137">AzureRmBackupJob</span></span>

## <span data-ttu-id="d1b90-138">상속자</span><span class="sxs-lookup"><span data-stu-id="d1b90-138">NOTES</span></span>

## <span data-ttu-id="d1b90-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1b90-139">RELATED LINKS</span></span>

[<span data-ttu-id="d1b90-140">백업-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="d1b90-140">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="d1b90-141">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="d1b90-141">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="d1b90-142">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d1b90-142">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)


