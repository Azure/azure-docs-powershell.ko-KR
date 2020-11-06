---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 590512c822bd55b992c8cc58eab4091863792e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533011"
---
# <span data-ttu-id="72624-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="72624-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="72624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72624-102">SYNOPSIS</span></span>
<span data-ttu-id="72624-103">사이트 복구 개체에 대 한 장애 조치 커밋 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="72624-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72624-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72624-104">SYNTAX</span></span>

### <span data-ttu-id="72624-105">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="72624-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72624-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="72624-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72624-107">설명은</span><span class="sxs-lookup"><span data-stu-id="72624-107">DESCRIPTION</span></span>
<span data-ttu-id="72624-108">**AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet은 장애 조치 (failover) 작업 후 Azure Site Recovery 개체에 대 한 장애 조치 (failover) 처리 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="72624-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="72624-109">예제의</span><span class="sxs-lookup"><span data-stu-id="72624-109">EXAMPLES</span></span>

### <span data-ttu-id="72624-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="72624-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="72624-111">지정 된 복구 계획에 대 한 커밋 장애 조치를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="72624-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="72624-112">변수</span><span class="sxs-lookup"><span data-stu-id="72624-112">PARAMETERS</span></span>

### <span data-ttu-id="72624-113">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="72624-113">-RecoveryPlan</span></span>
<span data-ttu-id="72624-114">ASR 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72624-114">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="72624-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="72624-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="72624-116">ASR 복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72624-116">Specifies an ASR replication protected item object.</span></span>

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

### <span data-ttu-id="72624-117">-확인</span><span class="sxs-lookup"><span data-stu-id="72624-117">-Confirm</span></span>
<span data-ttu-id="72624-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72624-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72624-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72624-119">-WhatIf</span></span>
<span data-ttu-id="72624-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72624-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72624-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72624-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72624-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72624-122">CommonParameters</span></span>
<span data-ttu-id="72624-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72624-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72624-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72624-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72624-125">입력</span><span class="sxs-lookup"><span data-stu-id="72624-125">INPUTS</span></span>

### <span data-ttu-id="72624-126">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="72624-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="72624-127">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="72624-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="72624-128">출력</span><span class="sxs-lookup"><span data-stu-id="72624-128">OUTPUTS</span></span>

### <span data-ttu-id="72624-129">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="72624-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="72624-130">상속자</span><span class="sxs-lookup"><span data-stu-id="72624-130">NOTES</span></span>

## <span data-ttu-id="72624-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72624-131">RELATED LINKS</span></span>

