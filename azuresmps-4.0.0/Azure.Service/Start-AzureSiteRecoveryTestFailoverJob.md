---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 9AE41884-C39F-4AEB-8030-96167F98C8DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b46cc27b2e5380f3cb533a4355a94170e941cd8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046028"
---
# <span data-ttu-id="7e2e7-101">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="7e2e7-101">Start-AzureSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="7e2e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="7e2e7-103">사이트 복구 보호 엔터티에 대 한 테스트 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-103">Starts a test failover for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="7e2e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e2e7-104">SYNTAX</span></span>

### <span data-ttu-id="7e2e7-105">ByPEId (기본값)</span><span class="sxs-lookup"><span data-stu-id="7e2e7-105">ByPEId (Default)</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="7e2e7-106">ByRPId</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-107">ByRPIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="7e2e7-107">ByRPIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-108">ByRPIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="7e2e7-108">ByRPIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-109">ByRPIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="7e2e7-109">ByRPIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> -Network <ASRNetwork> [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-110">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="7e2e7-110">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-111">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="7e2e7-111">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-112">ByPEIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="7e2e7-112">ByPEIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="7e2e7-113">ByRPObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-114">ByRPObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="7e2e7-114">ByRPObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-115">ByRPObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="7e2e7-115">ByRPObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-116">ByPEIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="7e2e7-116">ByPEIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-117">ByPEIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="7e2e7-117">ByPEIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-118">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="7e2e7-118">ByPEObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-119">ByPEObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="7e2e7-119">ByPEObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7e2e7-120">ByPEObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="7e2e7-120">ByPEObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e2e7-121">설명은</span><span class="sxs-lookup"><span data-stu-id="7e2e7-121">DESCRIPTION</span></span>
<span data-ttu-id="7e2e7-122">**AzureSiteRecoveryTestFailoverJob** Cmdlet은 Azure Site Recovery 보호 엔터티 또는 복구 계획의 장애 조치 테스트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-122">The **Start-AzureSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="7e2e7-123">**AzureRMSiteRecoveryJob** cmdlet을 사용 하 여 작업이 성공 했는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-123">You can check whether the job succeeded by using the **Get-AzureRMSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="7e2e7-124">예제의</span><span class="sxs-lookup"><span data-stu-id="7e2e7-124">EXAMPLES</span></span>

### <span data-ttu-id="7e2e7-125">예제 1: 테스트 장애 조치 시작</span><span class="sxs-lookup"><span data-stu-id="7e2e7-125">Example 1: Start a test failover</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer
PS C:\> Start-AzureSiteRecoveryTestFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="7e2e7-126">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 protected 컨테이너를 얻은 다음 $ProtectionContainer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-126">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="7e2e7-127">두 번째 명령은 **AzureSiteRecoveryProtectionEntity** cmdlet을 사용 하 여 $ProtectionContainer에 저장 된 보호 컨테이너에 속하는 보호 되는 엔터티를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-127">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="7e2e7-128">명령이 $ProtectionEntity 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-128">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="7e2e7-129">마지막 명령은 $ProtectionEntity에 저장 된 보호 되는 엔터티에 대해 테스트 장애 조치 (failover) 작업을 시작 하 고 장애 조치 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-129">The final command starts the test failover operation for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

### <span data-ttu-id="7e2e7-130">예제 2: 복구 계획을 사용 하 여 테스트 장애 조치 시작</span><span class="sxs-lookup"><span data-stu-id="7e2e7-130">Example 2: Start a test failover using a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan -Name "RecoveryPlan01"
Start-AzureSiteRecoveryTestFailoverJob -Direction PrimaryToRecovery -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="7e2e7-131">이 명령은 **AzureSiteRecoveryRecoveryPlan** cmdlet을 사용 하 여 현재 Azure Site recovery 자격 증명 모음에 대 한 RecoveryPlan01 라는 복구 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-131">This command gets the recovery plan named RecoveryPlan01 for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>
<span data-ttu-id="7e2e7-132">명령이 $RecoveryPlan 변수에 계획을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-132">The command stores the plan in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="7e2e7-133">두 번째 명령은 $RecoveryPlan에 저장 된 복구 계획에 대 한 테스트 장애 조치 (failover) 작업을 시작 하 고 장애 조치 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-133">The second command starts the test failover operation for the recovery plan stored in $RecoveryPlan and specifies the direction of the failover.</span></span>

## <span data-ttu-id="7e2e7-134">변수</span><span class="sxs-lookup"><span data-stu-id="7e2e7-134">PARAMETERS</span></span>

