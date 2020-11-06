---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: afef81ad904ccd5bf53f0b2a09bb10511e71fca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536220"
---
# <span data-ttu-id="94de8-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="94de8-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="94de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94de8-102">SYNOPSIS</span></span>
<span data-ttu-id="94de8-103">지정 된 ASR 작업 또는 복구 서비스 자격 증명 모음의 최근 ASR 작업 목록에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94de8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94de8-104">SYNTAX</span></span>

### <span data-ttu-id="94de8-105">ByParam (기본값)</span><span class="sxs-lookup"><span data-stu-id="94de8-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [<CommonParameters>]
```

### <span data-ttu-id="94de8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="94de8-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="94de8-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="94de8-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [<CommonParameters>]
```

## <span data-ttu-id="94de8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="94de8-108">DESCRIPTION</span></span>
<span data-ttu-id="94de8-109">**AzureRmRecoveryServicesAsrJob** Cmdlet은 Azure Site Recovery 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="94de8-110">이 cmdlet을 사용 하 여 복구 서비스 자격 증명 모음에서 ASR 작업을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="94de8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="94de8-111">EXAMPLES</span></span>

### <span data-ttu-id="94de8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="94de8-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="94de8-113">특정 ASR 개체의 모든 작업을 반환 합니다 (복제 된 항목 또는 복구 계획과 같은 ASR 개체를 해당 ID로 참조).</span><span class="sxs-lookup"><span data-stu-id="94de8-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="94de8-114">변수</span><span class="sxs-lookup"><span data-stu-id="94de8-114">PARAMETERS</span></span>

### <span data-ttu-id="94de8-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="94de8-115">-EndTime</span></span>
<span data-ttu-id="94de8-116">작업의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="94de8-117">이 cmdlet은 지정 된 시간 전에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="94de8-118">이 매개 변수에 대 한 **DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="94de8-119">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="94de8-119">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="94de8-120">-작업</span><span class="sxs-lookup"><span data-stu-id="94de8-120">-Job</span></span>
<span data-ttu-id="94de8-121">업데이트 세부 정보를 얻을 ASR 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-121">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="94de8-122">-이름</span><span class="sxs-lookup"><span data-stu-id="94de8-122">-Name</span></span>
<span data-ttu-id="94de8-123">이름으로 ASR 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-123">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94de8-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="94de8-124">-StartTime</span></span>
<span data-ttu-id="94de8-125">작업의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="94de8-126">이 cmdlet은 지정 된 시간 이후에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-126">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="94de8-127">-상태</span><span class="sxs-lookup"><span data-stu-id="94de8-127">-State</span></span>
<span data-ttu-id="94de8-128">ASR 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-128">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="94de8-129">이 cmdlet은 지정 된 상태와 일치 하는 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="94de8-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94de8-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="94de8-131">NotStarted</span></span>
- <span data-ttu-id="94de8-132">InProgress</span><span class="sxs-lookup"><span data-stu-id="94de8-132">InProgress</span></span>
- <span data-ttu-id="94de8-133">했음을</span><span class="sxs-lookup"><span data-stu-id="94de8-133">Succeeded</span></span>
- <span data-ttu-id="94de8-134">나머지</span><span class="sxs-lookup"><span data-stu-id="94de8-134">Other</span></span>
- <span data-ttu-id="94de8-135">못함</span><span class="sxs-lookup"><span data-stu-id="94de8-135">Failed</span></span>
- <span data-ttu-id="94de8-136">되었습니다</span><span class="sxs-lookup"><span data-stu-id="94de8-136">Cancelled</span></span>
- <span data-ttu-id="94de8-137">된</span><span class="sxs-lookup"><span data-stu-id="94de8-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94de8-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="94de8-138">-TargetObjectId</span></span>
<span data-ttu-id="94de8-139">개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-139">Specifies the ID of the object.</span></span> <span data-ttu-id="94de8-140">지정 된 개체에 대 한 작업을 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-140">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="94de8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94de8-141">CommonParameters</span></span>
<span data-ttu-id="94de8-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94de8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94de8-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94de8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94de8-144">입력</span><span class="sxs-lookup"><span data-stu-id="94de8-144">INPUTS</span></span>

### <span data-ttu-id="94de8-145">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="94de8-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="94de8-146">출력</span><span class="sxs-lookup"><span data-stu-id="94de8-146">OUTPUTS</span></span>

### <span data-ttu-id="94de8-147">System.webserver. t e r ' 1 [[SiteRecovery Rjob], [[Microsoft Azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="94de8-147">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="94de8-148">상속자</span><span class="sxs-lookup"><span data-stu-id="94de8-148">NOTES</span></span>

## <span data-ttu-id="94de8-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94de8-149">RELATED LINKS</span></span>

[<span data-ttu-id="94de8-150">다시 시작-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="94de8-150">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="94de8-151">이력서-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="94de8-151">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="94de8-152">중지-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="94de8-152">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
