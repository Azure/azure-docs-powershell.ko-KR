---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 68e06f8a4d9c88b57fa88ee8044ca2e5d04d9ce9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535452"
---
# <span data-ttu-id="ce458-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ce458-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="ce458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce458-102">SYNOPSIS</span></span>
<span data-ttu-id="ce458-103">사이트 복구 계획을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce458-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce458-104">SYNTAX</span></span>

### <span data-ttu-id="ce458-105">AppendGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="ce458-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce458-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="ce458-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce458-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="ce458-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce458-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="ce458-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce458-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ce458-109">DESCRIPTION</span></span>
<span data-ttu-id="ce458-110">**편집-AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet은 Azure Site Recovery 계획을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="ce458-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ce458-111">EXAMPLES</span></span>

### <span data-ttu-id="ce458-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ce458-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="ce458-113">기존 Azure Site Recovery 복구 계획에 그룹을 추가 하 고 메모리 내 업데이트 복구 계획을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="ce458-114">변수</span><span class="sxs-lookup"><span data-stu-id="ce458-114">PARAMETERS</span></span>

### <span data-ttu-id="ce458-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ce458-115">-AddProtectedItem</span></span>
<span data-ttu-id="ce458-116">복구 계획 개체의 복구 계획 그룹에 추가할 ASR 복제 보호 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce458-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="ce458-117">-AppendGroup</span></span>
<span data-ttu-id="ce458-118">복구 계획 개체에 복구 계획 그룹을 추가 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce458-119">-그룹</span><span class="sxs-lookup"><span data-stu-id="ce458-119">-Group</span></span>
<span data-ttu-id="ce458-120">복구 계획 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-120">Specifies a recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce458-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce458-121">-InputObject</span></span>
<span data-ttu-id="ce458-122">편집할 ASR 복구 계획 개체입니다 (메모리 작업).</span><span class="sxs-lookup"><span data-stu-id="ce458-122">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="ce458-123">복구 계획을 업데이트 하려면 편집한 복구 계획 개체를 사용 하 여 Update-AzureRmASRRecoveryPlan를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-123">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce458-124">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="ce458-124">-RemoveGroup</span></span>
<span data-ttu-id="ce458-125">복구 계획 개체에서 지정 된 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-125">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce458-126">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ce458-126">-RemoveProtectedItem</span></span>
<span data-ttu-id="ce458-127">복구 계획 개체의 복구 계획 그룹에서 제거할 ASR 복제 보호 된 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-127">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce458-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ce458-128">-Confirm</span></span>
<span data-ttu-id="ce458-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce458-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce458-130">-WhatIf</span></span>
<span data-ttu-id="ce458-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce458-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce458-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce458-133">CommonParameters</span></span>
<span data-ttu-id="ce458-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce458-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce458-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce458-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce458-136">입력</span><span class="sxs-lookup"><span data-stu-id="ce458-136">INPUTS</span></span>

### <span data-ttu-id="ce458-137">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="ce458-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="ce458-138">출력</span><span class="sxs-lookup"><span data-stu-id="ce458-138">OUTPUTS</span></span>

### <span data-ttu-id="ce458-139">System. 개체</span><span class="sxs-lookup"><span data-stu-id="ce458-139">System.Object</span></span>

## <span data-ttu-id="ce458-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ce458-140">NOTES</span></span>

## <span data-ttu-id="ce458-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce458-141">RELATED LINKS</span></span>

[<span data-ttu-id="ce458-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ce458-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="ce458-143">새로운 AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ce458-143">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