### <span data-ttu-id="7e2e7-135">방향</span><span class="sxs-lookup"><span data-stu-id="7e2e7-135">-Direction</span></span>
<span data-ttu-id="7e2e7-136">장애 조치 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-136">Specifies the failover direction.</span></span>
<span data-ttu-id="7e2e7-137">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e2e7-138">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="7e2e7-138">PrimaryToRecovery</span></span>
- <span data-ttu-id="7e2e7-139">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="7e2e7-139">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="7e2e7-140">-LogicalNetworkId</span><span class="sxs-lookup"><span data-stu-id="7e2e7-140">-LogicalNetworkId</span></span>
<span data-ttu-id="7e2e7-141">논리 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-141">Specifies the ID of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithLogicalNetworkID, ByRPObjectWithLogicalNetworkID, ByPEIdWithLogicalNetworkID, ByPEObjectWithLogicalNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2e7-142">-네트워크</span><span class="sxs-lookup"><span data-stu-id="7e2e7-142">-Network</span></span>
<span data-ttu-id="7e2e7-143">테스트 장애 조치에 사용할 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-143">Specifies the network object to use for test failover.</span></span>
<span data-ttu-id="7e2e7-144">네트워크를 얻으려면 **AzureSiteRecoveryNetwork** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-144">To obtain a network, use the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByPEId, ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPObject, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID, ByPEObject, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRNetwork
Parameter Sets: ByRPIdWithVMNetwork, ByPEObjectWithVMNetwork, ByRPObjectWithVMNetwork, ByPEIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2e7-145">-NetworkType</span><span class="sxs-lookup"><span data-stu-id="7e2e7-145">-NetworkType</span></span>
<span data-ttu-id="7e2e7-146">테스트 장애 조치에 사용할 네트워크 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-146">Specifies the network type to use for test failover.</span></span>
<span data-ttu-id="7e2e7-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e2e7-148">않아야</span><span class="sxs-lookup"><span data-stu-id="7e2e7-148">None</span></span>
- <span data-ttu-id="7e2e7-149">새로운</span><span class="sxs-lookup"><span data-stu-id="7e2e7-149">New</span></span>
- <span data-ttu-id="7e2e7-150">존재</span><span class="sxs-lookup"><span data-stu-id="7e2e7-150">Existing</span></span>

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

### <span data-ttu-id="7e2e7-151">-프로필</span><span class="sxs-lookup"><span data-stu-id="7e2e7-151">-Profile</span></span>
<span data-ttu-id="7e2e7-152">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7e2e7-153">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e2e7-154">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="7e2e7-154">-ProtectionContainerId</span></span>
<span data-ttu-id="7e2e7-155">보호 된 컨테이너의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-155">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="7e2e7-156">이 cmdlet은이 cmdlet에서 지정 하는 컨테이너에 속하는 보호 된 가상 컴퓨터에 대 한 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-156">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2e7-157">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7e2e7-157">-ProtectionEntity</span></span>
<span data-ttu-id="7e2e7-158">사이트 복구 보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-158">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObjectWithVMNetwork, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2e7-159">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="7e2e7-159">-ProtectionEntityId</span></span>
<span data-ttu-id="7e2e7-160">작업을 시작할 보호 된 가상 컴퓨터의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-160">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2e7-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7e2e7-161">-RecoveryPlan</span></span>
<span data-ttu-id="7e2e7-162">작업을 시작할 복구 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-162">Specifies a recovery plan for which to start the job.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObjectWithVMNetwork, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2e7-163">-RpId</span><span class="sxs-lookup"><span data-stu-id="7e2e7-163">-RpId</span></span>
<span data-ttu-id="7e2e7-164">작업을 시작할 복구 계획의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-164">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2e7-165">-VmNetworkId</span><span class="sxs-lookup"><span data-stu-id="7e2e7-165">-VmNetworkId</span></span>
<span data-ttu-id="7e2e7-166">가상 컴퓨터 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-166">Specifies the ID of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithVMNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithVMNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2e7-167">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7e2e7-167">-WaitForCompletion</span></span>
<span data-ttu-id="7e2e7-168">Cmdlet이 Windows PowerShell 콘솔에 제어를 반환 하기 전에 작업이 완료 될 때까지 대기 하 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-168">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="7e2e7-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e2e7-169">CommonParameters</span></span>
<span data-ttu-id="7e2e7-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2e7-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e2e7-171">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e2e7-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e2e7-172">입력</span><span class="sxs-lookup"><span data-stu-id="7e2e7-172">INPUTS</span></span>

## <span data-ttu-id="7e2e7-173">출력</span><span class="sxs-lookup"><span data-stu-id="7e2e7-173">OUTPUTS</span></span>

## <span data-ttu-id="7e2e7-174">상속자</span><span class="sxs-lookup"><span data-stu-id="7e2e7-174">NOTES</span></span>

## <span data-ttu-id="7e2e7-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e2e7-175">RELATED LINKS</span></span>

[<span data-ttu-id="7e2e7-176">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7e2e7-176">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="7e2e7-177">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="7e2e7-177">Get-AzureSiteRecoveryNetwork</span></span>](./Get-AzureSiteRecoveryNetwork.md)

[<span data-ttu-id="7e2e7-178">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7e2e7-178">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="7e2e7-179">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7e2e7-179">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="7e2e7-180">시작-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="7e2e7-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>](./Start-AzureSiteRecoveryUnplannedFailoverJob.md)


