---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: f79bc9e32ab179c10c09f3780a591182ea1d630b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702906"
---
# <span data-ttu-id="bb6f9-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bb6f9-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="bb6f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6f9-103">지정 된 ASR 작업 또는 복구 서비스 자격 증명 모음의 최근 ASR 작업 목록에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb6f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb6f9-104">SYNTAX</span></span>

### <span data-ttu-id="bb6f9-105">ByParam (기본값)</span><span class="sxs-lookup"><span data-stu-id="bb6f9-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb6f9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bb6f9-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb6f9-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="bb6f9-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb6f9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bb6f9-108">DESCRIPTION</span></span>
<span data-ttu-id="bb6f9-109">**AzureRmRecoveryServicesAsrJob** Cmdlet은 Azure Site Recovery 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="bb6f9-110">이 cmdlet을 사용 하 여 복구 서비스 자격 증명 모음에서 ASR 작업을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="bb6f9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bb6f9-111">EXAMPLES</span></span>

### <span data-ttu-id="bb6f9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb6f9-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="bb6f9-113">특정 ASR 개체의 모든 작업을 반환 합니다 (복제 된 항목 또는 복구 계획과 같은 ASR 개체를 해당 ID로 참조).</span><span class="sxs-lookup"><span data-stu-id="bb6f9-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="bb6f9-114">변수</span><span class="sxs-lookup"><span data-stu-id="bb6f9-114">PARAMETERS</span></span>

### <span data-ttu-id="bb6f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6f9-115">-DefaultProfile</span></span>
<span data-ttu-id="bb6f9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6f9-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="bb6f9-117">-EndTime</span></span>
<span data-ttu-id="bb6f9-118">작업의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="bb6f9-119">이 cmdlet은 지정 된 시간 전에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="bb6f9-120">이 매개 변수에 대 한 **DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="bb6f9-121">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="bb6f9-122">-작업</span><span class="sxs-lookup"><span data-stu-id="bb6f9-122">-Job</span></span>
<span data-ttu-id="bb6f9-123">업데이트 세부 정보를 얻을 ASR 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-123">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="bb6f9-124">-이름</span><span class="sxs-lookup"><span data-stu-id="bb6f9-124">-Name</span></span>
<span data-ttu-id="bb6f9-125">이름으로 ASR 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="bb6f9-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bb6f9-126">-StartTime</span></span>
<span data-ttu-id="bb6f9-127">작업의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="bb6f9-128">이 cmdlet은 지정 된 시간 이후에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-128">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="bb6f9-129">-상태</span><span class="sxs-lookup"><span data-stu-id="bb6f9-129">-State</span></span>
<span data-ttu-id="bb6f9-130">ASR 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="bb6f9-131">이 cmdlet은 지정 된 상태와 일치 하는 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="bb6f9-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bb6f9-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="bb6f9-133">NotStarted</span></span>
- <span data-ttu-id="bb6f9-134">InProgress</span><span class="sxs-lookup"><span data-stu-id="bb6f9-134">InProgress</span></span>
- <span data-ttu-id="bb6f9-135">했음을</span><span class="sxs-lookup"><span data-stu-id="bb6f9-135">Succeeded</span></span>
- <span data-ttu-id="bb6f9-136">나머지</span><span class="sxs-lookup"><span data-stu-id="bb6f9-136">Other</span></span>
- <span data-ttu-id="bb6f9-137">못함</span><span class="sxs-lookup"><span data-stu-id="bb6f9-137">Failed</span></span>
- <span data-ttu-id="bb6f9-138">되었습니다</span><span class="sxs-lookup"><span data-stu-id="bb6f9-138">Cancelled</span></span>
- <span data-ttu-id="bb6f9-139">된</span><span class="sxs-lookup"><span data-stu-id="bb6f9-139">Suspended</span></span>

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

### <span data-ttu-id="bb6f9-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="bb6f9-140">-TargetObjectId</span></span>
<span data-ttu-id="bb6f9-141">개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-141">Specifies the ID of the object.</span></span> <span data-ttu-id="bb6f9-142">지정 된 개체에 대 한 작업을 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-142">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="bb6f9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6f9-143">CommonParameters</span></span>
<span data-ttu-id="bb6f9-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6f9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6f9-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb6f9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6f9-146">입력</span><span class="sxs-lookup"><span data-stu-id="bb6f9-146">INPUTS</span></span>

### <span data-ttu-id="bb6f9-147">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="bb6f9-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bb6f9-148">출력</span><span class="sxs-lookup"><span data-stu-id="bb6f9-148">OUTPUTS</span></span>

### <span data-ttu-id="bb6f9-149">System.webserver. t e r ' 1 [[SiteRecovery Rjob], [[Microsoft Azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="bb6f9-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bb6f9-150">상속자</span><span class="sxs-lookup"><span data-stu-id="bb6f9-150">NOTES</span></span>

## <span data-ttu-id="bb6f9-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb6f9-151">RELATED LINKS</span></span>

[<span data-ttu-id="bb6f9-152">다시 시작-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bb6f9-152">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="bb6f9-153">이력서-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bb6f9-153">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="bb6f9-154">중지-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bb6f9-154">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
