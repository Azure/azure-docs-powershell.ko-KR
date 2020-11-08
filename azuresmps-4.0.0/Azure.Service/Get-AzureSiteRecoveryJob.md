---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0b272732cf6c1e1b2025c8e7f48b58e4807cdb3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045595"
---
# <span data-ttu-id="e1351-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e1351-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="e1351-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1351-102">SYNOPSIS</span></span>
<span data-ttu-id="e1351-103">사이트 복구 자격 증명 모음에 대 한 작업 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="e1351-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1351-104">SYNTAX</span></span>

### <span data-ttu-id="e1351-105">ByParam (기본값)</span><span class="sxs-lookup"><span data-stu-id="e1351-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e1351-106">ById</span><span class="sxs-lookup"><span data-stu-id="e1351-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e1351-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="e1351-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e1351-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e1351-108">DESCRIPTION</span></span>
<span data-ttu-id="e1351-109">**AzureSiteRecoveryJob** Cmdlet은 Azure Site Recovery 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="e1351-110">이 cmdlet을 사용 하 여 현재 사이트 복구 자격 증명 모음에 대 한 작업 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="e1351-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e1351-111">EXAMPLES</span></span>

### <span data-ttu-id="e1351-112">예제 1: ID를 지정 하 여 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="e1351-112">Example 1: Get a job by specifying an ID</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="e1351-113">이 명령은 지정 된 ID를 갖는 Azure Site Recovery 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="e1351-114">예제 2: 시간을 기준으로 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-114">Example 2: Gets a job based on time</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="e1351-115">이 명령은 지정 된 시작 시간과 종료 시간 사이에 속하는 사이트 복구 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="e1351-116">변수</span><span class="sxs-lookup"><span data-stu-id="e1351-116">PARAMETERS</span></span>

### <span data-ttu-id="e1351-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e1351-117">-EndTime</span></span>
<span data-ttu-id="e1351-118">작업의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="e1351-119">이 cmdlet은 지정 된 시간 전에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="e1351-120">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="e1351-121">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="e1351-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1351-122">-Id</span><span class="sxs-lookup"><span data-stu-id="e1351-122">-Id</span></span>
<span data-ttu-id="e1351-123">가져올 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-123">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1351-124">-작업</span><span class="sxs-lookup"><span data-stu-id="e1351-124">-Job</span></span>
<span data-ttu-id="e1351-125">가져올 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-125">Specifies a job to get.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1351-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="e1351-126">-Profile</span></span>
<span data-ttu-id="e1351-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e1351-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e1351-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e1351-129">-StartTime</span></span>
<span data-ttu-id="e1351-130">작업의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="e1351-131">이 cmdlet은 지정 된 시간 이후에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-131">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1351-132">-상태</span><span class="sxs-lookup"><span data-stu-id="e1351-132">-State</span></span>
<span data-ttu-id="e1351-133">사이트 복구 작업의 입력 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="e1351-134">이 cmdlet은 지정 된 상태와 일치 하는 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="e1351-135">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1351-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="e1351-136">NotStarted</span></span>
- <span data-ttu-id="e1351-137">InProgress</span><span class="sxs-lookup"><span data-stu-id="e1351-137">InProgress</span></span>
- <span data-ttu-id="e1351-138">했음을</span><span class="sxs-lookup"><span data-stu-id="e1351-138">Succeeded</span></span>
- <span data-ttu-id="e1351-139">나머지</span><span class="sxs-lookup"><span data-stu-id="e1351-139">Other</span></span>
- <span data-ttu-id="e1351-140">못함</span><span class="sxs-lookup"><span data-stu-id="e1351-140">Failed</span></span>
- <span data-ttu-id="e1351-141">되었습니다</span><span class="sxs-lookup"><span data-stu-id="e1351-141">Cancelled</span></span>
- <span data-ttu-id="e1351-142">된</span><span class="sxs-lookup"><span data-stu-id="e1351-142">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1351-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="e1351-143">-TargetObjectId</span></span>
<span data-ttu-id="e1351-144">작업을 대상으로 하는 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-144">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1351-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1351-145">CommonParameters</span></span>
<span data-ttu-id="e1351-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1351-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1351-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1351-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1351-148">입력</span><span class="sxs-lookup"><span data-stu-id="e1351-148">INPUTS</span></span>

## <span data-ttu-id="e1351-149">출력</span><span class="sxs-lookup"><span data-stu-id="e1351-149">OUTPUTS</span></span>

## <span data-ttu-id="e1351-150">상속자</span><span class="sxs-lookup"><span data-stu-id="e1351-150">NOTES</span></span>

## <span data-ttu-id="e1351-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1351-151">RELATED LINKS</span></span>

[<span data-ttu-id="e1351-152">Azure Site Recovery 서비스 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e1351-152">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)

[<span data-ttu-id="e1351-153">다시 시작-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e1351-153">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="e1351-154">이력서-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e1351-154">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="e1351-155">중지-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e1351-155">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


