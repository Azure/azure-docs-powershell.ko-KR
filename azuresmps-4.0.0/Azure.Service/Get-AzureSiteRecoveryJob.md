---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a7c99e2ce307d700e43094ffa9be47e5449acc0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411656"
---
# <span data-ttu-id="05be7-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="05be7-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="05be7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05be7-102">SYNOPSIS</span></span>
<span data-ttu-id="05be7-103">Site Recovery 자격 증명 모음에 대한 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="05be7-104">구문</span><span class="sxs-lookup"><span data-stu-id="05be7-104">SYNTAX</span></span>

### <span data-ttu-id="05be7-105">ByParam(기본값)</span><span class="sxs-lookup"><span data-stu-id="05be7-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="05be7-106">ById</span><span class="sxs-lookup"><span data-stu-id="05be7-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="05be7-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="05be7-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="05be7-108">설명</span><span class="sxs-lookup"><span data-stu-id="05be7-108">DESCRIPTION</span></span>
<span data-ttu-id="05be7-109">**Get-AzureSiteRecoveryJob** cmdlet은 Azure Site Recovery 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="05be7-110">이 cmdlet을 사용하여 현재 Site Recovery 자격 증명 모음에 대한 작업 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="05be7-111">예제</span><span class="sxs-lookup"><span data-stu-id="05be7-111">EXAMPLES</span></span>

### <span data-ttu-id="05be7-112">예제 1: ID를 지정하여 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="05be7-112">Example 1: Get a job by specifying an ID</span></span>
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

<span data-ttu-id="05be7-113">이 명령은 지정된 ID가 있는 Azure Site Recovery 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="05be7-114">예제 2: 시간을 기준으로 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-114">Example 2: Gets a job based on time</span></span>
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

<span data-ttu-id="05be7-115">이 명령은 지정된 시작 시간과 종료 시간 사이에 있는 Site Recovery 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="05be7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05be7-116">PARAMETERS</span></span>

### <span data-ttu-id="05be7-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="05be7-117">-EndTime</span></span>
<span data-ttu-id="05be7-118">작업의 종료 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="05be7-119">이 cmdlet은 지정된 시간 전에 시작된 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="05be7-120">**DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="05be7-121">자세한 내용은 `Get-Help Get-Date` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="05be7-122">-Id</span><span class="sxs-lookup"><span data-stu-id="05be7-122">-Id</span></span>
<span data-ttu-id="05be7-123">얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-123">Specifies the ID of a job to get.</span></span>

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

### <span data-ttu-id="05be7-124">-Job</span><span class="sxs-lookup"><span data-stu-id="05be7-124">-Job</span></span>
<span data-ttu-id="05be7-125">얻을 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-125">Specifies a job to get.</span></span>

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

### <span data-ttu-id="05be7-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="05be7-126">-Profile</span></span>
<span data-ttu-id="05be7-127">이 cmdlet이 읽을 Azure 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05be7-128">프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05be7-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="05be7-129">-StartTime</span></span>
<span data-ttu-id="05be7-130">작업의 시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="05be7-131">이 cmdlet은 지정된 시간 후에 시작된 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-131">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="05be7-132">-State</span><span class="sxs-lookup"><span data-stu-id="05be7-132">-State</span></span>
<span data-ttu-id="05be7-133">Site Recovery 작업의 입력 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="05be7-134">이 cmdlet은 지정된 상태와 일치하는 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="05be7-135">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="05be7-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05be7-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="05be7-136">NotStarted</span></span>
- <span data-ttu-id="05be7-137">InProgress</span><span class="sxs-lookup"><span data-stu-id="05be7-137">InProgress</span></span>
- <span data-ttu-id="05be7-138">성공</span><span class="sxs-lookup"><span data-stu-id="05be7-138">Succeeded</span></span>
- <span data-ttu-id="05be7-139">기타</span><span class="sxs-lookup"><span data-stu-id="05be7-139">Other</span></span>
- <span data-ttu-id="05be7-140">실패</span><span class="sxs-lookup"><span data-stu-id="05be7-140">Failed</span></span>
- <span data-ttu-id="05be7-141">Cancelled</span><span class="sxs-lookup"><span data-stu-id="05be7-141">Cancelled</span></span>
- <span data-ttu-id="05be7-142">일시 중단</span><span class="sxs-lookup"><span data-stu-id="05be7-142">Suspended</span></span>

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

### <span data-ttu-id="05be7-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="05be7-143">-TargetObjectId</span></span>
<span data-ttu-id="05be7-144">작업을 대상으로 하는 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-144">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="05be7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05be7-145">CommonParameters</span></span>
<span data-ttu-id="05be7-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="05be7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05be7-147">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="05be7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05be7-148">입력</span><span class="sxs-lookup"><span data-stu-id="05be7-148">INPUTS</span></span>

## <span data-ttu-id="05be7-149">출력</span><span class="sxs-lookup"><span data-stu-id="05be7-149">OUTPUTS</span></span>

## <span data-ttu-id="05be7-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="05be7-150">NOTES</span></span>

## <span data-ttu-id="05be7-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05be7-151">RELATED LINKS</span></span>



[<span data-ttu-id="05be7-152">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="05be7-152">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="05be7-153">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="05be7-153">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="05be7-154">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="05be7-154">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


