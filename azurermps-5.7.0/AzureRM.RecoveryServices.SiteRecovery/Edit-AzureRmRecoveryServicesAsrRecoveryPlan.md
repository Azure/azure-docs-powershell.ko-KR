---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 289804771010a586b73621ec5df81805ed30ae55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532688"
---
# <span data-ttu-id="2d068-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2d068-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="2d068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d068-102">SYNOPSIS</span></span>
<span data-ttu-id="2d068-103">사이트 복구 계획을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d068-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d068-104">SYNTAX</span></span>

### <span data-ttu-id="2d068-105">AppendGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="2d068-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d068-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="2d068-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d068-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="2d068-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d068-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="2d068-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d068-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2d068-109">DESCRIPTION</span></span>
<span data-ttu-id="2d068-110">**편집-AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet은 Azure Site Recovery 계획을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="2d068-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2d068-111">EXAMPLES</span></span>

### <span data-ttu-id="2d068-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2d068-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="2d068-113">기존 Azure Site Recovery 복구 계획에 그룹을 추가 하 고 메모리 내 업데이트 복구 계획을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="2d068-114">변수</span><span class="sxs-lookup"><span data-stu-id="2d068-114">PARAMETERS</span></span>

### <span data-ttu-id="2d068-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2d068-115">-AddProtectedItem</span></span>
<span data-ttu-id="2d068-116">복구 계획 개체의 복구 계획 그룹에 추가할 ASR 복제 보호 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="2d068-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="2d068-117">-AppendGroup</span></span>
<span data-ttu-id="2d068-118">복구 계획 개체에 복구 계획 그룹을 추가 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="2d068-119">-확인</span><span class="sxs-lookup"><span data-stu-id="2d068-119">-Confirm</span></span>
<span data-ttu-id="2d068-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d068-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d068-121">-DefaultProfile</span></span>
<span data-ttu-id="2d068-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="2d068-123">-그룹</span><span class="sxs-lookup"><span data-stu-id="2d068-123">-Group</span></span>
<span data-ttu-id="2d068-124">복구 계획 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-124">Specifies a recovery plan group.</span></span>

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

### <span data-ttu-id="2d068-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d068-125">-InputObject</span></span>
<span data-ttu-id="2d068-126">편집할 ASR 복구 계획 개체입니다 (메모리 작업).</span><span class="sxs-lookup"><span data-stu-id="2d068-126">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="2d068-127">복구 계획을 업데이트 하려면 편집한 복구 계획 개체를 사용 하 여 Update-AzureRmASRRecoveryPlan를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-127">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

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

### <span data-ttu-id="2d068-128">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="2d068-128">-RemoveGroup</span></span>
<span data-ttu-id="2d068-129">복구 계획 개체에서 지정 된 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-129">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="2d068-130">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2d068-130">-RemoveProtectedItem</span></span>
<span data-ttu-id="2d068-131">복구 계획 개체의 복구 계획 그룹에서 제거할 ASR 복제 보호 된 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-131">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="2d068-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d068-132">-WhatIf</span></span>
<span data-ttu-id="2d068-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d068-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d068-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d068-135">CommonParameters</span></span>
<span data-ttu-id="2d068-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d068-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d068-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d068-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d068-138">입력</span><span class="sxs-lookup"><span data-stu-id="2d068-138">INPUTS</span></span>

### <span data-ttu-id="2d068-139">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="2d068-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="2d068-140">출력</span><span class="sxs-lookup"><span data-stu-id="2d068-140">OUTPUTS</span></span>

### <span data-ttu-id="2d068-141">System. 개체</span><span class="sxs-lookup"><span data-stu-id="2d068-141">System.Object</span></span>

## <span data-ttu-id="2d068-142">상속자</span><span class="sxs-lookup"><span data-stu-id="2d068-142">NOTES</span></span>

## <span data-ttu-id="2d068-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d068-143">RELATED LINKS</span></span>

[<span data-ttu-id="2d068-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2d068-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2d068-145">새로운 AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2d068-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
