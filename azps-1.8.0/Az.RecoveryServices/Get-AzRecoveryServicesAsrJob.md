---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 85479392a34e81395d3f00e3ef3891772a2dcbec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699743"
---
# <span data-ttu-id="dce25-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dce25-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="dce25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dce25-102">SYNOPSIS</span></span>
<span data-ttu-id="dce25-103">지정 된 ASR 작업 또는 복구 서비스 자격 증명 모음의 최근 ASR 작업 목록에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="dce25-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dce25-104">SYNTAX</span></span>

### <span data-ttu-id="dce25-105">ByParam (기본값)</span><span class="sxs-lookup"><span data-stu-id="dce25-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dce25-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dce25-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dce25-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="dce25-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dce25-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dce25-108">DESCRIPTION</span></span>
<span data-ttu-id="dce25-109">**AzRecoveryServicesAsrJob** Cmdlet은 Azure Site Recovery 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="dce25-110">이 cmdlet을 사용 하 여 복구 서비스 자격 증명 모음에서 ASR 작업을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="dce25-111">예제의</span><span class="sxs-lookup"><span data-stu-id="dce25-111">EXAMPLES</span></span>

### <span data-ttu-id="dce25-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="dce25-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="dce25-113">특정 ASR 개체의 모든 작업을 반환 합니다 (복제 된 항목 또는 복구 계획과 같은 ASR 개체를 해당 ID로 참조).</span><span class="sxs-lookup"><span data-stu-id="dce25-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="dce25-114">변수</span><span class="sxs-lookup"><span data-stu-id="dce25-114">PARAMETERS</span></span>

### <span data-ttu-id="dce25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce25-115">-DefaultProfile</span></span>
<span data-ttu-id="dce25-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dce25-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dce25-117">-EndTime</span></span>
<span data-ttu-id="dce25-118">작업의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="dce25-119">이 cmdlet은 지정 된 시간 전에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="dce25-120">이 매개 변수에 대 한 **DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="dce25-121">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="dce25-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce25-122">-작업</span><span class="sxs-lookup"><span data-stu-id="dce25-122">-Job</span></span>
<span data-ttu-id="dce25-123">업데이트 세부 정보를 얻을 ASR 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-123">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dce25-124">-이름</span><span class="sxs-lookup"><span data-stu-id="dce25-124">-Name</span></span>
<span data-ttu-id="dce25-125">이름으로 ASR 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-125">Specify the ASR job by name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce25-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dce25-126">-StartTime</span></span>
<span data-ttu-id="dce25-127">작업의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="dce25-128">이 cmdlet은 지정 된 시간 이후에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-128">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce25-129">-상태</span><span class="sxs-lookup"><span data-stu-id="dce25-129">-State</span></span>
<span data-ttu-id="dce25-130">ASR 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="dce25-131">이 cmdlet은 지정 된 상태와 일치 하는 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="dce25-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dce25-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="dce25-133">NotStarted</span></span>
- <span data-ttu-id="dce25-134">InProgress</span><span class="sxs-lookup"><span data-stu-id="dce25-134">InProgress</span></span>
- <span data-ttu-id="dce25-135">했음을</span><span class="sxs-lookup"><span data-stu-id="dce25-135">Succeeded</span></span>
- <span data-ttu-id="dce25-136">나머지</span><span class="sxs-lookup"><span data-stu-id="dce25-136">Other</span></span>
- <span data-ttu-id="dce25-137">못함</span><span class="sxs-lookup"><span data-stu-id="dce25-137">Failed</span></span>
- <span data-ttu-id="dce25-138">되었습니다</span><span class="sxs-lookup"><span data-stu-id="dce25-138">Cancelled</span></span>
- <span data-ttu-id="dce25-139">된</span><span class="sxs-lookup"><span data-stu-id="dce25-139">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce25-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="dce25-140">-TargetObjectId</span></span>
<span data-ttu-id="dce25-141">개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-141">Specifies the ID of the object.</span></span> <span data-ttu-id="dce25-142">지정 된 개체에 대 한 작업을 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-142">Used to search for jobs on the specified object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce25-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce25-143">CommonParameters</span></span>
<span data-ttu-id="dce25-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce25-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce25-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce25-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce25-146">입력</span><span class="sxs-lookup"><span data-stu-id="dce25-146">INPUTS</span></span>

### <span data-ttu-id="dce25-147">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="dce25-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dce25-148">출력</span><span class="sxs-lookup"><span data-stu-id="dce25-148">OUTPUTS</span></span>

### <span data-ttu-id="dce25-149">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="dce25-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dce25-150">상속자</span><span class="sxs-lookup"><span data-stu-id="dce25-150">NOTES</span></span>

## <span data-ttu-id="dce25-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dce25-151">RELATED LINKS</span></span>

[<span data-ttu-id="dce25-152">다시 시작-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dce25-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="dce25-153">이력서-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dce25-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="dce25-154">중지-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dce25-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
