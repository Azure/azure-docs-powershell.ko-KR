---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 0d619084f62f4cad9b5bd7a9295987681994e53e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703652"
---
# <span data-ttu-id="70d8b-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="70d8b-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="70d8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="70d8b-103">계획 되지 않은 장애 조치 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-103">Starts an unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70d8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70d8b-104">SYNTAX</span></span>

### <span data-ttu-id="70d8b-105">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="70d8b-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70d8b-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="70d8b-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70d8b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="70d8b-107">DESCRIPTION</span></span>
<span data-ttu-id="70d8b-108">**AzureRmRecoveryServicesAsrUnplannedFailoverJob** Cmdlet은 Azure Site Recovery 복제 보호 항목 또는 복구 계획의 계획 되지 않은 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-108">The **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="70d8b-109">Get-AzureRmRecoveryServicesAsrJob cmdlet을 사용 하 여 작업이 성공 하는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="70d8b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="70d8b-110">EXAMPLES</span></span>

### <span data-ttu-id="70d8b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="70d8b-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="70d8b-112">지정 된 매개 변수를 사용 하 여 지정 된 복구 계획에 대해 계획 되지 않은 장애 조치 작업을 시작 하 고 작업 추적에 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-112">Starts the unplanned failover operation for the specified recovery plan using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="70d8b-113">변수</span><span class="sxs-lookup"><span data-stu-id="70d8b-113">PARAMETERS</span></span>

### <span data-ttu-id="70d8b-114">-Data Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="70d8b-114">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="70d8b-115">기본 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-115">Specifies the primary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d8b-116">-Data Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="70d8b-116">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="70d8b-117">보조 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-117">Specifies the secondary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d8b-118">방향</span><span class="sxs-lookup"><span data-stu-id="70d8b-118">-Direction</span></span>
<span data-ttu-id="70d8b-119">장애 조치의 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="70d8b-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70d8b-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="70d8b-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="70d8b-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="70d8b-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="70d8b-123">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="70d8b-123">-PerformSourceSideAction</span></span>
<span data-ttu-id="70d8b-124">복구 계획에 지정 된 모든 원본 사이트 작업을 장애 조치의 일부로 수행 하도록 시도 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-124">Indicates that any source site operations specified in the recovery plan must be attempted to be performed as part of the fail over.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d8b-125">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="70d8b-125">-RecoveryPlan</span></span>
<span data-ttu-id="70d8b-126">장애 조치 (failover) 작업을 수행할 복구 계획에 해당 하는 ASR 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-126">Specifies an ASR recovery plan object corresponding to the recovery plan on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="70d8b-127">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="70d8b-127">-ReplicationProtectedItem</span></span>
<span data-ttu-id="70d8b-128">장애 조치 (failover) 작업을 수행할 복제 보호 항목에 해당 하는 ASR 복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-128">Specifies the ASR replication protected item object corresponding to the replication protected item on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="70d8b-129">-확인</span><span class="sxs-lookup"><span data-stu-id="70d8b-129">-Confirm</span></span>
<span data-ttu-id="70d8b-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70d8b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70d8b-131">-WhatIf</span></span>
<span data-ttu-id="70d8b-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70d8b-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70d8b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d8b-134">CommonParameters</span></span>
<span data-ttu-id="70d8b-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d8b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d8b-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70d8b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d8b-137">입력</span><span class="sxs-lookup"><span data-stu-id="70d8b-137">INPUTS</span></span>

### <span data-ttu-id="70d8b-138">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="70d8b-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="70d8b-139">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="70d8b-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="70d8b-140">출력</span><span class="sxs-lookup"><span data-stu-id="70d8b-140">OUTPUTS</span></span>

### <span data-ttu-id="70d8b-141">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="70d8b-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="70d8b-142">상속자</span><span class="sxs-lookup"><span data-stu-id="70d8b-142">NOTES</span></span>

## <span data-ttu-id="70d8b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70d8b-143">RELATED LINKS</span></span>

[<span data-ttu-id="70d8b-144">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="70d8b-144">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)


