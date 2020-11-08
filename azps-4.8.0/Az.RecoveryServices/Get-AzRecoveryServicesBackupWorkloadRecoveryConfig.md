---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212725"
---
# <span data-ttu-id="19e17-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="19e17-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="19e17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19e17-102">SYNOPSIS</span></span>
<span data-ttu-id="19e17-103">이 명령은 SQL DB 등의 백업 항목에 대 한 복구 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="19e17-104">구성 개체는 복구 모드, restore에 대 한 대상 경로, SQL의 대상 물리적 경로 같은 응용 프로그램 특정 매개 변수에 대 한 모든 세부 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="19e17-105">구문과</span><span class="sxs-lookup"><span data-stu-id="19e17-105">SYNTAX</span></span>

### <span data-ttu-id="19e17-106">RpParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="19e17-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19e17-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="19e17-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19e17-108">설명은</span><span class="sxs-lookup"><span data-stu-id="19e17-108">DESCRIPTION</span></span>
<span data-ttu-id="19e17-109">이 명령은 restore cmdlet에 전달 되는 AzureWorkload 부하 항목에 대 한 복구 구성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="19e17-110">예제의</span><span class="sxs-lookup"><span data-stu-id="19e17-110">EXAMPLES</span></span>

### <span data-ttu-id="19e17-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="19e17-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="19e17-112">첫 번째 cmdlet은 복구 시점 개체를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="19e17-113">두 번째 cmdlet은 원래 위치 복원에 대 한 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="19e17-114">세 번째 cmdlet은 대체 위치 복원에 대 한 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="19e17-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="19e17-115">Example 2</span></span>

<span data-ttu-id="19e17-116">이 명령은 SQL DB 등의 백업 항목에 대 한 복구 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="19e17-117">생성</span><span class="sxs-lookup"><span data-stu-id="19e17-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="19e17-118">변수</span><span class="sxs-lookup"><span data-stu-id="19e17-118">PARAMETERS</span></span>

### <span data-ttu-id="19e17-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="19e17-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="19e17-120">백업 된 DB를 선택한 다른 서버에 복원 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="19e17-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e17-121">-DefaultProfile</span></span>
<span data-ttu-id="19e17-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19e17-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="19e17-123">-FilePath</span></span>
<span data-ttu-id="19e17-124">복원 작업에 사용 되는 filepath를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-124">Specifies the filepath which is used for restore operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e17-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="19e17-125">-FromFull</span></span>
<span data-ttu-id="19e17-126">로그 백업이 적용 되는 전체 RecoveryPoint를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e17-127">-항목</span><span class="sxs-lookup"><span data-stu-id="19e17-127">-Item</span></span>
<span data-ttu-id="19e17-128">복원 작업이 수행 되는 대상 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-128">Specifies the backup item on which the restore operation is being performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e17-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="19e17-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="19e17-130">복구 시점에 있는 DB 정보를 사용 하 여 백업 된 DB를 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="19e17-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="19e17-131">-PointInTime</span></span>
<span data-ttu-id="19e17-132">복구 지점을 가져오지 않아도 되는 시간 범위 종료 시간</span><span class="sxs-lookup"><span data-stu-id="19e17-132">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.DateTime
Parameter Sets: LogChainParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e17-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="19e17-133">-RecoveryPoint</span></span>
<span data-ttu-id="19e17-134">복원할 복구 시점 개체</span><span class="sxs-lookup"><span data-stu-id="19e17-134">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: RpParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19e17-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="19e17-135">-RestoreAsFiles</span></span>
<span data-ttu-id="19e17-136">데이터베이스를 컴퓨터의 파일로 복원 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="19e17-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="19e17-137">-TargetContainer</span></span>
<span data-ttu-id="19e17-138">DB 파일을 복원 해야 하는 대상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-138">Specifies the target machine on which DB Files need to be restored.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e17-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="19e17-139">-TargetItem</span></span>
<span data-ttu-id="19e17-140">DB를 복원 해야 하는 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="19e17-141">SQL 복원의 경우 보호 가능한 항목 유형 SQLInstance만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e17-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="19e17-142">-VaultId</span></span>
<span data-ttu-id="19e17-143">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="19e17-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e17-144">CommonParameters</span></span>
<span data-ttu-id="19e17-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19e17-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e17-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19e17-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e17-147">입력</span><span class="sxs-lookup"><span data-stu-id="19e17-147">INPUTS</span></span>

### <span data-ttu-id="19e17-148">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="19e17-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="19e17-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="19e17-149">System.String</span></span>

## <span data-ttu-id="19e17-150">출력</span><span class="sxs-lookup"><span data-stu-id="19e17-150">OUTPUTS</span></span>

### <span data-ttu-id="19e17-151">유틸리티. i. i. i m a.</span><span class="sxs-lookup"><span data-stu-id="19e17-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="19e17-152">상속자</span><span class="sxs-lookup"><span data-stu-id="19e17-152">NOTES</span></span>

## <span data-ttu-id="19e17-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19e17-153">RELATED LINKS</span></span>
