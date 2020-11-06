---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 08e864c3d95c4d077e4d9e1227a0ec606508c193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529106"
---
# <span data-ttu-id="b46e4-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="b46e4-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="b46e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b46e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b46e4-103">사이트 복구 개체에 대 한 장애 조치 커밋 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b46e4-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b46e4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b46e4-104">SYNTAX</span></span>

### <span data-ttu-id="b46e4-105">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="b46e4-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b46e4-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="b46e4-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b46e4-107">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="b46e4-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b46e4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b46e4-108">DESCRIPTION</span></span>
<span data-ttu-id="b46e4-109">**AzureRmSiteRecoveryCommitFailoverJob** cmdlet은 장애 조치 (failover) 작업 후 Azure Site Recovery 개체에 대 한 장애 조치 (failover) 처리 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b46e4-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="b46e4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b46e4-110">EXAMPLES</span></span>

## <span data-ttu-id="b46e4-111">변수</span><span class="sxs-lookup"><span data-stu-id="b46e4-111">PARAMETERS</span></span>

### <span data-ttu-id="b46e4-112">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b46e4-112">-ProtectionEntity</span></span>
<span data-ttu-id="b46e4-113">사이트 복구 보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b46e4-113">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b46e4-114">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b46e4-114">-RecoveryPlan</span></span>
<span data-ttu-id="b46e4-115">복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b46e4-115">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b46e4-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b46e4-116">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b46e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b46e4-117">-DefaultProfile</span></span>
<span data-ttu-id="b46e4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b46e4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b46e4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b46e4-119">CommonParameters</span></span>
<span data-ttu-id="b46e4-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b46e4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b46e4-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b46e4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b46e4-122">입력</span><span class="sxs-lookup"><span data-stu-id="b46e4-122">INPUTS</span></span>

### <span data-ttu-id="b46e4-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b46e4-123">ASRProtectionEntity</span></span>
<span data-ttu-id="b46e4-124">' ProtectionEntity ' 매개 변수는 파이프라인에서 ' ASRProtectionEntity ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b46e4-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="b46e4-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b46e4-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="b46e4-126">' RecoveryPlan ' 매개 변수는 파이프라인에서 ' ASRRecoveryPlan ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b46e4-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="b46e4-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b46e4-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="b46e4-128">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b46e4-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="b46e4-129">출력</span><span class="sxs-lookup"><span data-stu-id="b46e4-129">OUTPUTS</span></span>

### <span data-ttu-id="b46e4-130">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="b46e4-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b46e4-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b46e4-131">NOTES</span></span>

## <span data-ttu-id="b46e4-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b46e4-132">RELATED LINKS</span></span>

