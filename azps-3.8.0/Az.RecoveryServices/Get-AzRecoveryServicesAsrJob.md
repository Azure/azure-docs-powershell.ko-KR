---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: b71c9a5da3c89916b18bdb5446f311e3d71615bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877438"
---
# <span data-ttu-id="f420c-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f420c-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="f420c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f420c-102">SYNOPSIS</span></span>
<span data-ttu-id="f420c-103">지정 된 ASR 작업 또는 복구 서비스 자격 증명 모음의 최근 ASR 작업 목록에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="f420c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f420c-104">SYNTAX</span></span>

### <span data-ttu-id="f420c-105">ByParam (기본값)</span><span class="sxs-lookup"><span data-stu-id="f420c-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f420c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f420c-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f420c-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="f420c-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f420c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f420c-108">DESCRIPTION</span></span>
<span data-ttu-id="f420c-109">**AzRecoveryServicesAsrJob** Cmdlet은 Azure Site Recovery 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="f420c-110">이 cmdlet을 사용 하 여 복구 서비스 자격 증명 모음에서 ASR 작업을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="f420c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f420c-111">EXAMPLES</span></span>

### <span data-ttu-id="f420c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f420c-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="f420c-113">특정 ASR 개체의 모든 작업을 반환 합니다 (복제 된 항목 또는 복구 계획과 같은 ASR 개체를 해당 ID로 참조).</span><span class="sxs-lookup"><span data-stu-id="f420c-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="f420c-114">변수</span><span class="sxs-lookup"><span data-stu-id="f420c-114">PARAMETERS</span></span>

### <span data-ttu-id="f420c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f420c-115">-DefaultProfile</span></span>
<span data-ttu-id="f420c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f420c-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f420c-117">-EndTime</span></span>
<span data-ttu-id="f420c-118">작업의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="f420c-119">이 cmdlet은 지정 된 시간 전에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="f420c-120">이 매개 변수에 대 한 **DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="f420c-121">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="f420c-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="f420c-122">-작업</span><span class="sxs-lookup"><span data-stu-id="f420c-122">-Job</span></span>
<span data-ttu-id="f420c-123">업데이트 세부 정보를 얻을 ASR 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-123">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="f420c-124">-이름</span><span class="sxs-lookup"><span data-stu-id="f420c-124">-Name</span></span>
<span data-ttu-id="f420c-125">이름으로 ASR 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="f420c-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f420c-126">-StartTime</span></span>
<span data-ttu-id="f420c-127">작업의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="f420c-128">이 cmdlet은 지정 된 시간 이후에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-128">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="f420c-129">-상태</span><span class="sxs-lookup"><span data-stu-id="f420c-129">-State</span></span>
<span data-ttu-id="f420c-130">ASR 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="f420c-131">이 cmdlet은 지정 된 상태와 일치 하는 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="f420c-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f420c-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="f420c-133">NotStarted</span></span>
- <span data-ttu-id="f420c-134">InProgress</span><span class="sxs-lookup"><span data-stu-id="f420c-134">InProgress</span></span>
- <span data-ttu-id="f420c-135">했음을</span><span class="sxs-lookup"><span data-stu-id="f420c-135">Succeeded</span></span>
- <span data-ttu-id="f420c-136">나머지</span><span class="sxs-lookup"><span data-stu-id="f420c-136">Other</span></span>
- <span data-ttu-id="f420c-137">못함</span><span class="sxs-lookup"><span data-stu-id="f420c-137">Failed</span></span>
- <span data-ttu-id="f420c-138">되었습니다</span><span class="sxs-lookup"><span data-stu-id="f420c-138">Cancelled</span></span>
- <span data-ttu-id="f420c-139">된</span><span class="sxs-lookup"><span data-stu-id="f420c-139">Suspended</span></span>

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

### <span data-ttu-id="f420c-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="f420c-140">-TargetObjectId</span></span>
<span data-ttu-id="f420c-141">개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-141">Specifies the ID of the object.</span></span> <span data-ttu-id="f420c-142">지정 된 개체에 대 한 작업을 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-142">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="f420c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f420c-143">CommonParameters</span></span>
<span data-ttu-id="f420c-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f420c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f420c-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f420c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f420c-146">입력</span><span class="sxs-lookup"><span data-stu-id="f420c-146">INPUTS</span></span>

### <span data-ttu-id="f420c-147">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="f420c-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f420c-148">출력</span><span class="sxs-lookup"><span data-stu-id="f420c-148">OUTPUTS</span></span>

### <span data-ttu-id="f420c-149">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="f420c-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f420c-150">상속자</span><span class="sxs-lookup"><span data-stu-id="f420c-150">NOTES</span></span>

## <span data-ttu-id="f420c-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f420c-151">RELATED LINKS</span></span>

[<span data-ttu-id="f420c-152">다시 시작-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f420c-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="f420c-153">이력서-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f420c-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="f420c-154">중지-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f420c-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
