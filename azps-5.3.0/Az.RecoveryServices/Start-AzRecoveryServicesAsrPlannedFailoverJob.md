---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492478"
---
# <span data-ttu-id="ac156-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ac156-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="ac156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac156-102">SYNOPSIS</span></span>
<span data-ttu-id="ac156-103">계획된 장애 조치(failover) 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="ac156-104">구문</span><span class="sxs-lookup"><span data-stu-id="ac156-104">SYNTAX</span></span>

### <span data-ttu-id="ac156-105">ByRPIObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="ac156-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac156-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ac156-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac156-107">설명</span><span class="sxs-lookup"><span data-stu-id="ac156-107">DESCRIPTION</span></span>
<span data-ttu-id="ac156-108">**Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet은 Azure Site Recovery 복제 보호된 항목 또는 복구 계획에 대한 계획된 장애 조치(failover)를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="ac156-109">Get-AzRecoveryServicesAsrJob cmdlet을 사용하여 작업이 성공하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="ac156-110">예제</span><span class="sxs-lookup"><span data-stu-id="ac156-110">EXAMPLES</span></span>

### <span data-ttu-id="ac156-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ac156-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="ac156-112">지정된 ASR 복구 계획에 대해 계획된 장애 조치(failover)를 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ac156-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac156-113">PARAMETERS</span></span>

### <span data-ttu-id="ac156-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="ac156-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="ac156-115">주 지역(대체 위치 복구에 사용)으로 장애 복구하는 동안 가상 머신을 찾을 수 없는 경우 가상 머신을 생성합니다. 이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="ac156-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac156-116">예</span><span class="sxs-lookup"><span data-stu-id="ac156-116">Yes</span></span>
- <span data-ttu-id="ac156-117">아니요</span><span class="sxs-lookup"><span data-stu-id="ac156-117">No</span></span>

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

### <span data-ttu-id="ac156-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ac156-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ac156-119">기본 인증서 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="ac156-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ac156-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ac156-121">보조 인증서 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="ac156-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac156-122">-DefaultProfile</span></span>
<span data-ttu-id="ac156-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ac156-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="ac156-124">-Direction</span></span>
<span data-ttu-id="ac156-125">장애 조치(failover)의 방향을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="ac156-126">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="ac156-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac156-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ac156-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="ac156-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ac156-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="ac156-129">-Optimize</span><span class="sxs-lookup"><span data-stu-id="ac156-129">-Optimize</span></span>
<span data-ttu-id="ac156-130">최적화할 것을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="ac156-131">이 매개 변수는 Azure 사이트에서 상당한 데이터 동기화가 필요한 Azure 사이트로 장애 조치(failover)가 수행될 때 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="ac156-132">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="ac156-132">Valid values are:</span></span>

- <span data-ttu-id="ac156-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="ac156-133">ForDowntime</span></span>
- <span data-ttu-id="ac156-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="ac156-134">ForSynchronization</span></span>

<span data-ttu-id="ac156-135">**ForDowntime을** 지정하면 장애 조치(failover) 전에 데이터가 동기화되어 다운타임이 최소화됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="ac156-136">동기화는 가상 머신을 종료하지 않고 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="ac156-137">동기화가 완료되면 작업이 일시 중단됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="ac156-138">작업을 다시 시작하여 가상 머신을 종료하는 추가 동기화 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="ac156-139">**ForSynchronization을** 지정하면 데이터 동기화가 최소화되도록 장애 조치(failover) 중에만 데이터가 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="ac156-140">이 설정을 사용하도록 설정하면 가상 머신이 즉시 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="ac156-141">장애 조치(failover) 작업을 완료하기 위해 종료 후 동기화가 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="ac156-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ac156-142">-RecoveryPlan</span></span>
<span data-ttu-id="ac156-143">복구 계획에 해당하는 ASR 복구 계획 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="ac156-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ac156-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ac156-145">복제 보호된 항목에 해당하는 ASR 복제 보호 항목 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="ac156-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ac156-146">-ServicesProvider</span></span>
<span data-ttu-id="ac156-147">호스트에서 실행되는 ASR 서비스 공급자에 해당하는 ASR 서비스 공급자 개체를 지정하여 대체 위치로 장애 조치하는 동안 가상 머신을 만들 호스트를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="ac156-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac156-148">-Confirm</span></span>
<span data-ttu-id="ac156-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac156-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac156-150">-WhatIf</span></span>
<span data-ttu-id="ac156-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ac156-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac156-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac156-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac156-153">CommonParameters</span></span>
<span data-ttu-id="ac156-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ac156-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac156-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac156-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac156-156">입력</span><span class="sxs-lookup"><span data-stu-id="ac156-156">INPUTS</span></span>

### <span data-ttu-id="ac156-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ac156-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="ac156-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ac156-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ac156-159">출력</span><span class="sxs-lookup"><span data-stu-id="ac156-159">OUTPUTS</span></span>

### <span data-ttu-id="ac156-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ac156-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ac156-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac156-161">NOTES</span></span>

## <span data-ttu-id="ac156-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac156-162">RELATED LINKS</span></span>
