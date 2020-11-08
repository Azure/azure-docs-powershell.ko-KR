---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AC73119B-BB76-425B-AA44-44502028ECC4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a74a02f219b5bb64957ab919168cb79ccf681869
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045806"
---
# <span data-ttu-id="f4f87-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f4f87-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="f4f87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f87-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f87-103">사이트 복구 보호 엔터티 또는 복구 계획에 대해 계획 되지 않은 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

## <span data-ttu-id="f4f87-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4f87-104">SYNTAX</span></span>

### <span data-ttu-id="f4f87-105">ByRPId (기본값)</span><span class="sxs-lookup"><span data-stu-id="f4f87-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RPId <String> -Direction <String> [-PrimaryAction <Boolean>]
 [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f4f87-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="f4f87-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f4f87-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f4f87-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PrimaryAction <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4f87-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="f4f87-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f4f87-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f4f87-109">DESCRIPTION</span></span>
<span data-ttu-id="f4f87-110">**AzureSiteRecoveryUnplannedFailoverJob** Cmdlet은 Azure Site Recovery 보호 엔터티 또는 복구 계획의 계획 되지 않은 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-110">The **Start-AzureSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="f4f87-111">**AzureSiteRecoveryJob** cmdlet을 사용 하 여 작업이 성공 하는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="f4f87-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f4f87-112">EXAMPLES</span></span>

### <span data-ttu-id="f4f87-113">예제 1: 계획 되지 않은 장애 조치 작업 시작</span><span class="sxs-lookup"><span data-stu-id="f4f87-113">Example 1: Start an unplanned failover job</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer 
PS C:\> Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="f4f87-114">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 보호 된 컨테이너를 가져온 다음 $ProtectionContainer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-114">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="f4f87-115">두 번째 명령은 **AzureSiteRecoveryProtectionEntity** cmdlet을 사용 하 여 $ProtectionContainer에 저장 된 보호 컨테이너에 속하는 보호 되는 엔터티를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-115">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="f4f87-116">명령이 $ProtectionEntity 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-116">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="f4f87-117">마지막 명령은 $ProtectionEntity에 저장 된 보호 된 엔터티에 대 한 장애 조치를 시작 하 고 장애 조치 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-117">The final command starts the failover for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

## <span data-ttu-id="f4f87-118">변수</span><span class="sxs-lookup"><span data-stu-id="f4f87-118">PARAMETERS</span></span>

### <span data-ttu-id="f4f87-119">방향</span><span class="sxs-lookup"><span data-stu-id="f4f87-119">-Direction</span></span>
<span data-ttu-id="f4f87-120">장애 조치의 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="f4f87-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f4f87-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f4f87-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="f4f87-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f4f87-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="f4f87-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="f4f87-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="f4f87-125">작업이 소스 측 작업을 수행할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-125">Indicates that the action can perform source side actions.</span></span>

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

### <span data-ttu-id="f4f87-126">-PerformSourceSiteOperations</span><span class="sxs-lookup"><span data-stu-id="f4f87-126">-PerformSourceSiteOperations</span></span>
<span data-ttu-id="f4f87-127">원본 사이트 작업을 수행할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-127">Indicates that source site operations can be performed.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByPEId, ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f87-128">-PrimaryAction</span><span class="sxs-lookup"><span data-stu-id="f4f87-128">-PrimaryAction</span></span>
<span data-ttu-id="f4f87-129">기본 사이트 작업이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-129">Indicates that  primary site actions are required.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByRPId, ByRPObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f87-130">-프로필</span><span class="sxs-lookup"><span data-stu-id="f4f87-130">-Profile</span></span>
<span data-ttu-id="f4f87-131">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4f87-132">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4f87-133">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="f4f87-133">-ProtectionContainerId</span></span>
<span data-ttu-id="f4f87-134">보호 된 컨테이너의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-134">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="f4f87-135">이 cmdlet은이 cmdlet에서 지정 하는 컨테이너에 속하는 보호 된 가상 컴퓨터에 대 한 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-135">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="f4f87-136">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f4f87-136">-ProtectionEntity</span></span>
<span data-ttu-id="f4f87-137">사이트 복구 보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-137">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="f4f87-138">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="f4f87-138">-ProtectionEntityId</span></span>
<span data-ttu-id="f4f87-139">작업을 시작할 보호 된 가상 컴퓨터의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-139">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="f4f87-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f4f87-140">-RecoveryPlan</span></span>
<span data-ttu-id="f4f87-141">복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-141">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="f4f87-142">-RPId</span><span class="sxs-lookup"><span data-stu-id="f4f87-142">-RPId</span></span>
<span data-ttu-id="f4f87-143">작업을 시작할 복구 계획의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-143">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="f4f87-144">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f4f87-144">-WaitForCompletion</span></span>
<span data-ttu-id="f4f87-145">Cmdlet이 Windows PowerShell 콘솔에 제어를 반환 하기 전에 작업이 완료 될 때까지 대기 하 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-145">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f4f87-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f87-146">CommonParameters</span></span>
<span data-ttu-id="f4f87-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f87-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f87-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4f87-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f87-149">입력</span><span class="sxs-lookup"><span data-stu-id="f4f87-149">INPUTS</span></span>

## <span data-ttu-id="f4f87-150">출력</span><span class="sxs-lookup"><span data-stu-id="f4f87-150">OUTPUTS</span></span>

## <span data-ttu-id="f4f87-151">상속자</span><span class="sxs-lookup"><span data-stu-id="f4f87-151">NOTES</span></span>

## <span data-ttu-id="f4f87-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4f87-152">RELATED LINKS</span></span>

[<span data-ttu-id="f4f87-153">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f4f87-153">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="f4f87-154">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f4f87-154">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="f4f87-155">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f4f87-155">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="f4f87-156">시작-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f4f87-156">Start-AzureSiteRecoveryTestFailoverJob</span></span>](./Start-AzureSiteRecoveryTestFailoverJob.md)


