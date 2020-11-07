---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: afa5da5a34954c1e1a610ce9153172934069c2a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703646"
---
# <span data-ttu-id="64802-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="64802-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="64802-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64802-102">SYNOPSIS</span></span>
<span data-ttu-id="64802-103">지정 된 복제 보호 항목 또는 복구 계획에 대 한 복제 방향을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="64802-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="64802-104">복제 된 항목 또는 복구 계획을 통해 장애를 다시 방지 하거나 역 복제 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64802-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64802-105">구문과</span><span class="sxs-lookup"><span data-stu-id="64802-105">SYNTAX</span></span>

### <span data-ttu-id="64802-106">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="64802-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64802-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="64802-107">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64802-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="64802-108">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64802-109">설명은</span><span class="sxs-lookup"><span data-stu-id="64802-109">DESCRIPTION</span></span>
<span data-ttu-id="64802-110">**AzureRmRecoveryServicesAsrProtectionDirection** cmdlet은 커밋 장애 조치 작업이 완료 된 후 지정 된 Azure Site Recovery 개체의 복제 방향을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="64802-110">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="64802-111">예제의</span><span class="sxs-lookup"><span data-stu-id="64802-111">EXAMPLES</span></span>

### <span data-ttu-id="64802-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="64802-112">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="64802-113">지정 된 recoveyr 계획에 대 한 방향 업데이트 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="64802-113">Start the update direction operation for the specified recoveyr plan and returns the ASR job object used to track the operation.</span></span>

## <span data-ttu-id="64802-114">변수</span><span class="sxs-lookup"><span data-stu-id="64802-114">PARAMETERS</span></span>

### <span data-ttu-id="64802-115">방향</span><span class="sxs-lookup"><span data-stu-id="64802-115">-Direction</span></span>
<span data-ttu-id="64802-116">업데이트 작업에 대해 장애 조치를 게시 하는 데 사용할 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64802-116">Specifies the direction to be used for the update operation post a failover.</span></span>  
<span data-ttu-id="64802-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64802-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64802-118">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="64802-118">PrimaryToRecovery</span></span>
- <span data-ttu-id="64802-119">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="64802-119">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64802-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64802-120">-RecoveryPlan</span></span>
<span data-ttu-id="64802-121">ASR 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64802-121">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64802-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="64802-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="64802-123">ASR 복제 보호 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64802-123">Specifies an ASR replication protected item</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64802-124">-확인</span><span class="sxs-lookup"><span data-stu-id="64802-124">-Confirm</span></span>
<span data-ttu-id="64802-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="64802-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64802-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64802-126">-WhatIf</span></span>
<span data-ttu-id="64802-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64802-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64802-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64802-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64802-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64802-129">CommonParameters</span></span>
<span data-ttu-id="64802-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64802-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64802-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64802-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64802-132">입력</span><span class="sxs-lookup"><span data-stu-id="64802-132">INPUTS</span></span>

### <span data-ttu-id="64802-133">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="64802-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="64802-134">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="64802-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="64802-135">출력</span><span class="sxs-lookup"><span data-stu-id="64802-135">OUTPUTS</span></span>

### <span data-ttu-id="64802-136">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="64802-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="64802-137">상속자</span><span class="sxs-lookup"><span data-stu-id="64802-137">NOTES</span></span>

## <span data-ttu-id="64802-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64802-138">RELATED LINKS</span></span>

