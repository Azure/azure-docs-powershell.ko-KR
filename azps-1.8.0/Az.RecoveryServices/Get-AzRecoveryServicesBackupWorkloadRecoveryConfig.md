---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6b0f2e2c5b2e9579a92b2cee7387a19fda498fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699683"
---
# <span data-ttu-id="c5ddc-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="c5ddc-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="c5ddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ddc-103">이 명령은 SQL DB 등의 백업 항목에 대 한 복구 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="c5ddc-104">구성 개체는 복구 모드, restore에 대 한 대상 경로, SQL의 대상 물리적 경로 같은 응용 프로그램 특정 매개 변수에 대 한 모든 세부 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="c5ddc-105">구문과</span><span class="sxs-lookup"><span data-stu-id="c5ddc-105">SYNTAX</span></span>

### <span data-ttu-id="c5ddc-106">RpParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c5ddc-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ddc-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5ddc-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5ddc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c5ddc-108">DESCRIPTION</span></span>
<span data-ttu-id="c5ddc-109">이 명령은 restore cmdlet에 전달 되는 AzureWorkload 부하 항목에 대 한 복구 구성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="c5ddc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c5ddc-110">EXAMPLES</span></span>

### <span data-ttu-id="c5ddc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c5ddc-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="c5ddc-112">첫 번째 cmdlet은 복구 시점 개체를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="c5ddc-113">두 번째 cmdlet은 원래 위치 복원에 대 한 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="c5ddc-114">세 번째 cmdlet은 대체 위치 복원에 대 한 복구 계획을 crreats.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-114">THe third cmdlet crreats a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="c5ddc-115">변수</span><span class="sxs-lookup"><span data-stu-id="c5ddc-115">PARAMETERS</span></span>

### <span data-ttu-id="c5ddc-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="c5ddc-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="c5ddc-117">복구 시점에 있는 DB 정보를 사용 하 여 백업 된 DB를 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="c5ddc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5ddc-118">-DefaultProfile</span></span>
<span data-ttu-id="c5ddc-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5ddc-120">-항목</span><span class="sxs-lookup"><span data-stu-id="c5ddc-120">-Item</span></span>
<span data-ttu-id="c5ddc-121">복원 작업이 수행 되는 대상 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-121">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="c5ddc-122">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="c5ddc-122">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="c5ddc-123">복구 시점에 있는 DB 정보를 사용 하 여 백업 된 DB를 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-123">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="c5ddc-124">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="c5ddc-124">-PointInTime</span></span>
<span data-ttu-id="c5ddc-125">복구 지점을 가져오지 않아도 되는 시간 범위 종료 시간</span><span class="sxs-lookup"><span data-stu-id="c5ddc-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="c5ddc-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c5ddc-126">-RecoveryPoint</span></span>
<span data-ttu-id="c5ddc-127">복원할 복구 시점 개체</span><span class="sxs-lookup"><span data-stu-id="c5ddc-127">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="c5ddc-128">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="c5ddc-128">-TargetItem</span></span>
<span data-ttu-id="c5ddc-129">DB를 복원 해야 하는 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-129">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="c5ddc-130">SQL 복원의 경우 보호 가능한 항목 유형 SQLInstance만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-130">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="c5ddc-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c5ddc-131">-VaultId</span></span>
<span data-ttu-id="c5ddc-132">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c5ddc-133">-확인</span><span class="sxs-lookup"><span data-stu-id="c5ddc-133">-Confirm</span></span>
<span data-ttu-id="c5ddc-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5ddc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5ddc-135">-WhatIf</span></span>
<span data-ttu-id="c5ddc-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5ddc-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5ddc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ddc-138">CommonParameters</span></span>
<span data-ttu-id="c5ddc-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ddc-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5ddc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ddc-141">입력</span><span class="sxs-lookup"><span data-stu-id="c5ddc-141">INPUTS</span></span>

### <span data-ttu-id="c5ddc-142">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="c5ddc-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c5ddc-143">System.String</span></span>

## <span data-ttu-id="c5ddc-144">출력</span><span class="sxs-lookup"><span data-stu-id="c5ddc-144">OUTPUTS</span></span>

### <span data-ttu-id="c5ddc-145">유틸리티. i. i. i m a.</span><span class="sxs-lookup"><span data-stu-id="c5ddc-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="c5ddc-146">상속자</span><span class="sxs-lookup"><span data-stu-id="c5ddc-146">NOTES</span></span>

## <span data-ttu-id="c5ddc-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5ddc-147">RELATED LINKS</span></span>