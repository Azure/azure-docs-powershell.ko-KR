---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: f60da52bffcc78e563863c79971beea8d45e398e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531965"
---
# <span data-ttu-id="7b238-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7b238-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="7b238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b238-102">SYNOPSIS</span></span>
<span data-ttu-id="7b238-103">사이트 복구 계획을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b238-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b238-104">SYNTAX</span></span>

### <span data-ttu-id="7b238-105">AppendGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="7b238-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b238-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="7b238-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b238-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="7b238-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b238-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="7b238-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b238-109">설명은</span><span class="sxs-lookup"><span data-stu-id="7b238-109">DESCRIPTION</span></span>
<span data-ttu-id="7b238-110">**편집-AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet은 Azure Site Recovery 계획을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="7b238-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7b238-111">EXAMPLES</span></span>

### <span data-ttu-id="7b238-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7b238-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="7b238-113">기존 Azure Site Recovery 복구 계획에 그룹을 추가 하 고 메모리 내 업데이트 복구 계획을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="7b238-114">변수</span><span class="sxs-lookup"><span data-stu-id="7b238-114">PARAMETERS</span></span>

### <span data-ttu-id="7b238-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7b238-115">-AddProtectedItem</span></span>
<span data-ttu-id="7b238-116">복구 계획 개체의 복구 계획 그룹에 추가할 ASR 복제 보호 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b238-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="7b238-117">-AppendGroup</span></span>
<span data-ttu-id="7b238-118">복구 계획 개체에 복구 계획 그룹을 추가 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b238-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b238-119">-DefaultProfile</span></span>
<span data-ttu-id="7b238-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7b238-121">-그룹</span><span class="sxs-lookup"><span data-stu-id="7b238-121">-Group</span></span>
<span data-ttu-id="7b238-122">복구 계획 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-122">Specifies a recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b238-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b238-123">-InputObject</span></span>
<span data-ttu-id="7b238-124">편집할 ASR 복구 계획 개체입니다 (메모리 작업).</span><span class="sxs-lookup"><span data-stu-id="7b238-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="7b238-125">복구 계획을 업데이트 하려면 편집한 복구 계획 개체를 사용 하 여 Update-AzureRmASRRecoveryPlan를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-125">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b238-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="7b238-126">-RemoveGroup</span></span>
<span data-ttu-id="7b238-127">복구 계획 개체에서 지정 된 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-127">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b238-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7b238-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="7b238-129">복구 계획 개체의 복구 계획 그룹에서 제거할 ASR 복제 보호 된 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b238-130">-확인</span><span class="sxs-lookup"><span data-stu-id="7b238-130">-Confirm</span></span>
<span data-ttu-id="7b238-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b238-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b238-132">-WhatIf</span></span>
<span data-ttu-id="7b238-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b238-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b238-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b238-135">CommonParameters</span></span>
<span data-ttu-id="7b238-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b238-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b238-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b238-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b238-138">입력</span><span class="sxs-lookup"><span data-stu-id="7b238-138">INPUTS</span></span>

### <span data-ttu-id="7b238-139">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="7b238-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="7b238-140">출력</span><span class="sxs-lookup"><span data-stu-id="7b238-140">OUTPUTS</span></span>

### <span data-ttu-id="7b238-141">System. 개체</span><span class="sxs-lookup"><span data-stu-id="7b238-141">System.Object</span></span>

## <span data-ttu-id="7b238-142">상속자</span><span class="sxs-lookup"><span data-stu-id="7b238-142">NOTES</span></span>

## <span data-ttu-id="7b238-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b238-143">RELATED LINKS</span></span>

[<span data-ttu-id="7b238-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7b238-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="7b238-145">새로운 AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7b238-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
