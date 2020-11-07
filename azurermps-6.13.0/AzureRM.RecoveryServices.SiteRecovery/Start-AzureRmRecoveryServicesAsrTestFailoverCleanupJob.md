---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 5d99c9cad96a3f0c4fb877ecd15f8450eb89c4fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702099"
---
# <span data-ttu-id="c2b85-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="c2b85-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="c2b85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2b85-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b85-103">테스트 장애 조치 정리 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-103">Starts the test failover cleanup operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2b85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2b85-104">SYNTAX</span></span>

### <span data-ttu-id="c2b85-105">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2b85-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b85-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2b85-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b85-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c2b85-107">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2b85-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c2b85-108">DESCRIPTION</span></span>
<span data-ttu-id="c2b85-109">**AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet은 테스트 장애 조치를 수행한 복제 보호 항목 또는 복구 계획에서 장애 조치 (failover) 정리 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="c2b85-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c2b85-110">EXAMPLES</span></span>

### <span data-ttu-id="c2b85-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2b85-111">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="c2b85-112">Azure Site Recovery 복제 보호 항목의 테스트 장애 조치 정리를 추적 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="c2b85-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c2b85-113">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="c2b85-114">Azure Site Recovery recoveryPlan의 테스트 장애 조치 정리를 추적 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="c2b85-115">변수</span><span class="sxs-lookup"><span data-stu-id="c2b85-115">PARAMETERS</span></span>

### <span data-ttu-id="c2b85-116">-메모</span><span class="sxs-lookup"><span data-stu-id="c2b85-116">-Comment</span></span>
<span data-ttu-id="c2b85-117">테스트 장애 조치에 대 한 사용자 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-117">User Comment for Test Failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b85-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b85-118">-DefaultProfile</span></span>
<span data-ttu-id="c2b85-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2b85-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c2b85-120">-RecoveryPlan</span></span>
<span data-ttu-id="c2b85-121">장애 조치 (failover) 정리 테스트를 수행 하는 복구 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-121">Recovery Plan to perform the test failover cleanup on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b85-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c2b85-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c2b85-123">복제 보호 항목에서 테스트 장애 조치 정리를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b85-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2b85-124">-ResourceId</span></span>
<span data-ttu-id="c2b85-125">Cleanon 테스트 장애 조치를 위해 복제 보호 항목의 리소스 Id/복구 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b85-126">-확인</span><span class="sxs-lookup"><span data-stu-id="c2b85-126">-Confirm</span></span>
<span data-ttu-id="c2b85-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b85-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b85-128">-WhatIf</span></span>
<span data-ttu-id="c2b85-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2b85-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b85-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b85-131">CommonParameters</span></span>
<span data-ttu-id="c2b85-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b85-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b85-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b85-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b85-134">입력</span><span class="sxs-lookup"><span data-stu-id="c2b85-134">INPUTS</span></span>

### <span data-ttu-id="c2b85-135">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="c2b85-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="c2b85-136">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="c2b85-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c2b85-137">출력</span><span class="sxs-lookup"><span data-stu-id="c2b85-137">OUTPUTS</span></span>

### <span data-ttu-id="c2b85-138">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="c2b85-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c2b85-139">상속자</span><span class="sxs-lookup"><span data-stu-id="c2b85-139">NOTES</span></span>

## <span data-ttu-id="c2b85-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2b85-140">RELATED LINKS</span></span>
