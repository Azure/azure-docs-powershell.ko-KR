---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/edit-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8c078c97a1531863979b6182867e8900550b68b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533615"
---
# <span data-ttu-id="86f70-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="86f70-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="86f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86f70-102">SYNOPSIS</span></span>
<span data-ttu-id="86f70-103">사이트 복구 계획을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f70-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86f70-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86f70-104">SYNTAX</span></span>

### <span data-ttu-id="86f70-105">AppendGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="86f70-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86f70-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="86f70-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86f70-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="86f70-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86f70-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="86f70-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86f70-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="86f70-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86f70-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="86f70-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86f70-111">설명은</span><span class="sxs-lookup"><span data-stu-id="86f70-111">DESCRIPTION</span></span>
<span data-ttu-id="86f70-112">**편집-AzureRmSiteRecoveryRecoveryPlan** Cmdlet은 Azure Site Recovery 계획을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f70-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="86f70-113">예제의</span><span class="sxs-lookup"><span data-stu-id="86f70-113">EXAMPLES</span></span>

## <span data-ttu-id="86f70-114">변수</span><span class="sxs-lookup"><span data-stu-id="86f70-114">PARAMETERS</span></span>

### <span data-ttu-id="86f70-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="86f70-115">-AddProtectedEntities</span></span>
<span data-ttu-id="86f70-116">추가할 보호 된 엔터티의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f70-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f70-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="86f70-117">-AddProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f70-118">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="86f70-118">-AppendGroup</span></span>
<span data-ttu-id="86f70-119">이 작업이 복구 계획 개체에 그룹을 추가 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="86f70-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

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

### <span data-ttu-id="86f70-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f70-120">-DefaultProfile</span></span>
<span data-ttu-id="86f70-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86f70-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86f70-122">-그룹</span><span class="sxs-lookup"><span data-stu-id="86f70-122">-Group</span></span>
<span data-ttu-id="86f70-123">사이트 복구 계획 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f70-123">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f70-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="86f70-124">-RecoveryPlan</span></span>
<span data-ttu-id="86f70-125">복구 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f70-125">Specifies a recovery plan.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86f70-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="86f70-126">-RemoveGroup</span></span>
<span data-ttu-id="86f70-127">지정 된 사이트 복구 복구 계획 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f70-127">Removes the specified Site Recovery recovery plan group.</span></span>

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

### <span data-ttu-id="86f70-128">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="86f70-128">-RemoveProtectedEntities</span></span>
<span data-ttu-id="86f70-129">보호 되는 엔터티의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f70-129">Specifies an array of protected entities.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f70-130">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="86f70-130">-RemoveProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f70-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f70-131">CommonParameters</span></span>
<span data-ttu-id="86f70-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f70-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f70-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86f70-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f70-134">입력</span><span class="sxs-lookup"><span data-stu-id="86f70-134">INPUTS</span></span>

### <span data-ttu-id="86f70-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="86f70-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="86f70-136">' RecoveryPlan ' 매개 변수는 파이프라인에서 ' ASRRecoveryPlan ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f70-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="86f70-137">출력</span><span class="sxs-lookup"><span data-stu-id="86f70-137">OUTPUTS</span></span>

## <span data-ttu-id="86f70-138">상속자</span><span class="sxs-lookup"><span data-stu-id="86f70-138">NOTES</span></span>

## <span data-ttu-id="86f70-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86f70-139">RELATED LINKS</span></span>

[<span data-ttu-id="86f70-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="86f70-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="86f70-141">새로운 AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="86f70-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
