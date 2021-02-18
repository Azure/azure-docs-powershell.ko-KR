---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192945"
---
# <span data-ttu-id="06dc6-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="06dc6-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="06dc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="06dc6-103">이 명령은 백업된 항목(예: SQL DB)의 복구 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="06dc6-104">구성 개체는 복구 모드, 복원에 대한 대상 대상 및 애플리케이션별 매개 변수(예: 복구 모드의 대상 물리적 경로)를 SQL.</span><span class="sxs-lookup"><span data-stu-id="06dc6-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="06dc6-105">구문</span><span class="sxs-lookup"><span data-stu-id="06dc6-105">SYNTAX</span></span>

### <span data-ttu-id="06dc6-106">RpParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="06dc6-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06dc6-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="06dc6-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06dc6-108">설명</span><span class="sxs-lookup"><span data-stu-id="06dc6-108">DESCRIPTION</span></span>
<span data-ttu-id="06dc6-109">이 명령은 복원 cmdlet에 전달되는 AzureWorkload 항목에 대한 복구 구성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="06dc6-110">예제</span><span class="sxs-lookup"><span data-stu-id="06dc6-110">EXAMPLES</span></span>

### <span data-ttu-id="06dc6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="06dc6-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="06dc6-112">첫 번째 cmdlet은 복구 지점 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="06dc6-113">두 번째 cmdlet은 원래 위치 복원에 대한 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="06dc6-114">세 번째 cmdlet은 대체 위치 복원을 위한 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="06dc6-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="06dc6-115">Example 2</span></span>

<span data-ttu-id="06dc6-116">이 명령은 백업된 항목(예: SQL DB)의 복구 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="06dc6-117">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="06dc6-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="06dc6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06dc6-118">PARAMETERS</span></span>

### <span data-ttu-id="06dc6-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="06dc6-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="06dc6-120">백업된 DB를 선택한 다른 서버로 복원해야 한다고 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="06dc6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06dc6-121">-DefaultProfile</span></span>
<span data-ttu-id="06dc6-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06dc6-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="06dc6-123">-FilePath</span></span>
<span data-ttu-id="06dc6-124">복원 작업에 사용되는 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="06dc6-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="06dc6-125">-FromFull</span></span>
<span data-ttu-id="06dc6-126">로그 백업이 적용될 전체 RecoveryPoint를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="06dc6-127">-Item</span><span class="sxs-lookup"><span data-stu-id="06dc6-127">-Item</span></span>
<span data-ttu-id="06dc6-128">복원 작업이 수행되는 백업 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="06dc6-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="06dc6-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="06dc6-130">백업된 DB를 복구 지점에 있는 DB 정보로 덮어 사용하게 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="06dc6-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="06dc6-131">-PointInTime</span></span>
<span data-ttu-id="06dc6-132">복구 지점을 페치해야 하는 시간 범위의 종료 시간</span><span class="sxs-lookup"><span data-stu-id="06dc6-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="06dc6-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="06dc6-133">-RecoveryPoint</span></span>
<span data-ttu-id="06dc6-134">복원할 복구 지점 개체</span><span class="sxs-lookup"><span data-stu-id="06dc6-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="06dc6-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="06dc6-135">-RestoreAsFiles</span></span>
<span data-ttu-id="06dc6-136">데이터베이스를 컴퓨터의 파일로 복원하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="06dc6-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="06dc6-137">-TargetContainer</span></span>
<span data-ttu-id="06dc6-138">DB 파일을 복원해야 하는 대상 머신을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="06dc6-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="06dc6-139">-TargetItem</span></span>
<span data-ttu-id="06dc6-140">DB를 복원해야 하는 대상을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="06dc6-141">복원 SQL 경우 보호 가능한 항목 유형 SQLInstance만 해당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="06dc6-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="06dc6-142">-VaultId</span></span>
<span data-ttu-id="06dc6-143">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="06dc6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06dc6-144">CommonParameters</span></span>
<span data-ttu-id="06dc6-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06dc6-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="06dc6-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06dc6-147">입력</span><span class="sxs-lookup"><span data-stu-id="06dc6-147">INPUTS</span></span>

### <span data-ttu-id="06dc6-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="06dc6-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="06dc6-149">System.String</span><span class="sxs-lookup"><span data-stu-id="06dc6-149">System.String</span></span>

## <span data-ttu-id="06dc6-150">출력</span><span class="sxs-lookup"><span data-stu-id="06dc6-150">OUTPUTS</span></span>

### <span data-ttu-id="06dc6-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="06dc6-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="06dc6-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="06dc6-152">NOTES</span></span>

## <span data-ttu-id="06dc6-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06dc6-153">RELATED LINKS</span></span>
