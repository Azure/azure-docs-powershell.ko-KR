---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: ee39fdfcb40c394bfbd7f1d804d8d9785a63f7c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873483"
---
# <span data-ttu-id="f59a9-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f59a9-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="f59a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f59a9-102">SYNOPSIS</span></span>
<span data-ttu-id="f59a9-103">계획 된 장애 조치 (failover) 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="f59a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f59a9-104">SYNTAX</span></span>

### <span data-ttu-id="f59a9-105">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="f59a9-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f59a9-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f59a9-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f59a9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f59a9-107">DESCRIPTION</span></span>
<span data-ttu-id="f59a9-108">**AzRecoveryServicesAsrPlannedFailoverJob** Cmdlet은 Azure Site Recovery 복제 보호 항목 또는 복구 계획에 대해 계획 된 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="f59a9-109">Get-AzRecoveryServicesAsrJob cmdlet을 사용 하 여 작업이 성공 하는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="f59a9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f59a9-110">EXAMPLES</span></span>

### <span data-ttu-id="f59a9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f59a9-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="f59a9-112">지정 된 ASR 복구 계획에 대해 계획 된 장애 조치를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f59a9-113">변수</span><span class="sxs-lookup"><span data-stu-id="f59a9-113">PARAMETERS</span></span>

### <span data-ttu-id="f59a9-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="f59a9-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="f59a9-115">대체 위치 복구에 사용 되는 기본 지역으로 다시 실패 하는 동안 찾지 못한 경우 가상 컴퓨터를 만듭니다. 이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f59a9-116">'</span><span class="sxs-lookup"><span data-stu-id="f59a9-116">Yes</span></span>
- <span data-ttu-id="f59a9-117">아니요</span><span class="sxs-lookup"><span data-stu-id="f59a9-117">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59a9-118">-Data Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="f59a9-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="f59a9-119">기본 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="f59a9-120">-Data Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="f59a9-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="f59a9-121">보조 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="f59a9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59a9-122">-DefaultProfile</span></span>
<span data-ttu-id="f59a9-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59a9-124">방향</span><span class="sxs-lookup"><span data-stu-id="f59a9-124">-Direction</span></span>
<span data-ttu-id="f59a9-125">장애 조치의 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="f59a9-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f59a9-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f59a9-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="f59a9-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f59a9-128">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59a9-129">-최적화</span><span class="sxs-lookup"><span data-stu-id="f59a9-129">-Optimize</span></span>
<span data-ttu-id="f59a9-130">최적화 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="f59a9-131">이 매개 변수는 실제 데이터 동기화가 필요한 Azure 사이트에서 온-프레미스 사이트로 장애 조치를 수행할 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="f59a9-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-132">Valid values are:</span></span>

- <span data-ttu-id="f59a9-133">ForDowntime 중지 시간</span><span class="sxs-lookup"><span data-stu-id="f59a9-133">ForDowntime</span></span>
- <span data-ttu-id="f59a9-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="f59a9-134">ForSynchronization</span></span>

<span data-ttu-id="f59a9-135">**Fordowntime** 지정 되 면 가동 중지 시간을 최소화 하기 위해 장애 조치 전에 데이터가 동기화 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="f59a9-136">동기화는 가상 컴퓨터를 종료 하지 않고 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="f59a9-137">동기화가 완료 되 면 작업이 일시 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="f59a9-138">작업을 다시 시작 하 여 가상 컴퓨터를 종료 하는 추가 동기화 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="f59a9-139">**Forsynchronization** 이 지정 된 경우 데이터 동기화가 최소화 될 때만 데이터가 장애 조치 중에 동기화 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="f59a9-140">이 설정을 사용 하도록 설정 하면 가상 컴퓨터가 즉시 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="f59a9-141">장애 조치 작업을 완료 하기 위해 종료 후 동기화가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59a9-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f59a9-142">-RecoveryPlan</span></span>
<span data-ttu-id="f59a9-143">장애 조치 복구 계획에 해당 하는 ASR 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="f59a9-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f59a9-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f59a9-145">장애 조치를 위해 복제 보호 항목에 해당 하는 ASR 복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="f59a9-146">-서비스 공급자</span><span class="sxs-lookup"><span data-stu-id="f59a9-146">-ServicesProvider</span></span>
<span data-ttu-id="f59a9-147">호스트에서 실행 되는 ASR services 공급자에 해당 하는 ASR services 공급자 개체를 지정 하 여 대체 위치로 장애 조치 하는 동안 가상 컴퓨터를 만들 호스트를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59a9-148">-확인</span><span class="sxs-lookup"><span data-stu-id="f59a9-148">-Confirm</span></span>
<span data-ttu-id="f59a9-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f59a9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f59a9-150">-WhatIf</span></span>
<span data-ttu-id="f59a9-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f59a9-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f59a9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59a9-153">CommonParameters</span></span>
<span data-ttu-id="f59a9-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59a9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59a9-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f59a9-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59a9-156">입력</span><span class="sxs-lookup"><span data-stu-id="f59a9-156">INPUTS</span></span>

### <span data-ttu-id="f59a9-157">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="f59a9-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="f59a9-158">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="f59a9-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f59a9-159">출력</span><span class="sxs-lookup"><span data-stu-id="f59a9-159">OUTPUTS</span></span>

### <span data-ttu-id="f59a9-160">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="f59a9-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f59a9-161">상속자</span><span class="sxs-lookup"><span data-stu-id="f59a9-161">NOTES</span></span>

## <span data-ttu-id="f59a9-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f59a9-162">RELATED LINKS</span></span>
