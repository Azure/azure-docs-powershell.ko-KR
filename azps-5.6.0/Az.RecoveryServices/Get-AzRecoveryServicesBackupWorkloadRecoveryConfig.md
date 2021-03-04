---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: d608b4265435041a918ba71cdd68ae00892bcc20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959483"
---
# <span data-ttu-id="563f4-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="563f4-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="563f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="563f4-102">SYNOPSIS</span></span>
<span data-ttu-id="563f4-103">이 명령은 백업된 항목(예: db)의 복구 SQL 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="563f4-104">구성 개체는 복구 모드, 복원 대상 대상 및 애플리케이션 특정 매개 변수(예: 대상 물리적 경로)과 같은 모든 세부 정보를 SQL.</span><span class="sxs-lookup"><span data-stu-id="563f4-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="563f4-105">구문</span><span class="sxs-lookup"><span data-stu-id="563f4-105">SYNTAX</span></span>

### <span data-ttu-id="563f4-106">RpParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="563f4-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="563f4-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="563f4-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="563f4-108">설명</span><span class="sxs-lookup"><span data-stu-id="563f4-108">DESCRIPTION</span></span>
<span data-ttu-id="563f4-109">명령은 복원 cmdlet에 전달되는 AzureWorkload 항목에 대한 복구 구성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="563f4-110">예제</span><span class="sxs-lookup"><span data-stu-id="563f4-110">EXAMPLES</span></span>

### <span data-ttu-id="563f4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="563f4-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="563f4-112">첫 번째 cmdlet은 복구 지점 개체를 얻는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="563f4-113">두 번째 cmdlet은 원래 위치 복원에 대한 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="563f4-114">THe 세 번째 cmdlet은 대체 위치 복원에 대한 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="563f4-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="563f4-115">Example 2</span></span>

<span data-ttu-id="563f4-116">이 명령은 백업된 항목(예: db)의 복구 SQL 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="563f4-117">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="563f4-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="563f4-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="563f4-118">PARAMETERS</span></span>

### <span data-ttu-id="563f4-119">-대체WorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="563f4-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="563f4-120">백업된 DB를 선택한 다른 서버에 복원해야 한다고 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="563f4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="563f4-121">-DefaultProfile</span></span>
<span data-ttu-id="563f4-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="563f4-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="563f4-123">-FilePath</span></span>
<span data-ttu-id="563f4-124">복원 작업에 사용되는 파일 경로가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="563f4-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="563f4-125">-FromFull</span></span>
<span data-ttu-id="563f4-126">로그 백업이 적용될 전체 복구점을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="563f4-127">-항목</span><span class="sxs-lookup"><span data-stu-id="563f4-127">-Item</span></span>
<span data-ttu-id="563f4-128">복원 작업이 수행되는 백업 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="563f4-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="563f4-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="563f4-130">백업된 DB를 복구 지점에 있는 DB 정보로 덮어 야 를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="563f4-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="563f4-131">-PointInTime</span></span>
<span data-ttu-id="563f4-132">복구 지점을 페치해야 하는 시간 범위의 종료 시간</span><span class="sxs-lookup"><span data-stu-id="563f4-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="563f4-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="563f4-133">-RecoveryPoint</span></span>
<span data-ttu-id="563f4-134">복원할 복구 지점 개체</span><span class="sxs-lookup"><span data-stu-id="563f4-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="563f4-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="563f4-135">-RestoreAsFiles</span></span>
<span data-ttu-id="563f4-136">데이터베이스를 컴퓨터의 파일로 복원하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="563f4-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="563f4-137">-TargetContainer</span></span>
<span data-ttu-id="563f4-138">DB 파일을 복원해야 하는 대상 머신을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="563f4-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="563f4-139">-TargetItem</span></span>
<span data-ttu-id="563f4-140">DB를 복원해야 하는 대상을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="563f4-141">SQL 복원의 경우 SQLInstance만 보호할 수 있는 항목 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="563f4-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="563f4-142">-VaultId</span></span>
<span data-ttu-id="563f4-143">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="563f4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563f4-144">CommonParameters</span></span>
<span data-ttu-id="563f4-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="563f4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563f4-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="563f4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563f4-147">입력</span><span class="sxs-lookup"><span data-stu-id="563f4-147">INPUTS</span></span>

### <span data-ttu-id="563f4-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="563f4-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="563f4-149">System.String</span><span class="sxs-lookup"><span data-stu-id="563f4-149">System.String</span></span>

## <span data-ttu-id="563f4-150">출력</span><span class="sxs-lookup"><span data-stu-id="563f4-150">OUTPUTS</span></span>

### <span data-ttu-id="563f4-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="563f4-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="563f4-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="563f4-152">NOTES</span></span>

## <span data-ttu-id="563f4-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="563f4-153">RELATED LINKS</span></span>
