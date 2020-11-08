---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045751"
---
# <span data-ttu-id="e0d7a-101">Start-AzureSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e0d7a-101">Start-AzureSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="e0d7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d7a-103">사이트 복구 계획 장애 조치 (failover) 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-103">Starts a Site Recovery planned failover operation.</span></span>

## <span data-ttu-id="e0d7a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0d7a-104">SYNTAX</span></span>

### <span data-ttu-id="e0d7a-105">ByRPId (기본값)</span><span class="sxs-lookup"><span data-stu-id="e0d7a-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e0d7a-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="e0d7a-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e0d7a-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e0d7a-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e0d7a-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="e0d7a-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0d7a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e0d7a-109">DESCRIPTION</span></span>
<span data-ttu-id="e0d7a-110">**AzureSiteRecoveryPlannedFailoverJob** Cmdlet은 Azure Site Recovery 보호 엔터티 또는 복구 계획에 대해 계획 된 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-110">The **Start-AzureSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="e0d7a-111">**AzureSiteRecoveryJob** cmdlet을 사용 하 여 작업이 성공 하는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="e0d7a-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e0d7a-112">EXAMPLES</span></span>

### <span data-ttu-id="e0d7a-113">예제 1: 계획 된 장애 조치 작업 시작</span><span class="sxs-lookup"><span data-stu-id="e0d7a-113">Example 1: Start a planned failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="e0d7a-114">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에서 보호 된 모든 컨테이너를 가져온 다음 결과를 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-114">The first command gets all protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>
<span data-ttu-id="e0d7a-115">이 예제에는 하나의 컨테이너가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-115">In this example, there is a single container.</span></span>

<span data-ttu-id="e0d7a-116">두 번째 명령은 **AzureSiteRecoveryProtectionEntity** cmdlet을 사용 하 여 $Container에 저장 된 컨테이너에 속하는 보호 된 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-116">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="e0d7a-117">명령이 $Protected 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-117">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="e0d7a-118">마지막 명령은 $Protected에 저장 된 보호 된 가상 머신에 대 한 PrimaryToRecovery 방향으로 장애 조치 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-118">The final command starts the failover job in the direction PrimaryToRecovery for the protected virtual machines stored in $Protected.</span></span>

## <span data-ttu-id="e0d7a-119">변수</span><span class="sxs-lookup"><span data-stu-id="e0d7a-119">PARAMETERS</span></span>

### <span data-ttu-id="e0d7a-120">방향</span><span class="sxs-lookup"><span data-stu-id="e0d7a-120">-Direction</span></span>
<span data-ttu-id="e0d7a-121">장애 조치의 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-121">Specifies the direction of the failover.</span></span>
<span data-ttu-id="e0d7a-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e0d7a-123">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e0d7a-123">PrimaryToRecovery</span></span>
- <span data-ttu-id="e0d7a-124">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e0d7a-124">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d7a-125">-최적화</span><span class="sxs-lookup"><span data-stu-id="e0d7a-125">-Optimize</span></span>
<span data-ttu-id="e0d7a-126">최적화 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-126">Specifies what to optimize for.</span></span>
<span data-ttu-id="e0d7a-127">이 매개 변수는 중요 한 데이터 동기화가 필요한 Azure 사이트에서 온-프레미스 사이트로의 장애 조치에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-127">This parameter applies for failover from an Azure site to an on-premise site which requires a significant data synchronization.</span></span>
<span data-ttu-id="e0d7a-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e0d7a-129">ForDowntime 중지 시간</span><span class="sxs-lookup"><span data-stu-id="e0d7a-129">ForDowntime</span></span>
- <span data-ttu-id="e0d7a-130">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="e0d7a-130">ForSynchronization</span></span>

<span data-ttu-id="e0d7a-131">**Fordowntime** 지정 되 면 가동 중지 시간을 최소화 하기 위해 장애 조치 전에 데이터가 동기화 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-131">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="e0d7a-132">동기화는 가상 컴퓨터를 종료 하지 않고 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-132">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="e0d7a-133">동기화가 완료 되 면 작업이 일시 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-133">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="e0d7a-134">작업을 다시 시작 하 여 가상 컴퓨터를 종료 하는 추가 동기화 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-134">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="e0d7a-135">**Forsynchronization** 이 지정 된 경우 데이터 동기화가 최소화 될 때만 데이터가 장애 조치 중에 동기화 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-135">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="e0d7a-136">이 설정을 사용 하도록 설정 하면 가상 컴퓨터가 즉시 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-136">Because this setting is enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="e0d7a-137">장애 조치 작업을 완료 하기 위해 종료 후 동기화가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-137">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="e0d7a-138">-프로필</span><span class="sxs-lookup"><span data-stu-id="e0d7a-138">-Profile</span></span>
<span data-ttu-id="e0d7a-139">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0d7a-140">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d7a-141">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="e0d7a-141">-ProtectionContainerId</span></span>
<span data-ttu-id="e0d7a-142">작업을 시작할 보호 된 컨테이너의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-142">Specifies the ID of the protected container for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d7a-143">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e0d7a-143">-ProtectionEntity</span></span>
<span data-ttu-id="e0d7a-144">사이트 복구 보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-144">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d7a-145">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="e0d7a-145">-ProtectionEntityId</span></span>
<span data-ttu-id="e0d7a-146">작업을 시작할 **ASRProtectionEntity** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-146">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="e0d7a-147">**ASRProtectionEntity** 개체를 얻으려면 **Get-AzureSiteRecoveryProtectionEntity** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-147">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d7a-148">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e0d7a-148">-RecoveryPlan</span></span>
<span data-ttu-id="e0d7a-149">복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-149">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="e0d7a-150">-RPId</span><span class="sxs-lookup"><span data-stu-id="e0d7a-150">-RPId</span></span>
<span data-ttu-id="e0d7a-151">작업을 시작할 복구 계획의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-151">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d7a-152">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e0d7a-152">-WaitForCompletion</span></span>
<span data-ttu-id="e0d7a-153">Cmdlet이 Windows PowerShell 콘솔에 제어를 반환 하기 전에 작업이 완료 될 때까지 대기 하 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-153">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d7a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d7a-154">CommonParameters</span></span>
<span data-ttu-id="e0d7a-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d7a-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0d7a-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d7a-157">입력</span><span class="sxs-lookup"><span data-stu-id="e0d7a-157">INPUTS</span></span>

## <span data-ttu-id="e0d7a-158">출력</span><span class="sxs-lookup"><span data-stu-id="e0d7a-158">OUTPUTS</span></span>

## <span data-ttu-id="e0d7a-159">상속자</span><span class="sxs-lookup"><span data-stu-id="e0d7a-159">NOTES</span></span>

## <span data-ttu-id="e0d7a-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0d7a-160">RELATED LINKS</span></span>

[<span data-ttu-id="e0d7a-161">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e0d7a-161">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="e0d7a-162">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e0d7a-162">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


