---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 44A22B6C-5FD4-43B0-9726-71E28AE53E9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: de1b7a24c1af362297319d0297ce356b00ef9d49
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045778"
---
# <span data-ttu-id="5a31c-101">Start-AzureSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="5a31c-101">Start-AzureSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="5a31c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a31c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a31c-103">사이트 복구 개체에 대 한 장애 조치 커밋 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="5a31c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a31c-104">SYNTAX</span></span>

### <span data-ttu-id="5a31c-105">ByRPId (기본값)</span><span class="sxs-lookup"><span data-stu-id="5a31c-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RPId <String> [-Direction <String>] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a31c-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="5a31c-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 [-Direction <String>] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a31c-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5a31c-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a31c-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="5a31c-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a31c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="5a31c-109">DESCRIPTION</span></span>
<span data-ttu-id="5a31c-110">**AzureSiteRecoveryCommitFailoverJob** cmdlet은 장애 조치 (failover) 작업 후 Azure Site Recovery 개체에 대 한 장애 조치 (failover) 처리 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-110">The **Start-AzureSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="5a31c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5a31c-111">EXAMPLES</span></span>

### <span data-ttu-id="5a31c-112">예제 1: 커밋 장애 조치 작업 시작</span><span class="sxs-lookup"><span data-stu-id="5a31c-112">Example 1: Start a commit failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity $Protected
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

<span data-ttu-id="5a31c-113">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음의 보호 된 모든 컨테이너를 가져온 다음 결과를 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-113">The first command gets all protected containers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>

<span data-ttu-id="5a31c-114">두 번째 명령은 **AzureSiteRecoveryProtectionEntity** cmdlet을 사용 하 여 $Container에 저장 된 컨테이너에 속하는 보호 된 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-114">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="5a31c-115">명령이 $Protected 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="5a31c-116">마지막 명령은 $Protected에 저장 된 보호 된 개체에 대 한 장애 조치 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-116">The final command starts the failover job for the protected objects stored in $Protected.</span></span>

## <span data-ttu-id="5a31c-117">변수</span><span class="sxs-lookup"><span data-stu-id="5a31c-117">PARAMETERS</span></span>

### <span data-ttu-id="5a31c-118">방향</span><span class="sxs-lookup"><span data-stu-id="5a31c-118">-Direction</span></span>
<span data-ttu-id="5a31c-119">장애 조치의 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="5a31c-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a31c-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="5a31c-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="5a31c-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="5a31c-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="5a31c-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="5a31c-123">-Profile</span></span>
<span data-ttu-id="5a31c-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a31c-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a31c-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="5a31c-126">-ProtectionContainerId</span></span>
<span data-ttu-id="5a31c-127">보호 된 컨테이너의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="5a31c-128">이 cmdlet은이 cmdlet에서 지정 하는 컨테이너에 속하는 보호 된 가상 컴퓨터에 대 한 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-128">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="5a31c-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5a31c-129">-ProtectionEntity</span></span>
<span data-ttu-id="5a31c-130">작업을 시작할 **ASRProtectionEntity** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-130">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="5a31c-131">**ASRProtectionEntity** 개체를 얻으려면 **Get-AzureSiteRecoveryProtectionEntity** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-131">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

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

### <span data-ttu-id="5a31c-132">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="5a31c-132">-ProtectionEntityId</span></span>
<span data-ttu-id="5a31c-133">작업을 시작할 보호 된 가상 컴퓨터의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-133">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="5a31c-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a31c-134">-RecoveryPlan</span></span>
<span data-ttu-id="5a31c-135">작업을 시작할 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-135">Specifies a recovery plan object for which to start the job.</span></span>
<span data-ttu-id="5a31c-136">**Asrrecoveryplan** 개체를 얻으려면 **Get-AzureSiteRecoveryRecoveryPlan** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-136">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="5a31c-137">-RPId</span><span class="sxs-lookup"><span data-stu-id="5a31c-137">-RPId</span></span>
<span data-ttu-id="5a31c-138">작업을 시작할 복구 계획의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-138">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="5a31c-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5a31c-139">-WaitForCompletion</span></span>
<span data-ttu-id="5a31c-140">Cmdlet이 Windows PowerShell 콘솔에 제어를 반환 하기 전에 작업이 완료 될 때까지 대기 하 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="5a31c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a31c-141">CommonParameters</span></span>
<span data-ttu-id="5a31c-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a31c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a31c-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a31c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a31c-144">입력</span><span class="sxs-lookup"><span data-stu-id="5a31c-144">INPUTS</span></span>

## <span data-ttu-id="5a31c-145">출력</span><span class="sxs-lookup"><span data-stu-id="5a31c-145">OUTPUTS</span></span>

## <span data-ttu-id="5a31c-146">상속자</span><span class="sxs-lookup"><span data-stu-id="5a31c-146">NOTES</span></span>

## <span data-ttu-id="5a31c-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a31c-147">RELATED LINKS</span></span>

[<span data-ttu-id="5a31c-148">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a31c-148">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="5a31c-149">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5a31c-149">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="5a31c-150">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5a31c-150">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


