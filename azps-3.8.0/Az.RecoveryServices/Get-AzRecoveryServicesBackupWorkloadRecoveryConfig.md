---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6033421b9a78e7cb531d2a33eabba1e97010c4f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044720"
---
# <span data-ttu-id="c6f36-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="c6f36-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="c6f36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f36-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f36-103">이 명령은 SQL DB 등의 백업 항목에 대 한 복구 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="c6f36-104">구성 개체는 복구 모드, restore에 대 한 대상 경로, SQL의 대상 물리적 경로 같은 응용 프로그램 특정 매개 변수에 대 한 모든 세부 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="c6f36-105">구문과</span><span class="sxs-lookup"><span data-stu-id="c6f36-105">SYNTAX</span></span>

### <span data-ttu-id="c6f36-106">RpParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c6f36-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f36-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6f36-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6f36-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c6f36-108">DESCRIPTION</span></span>
<span data-ttu-id="c6f36-109">이 명령은 restore cmdlet에 전달 되는 AzureWorkload 부하 항목에 대 한 복구 구성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="c6f36-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c6f36-110">EXAMPLES</span></span>

### <span data-ttu-id="c6f36-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6f36-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="c6f36-112">첫 번째 cmdlet은 복구 시점 개체를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="c6f36-113">두 번째 cmdlet은 원래 위치 복원에 대 한 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="c6f36-114">세 번째 cmdlet은 대체 위치 복원에 대 한 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="c6f36-115">변수</span><span class="sxs-lookup"><span data-stu-id="c6f36-115">PARAMETERS</span></span>

### <span data-ttu-id="c6f36-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="c6f36-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="c6f36-117">복구 시점에 있는 DB 정보를 사용 하 여 백업 된 DB를 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="c6f36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f36-118">-DefaultProfile</span></span>
<span data-ttu-id="c6f36-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6f36-120">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c6f36-120">-FilePath</span></span>
<span data-ttu-id="c6f36-121">복원 작업의 filepath를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-121">Specifies the filepath for restore operation.</span></span>

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

### <span data-ttu-id="c6f36-122">-FromFull</span><span class="sxs-lookup"><span data-stu-id="c6f36-122">-FromFull</span></span>
<span data-ttu-id="c6f36-123">로그 백업이 적용 되는 전체 RecoveryPoint를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-123">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="c6f36-124">-항목</span><span class="sxs-lookup"><span data-stu-id="c6f36-124">-Item</span></span>
<span data-ttu-id="c6f36-125">복원 작업이 수행 되는 대상 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-125">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="c6f36-126">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="c6f36-126">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="c6f36-127">복구 시점에 있는 DB 정보를 사용 하 여 백업 된 DB를 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-127">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="c6f36-128">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="c6f36-128">-PointInTime</span></span>
<span data-ttu-id="c6f36-129">복구 지점을 가져오지 않아도 되는 시간 범위 종료 시간</span><span class="sxs-lookup"><span data-stu-id="c6f36-129">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="c6f36-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c6f36-130">-RecoveryPoint</span></span>
<span data-ttu-id="c6f36-131">복원할 복구 시점 개체</span><span class="sxs-lookup"><span data-stu-id="c6f36-131">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="c6f36-132">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="c6f36-132">-RestoreAsFiles</span></span>
<span data-ttu-id="c6f36-133">데이터베이스를 컴퓨터의 파일로 복원 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-133">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="c6f36-134">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="c6f36-134">-TargetContainer</span></span>
<span data-ttu-id="c6f36-135">DB 파일을 복원 해야 하는 대상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-135">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="c6f36-136">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="c6f36-136">-TargetItem</span></span>
<span data-ttu-id="c6f36-137">DB를 복원 해야 하는 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-137">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="c6f36-138">SQL 복원의 경우 보호 가능한 항목 유형 SQLInstance만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-138">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="c6f36-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c6f36-139">-VaultId</span></span>
<span data-ttu-id="c6f36-140">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c6f36-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f36-141">CommonParameters</span></span>
<span data-ttu-id="c6f36-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f36-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f36-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c6f36-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f36-144">입력</span><span class="sxs-lookup"><span data-stu-id="c6f36-144">INPUTS</span></span>

### <span data-ttu-id="c6f36-145">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="c6f36-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="c6f36-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6f36-146">System.String</span></span>

## <span data-ttu-id="c6f36-147">출력</span><span class="sxs-lookup"><span data-stu-id="c6f36-147">OUTPUTS</span></span>

### <span data-ttu-id="c6f36-148">유틸리티. i. i. i m a.</span><span class="sxs-lookup"><span data-stu-id="c6f36-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="c6f36-149">상속자</span><span class="sxs-lookup"><span data-stu-id="c6f36-149">NOTES</span></span>

## <span data-ttu-id="c6f36-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6f36-150">RELATED LINKS</span></span>
