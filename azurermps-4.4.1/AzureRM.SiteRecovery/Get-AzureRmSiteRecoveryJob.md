---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 2365b806bd274bb9cc18f84c83a29423408780d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702401"
---
# <span data-ttu-id="943d1-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="943d1-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="943d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="943d1-102">SYNOPSIS</span></span>
<span data-ttu-id="943d1-103">현재 사이트 복구 자격 증명 모음에 대 한 작업 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="943d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="943d1-104">SYNTAX</span></span>

### <span data-ttu-id="943d1-105">ByParam (기본값)</span><span class="sxs-lookup"><span data-stu-id="943d1-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="943d1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="943d1-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="943d1-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="943d1-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="943d1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="943d1-108">DESCRIPTION</span></span>
<span data-ttu-id="943d1-109">**AzureRmSiteRecoveryJob** Cmdlet은 Azure Site Recovery 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="943d1-110">이 cmdlet을 사용 하 여 현재 사이트 복구 자격 증명 모음에 대 한 작업 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="943d1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="943d1-111">EXAMPLES</span></span>

## <span data-ttu-id="943d1-112">변수</span><span class="sxs-lookup"><span data-stu-id="943d1-112">PARAMETERS</span></span>

### <span data-ttu-id="943d1-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="943d1-113">-EndTime</span></span>
<span data-ttu-id="943d1-114">작업의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-114">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="943d1-115">이 cmdlet은 지정 된 시간 전에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-115">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="943d1-116">이 매개 변수에 대 한 **DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-116">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="943d1-117">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="943d1-117">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="943d1-118">-작업</span><span class="sxs-lookup"><span data-stu-id="943d1-118">-Job</span></span>
<span data-ttu-id="943d1-119">사이트 복구 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-119">Specifies the Site Recovery job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="943d1-120">-이름</span><span class="sxs-lookup"><span data-stu-id="943d1-120">-Name</span></span>
<span data-ttu-id="943d1-121">작업을 식별 하는 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-121">Specifies a unique name that identifies the job.</span></span>

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

### <span data-ttu-id="943d1-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="943d1-122">-StartTime</span></span>
<span data-ttu-id="943d1-123">작업의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-123">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="943d1-124">이 cmdlet은 지정 된 시간 이후에 시작 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-124">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="943d1-125">-상태</span><span class="sxs-lookup"><span data-stu-id="943d1-125">-State</span></span>
<span data-ttu-id="943d1-126">사이트 복구 작업의 입력 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-126">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="943d1-127">이 cmdlet은 지정 된 상태와 일치 하는 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-127">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="943d1-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="943d1-129">NotStarted</span><span class="sxs-lookup"><span data-stu-id="943d1-129">NotStarted</span></span>
- <span data-ttu-id="943d1-130">InProgress</span><span class="sxs-lookup"><span data-stu-id="943d1-130">InProgress</span></span>
- <span data-ttu-id="943d1-131">했음을</span><span class="sxs-lookup"><span data-stu-id="943d1-131">Succeeded</span></span>
- <span data-ttu-id="943d1-132">나머지</span><span class="sxs-lookup"><span data-stu-id="943d1-132">Other</span></span>
- <span data-ttu-id="943d1-133">못함</span><span class="sxs-lookup"><span data-stu-id="943d1-133">Failed</span></span>
- <span data-ttu-id="943d1-134">되었습니다</span><span class="sxs-lookup"><span data-stu-id="943d1-134">Cancelled</span></span>
- <span data-ttu-id="943d1-135">된</span><span class="sxs-lookup"><span data-stu-id="943d1-135">Suspended</span></span>

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

### <span data-ttu-id="943d1-136">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="943d1-136">-TargetObjectId</span></span>
<span data-ttu-id="943d1-137">작업을 대상으로 하는 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-137">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="943d1-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="943d1-138">-DefaultProfile</span></span>
<span data-ttu-id="943d1-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="943d1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="943d1-140">CommonParameters</span></span>
<span data-ttu-id="943d1-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="943d1-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="943d1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="943d1-143">입력</span><span class="sxs-lookup"><span data-stu-id="943d1-143">INPUTS</span></span>

### <span data-ttu-id="943d1-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="943d1-144">ASRJob</span></span>
<span data-ttu-id="943d1-145">' Job ' 매개 변수는 파이프라인에서 ' ASRJob ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="943d1-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="943d1-146">출력</span><span class="sxs-lookup"><span data-stu-id="943d1-146">OUTPUTS</span></span>

### <span data-ttu-id="943d1-147">System.webserver. t e r ' 1 [SiteRecovery Rm 작업]</span><span class="sxs-lookup"><span data-stu-id="943d1-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="943d1-148">상속자</span><span class="sxs-lookup"><span data-stu-id="943d1-148">NOTES</span></span>

## <span data-ttu-id="943d1-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="943d1-149">RELATED LINKS</span></span>

[<span data-ttu-id="943d1-150">다시 시작-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="943d1-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="943d1-151">이력서-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="943d1-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="943d1-152">중지-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="943d1-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
