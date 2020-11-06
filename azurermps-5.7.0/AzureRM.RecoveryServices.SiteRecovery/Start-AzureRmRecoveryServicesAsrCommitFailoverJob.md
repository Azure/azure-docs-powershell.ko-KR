---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: b491ede16973704f873e018a06ae6147df5cd06f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525007"
---
# <span data-ttu-id="f2edb-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f2edb-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="f2edb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2edb-102">SYNOPSIS</span></span>
<span data-ttu-id="f2edb-103">사이트 복구 개체에 대 한 장애 조치 커밋 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edb-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2edb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2edb-104">SYNTAX</span></span>

### <span data-ttu-id="f2edb-105">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="f2edb-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2edb-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f2edb-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2edb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f2edb-107">DESCRIPTION</span></span>
<span data-ttu-id="f2edb-108">**AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet은 장애 조치 (failover) 작업 후 Azure Site Recovery 개체에 대 한 장애 조치 (failover) 처리 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edb-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="f2edb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f2edb-109">EXAMPLES</span></span>

### <span data-ttu-id="f2edb-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2edb-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="f2edb-111">지정 된 복구 계획에 대 한 커밋 장애 조치를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edb-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f2edb-112">변수</span><span class="sxs-lookup"><span data-stu-id="f2edb-112">PARAMETERS</span></span>

### <span data-ttu-id="f2edb-113">-확인</span><span class="sxs-lookup"><span data-stu-id="f2edb-113">-Confirm</span></span>
<span data-ttu-id="f2edb-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edb-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2edb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2edb-115">-DefaultProfile</span></span>
<span data-ttu-id="f2edb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2edb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="f2edb-117">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f2edb-117">-RecoveryPlan</span></span>
<span data-ttu-id="f2edb-118">복구 계획에 해당 하는 ASR 복구 계획 개체를 failovered로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edb-118">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="f2edb-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f2edb-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f2edb-120">복제 보호 항목에 해당 하는 ASR 복제 보호 항목 개체를 failovered로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edb-120">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="f2edb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2edb-121">-WhatIf</span></span>
<span data-ttu-id="f2edb-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2edb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2edb-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2edb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2edb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2edb-124">CommonParameters</span></span>
<span data-ttu-id="f2edb-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2edb-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2edb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2edb-127">입력</span><span class="sxs-lookup"><span data-stu-id="f2edb-127">INPUTS</span></span>

### <span data-ttu-id="f2edb-128">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="f2edb-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="f2edb-129">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="f2edb-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f2edb-130">출력</span><span class="sxs-lookup"><span data-stu-id="f2edb-130">OUTPUTS</span></span>

### <span data-ttu-id="f2edb-131">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="f2edb-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f2edb-132">상속자</span><span class="sxs-lookup"><span data-stu-id="f2edb-132">NOTES</span></span>

## <span data-ttu-id="f2edb-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2edb-133">RELATED LINKS</span></span>
