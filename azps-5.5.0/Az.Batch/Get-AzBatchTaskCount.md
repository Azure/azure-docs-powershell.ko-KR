---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205224"
---
# <span data-ttu-id="88c5e-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="88c5e-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="88c5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="88c5e-103">지정된 작업에 대한 태스크 수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="88c5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="88c5e-104">SYNTAX</span></span>

### <span data-ttu-id="88c5e-105">ID</span><span class="sxs-lookup"><span data-stu-id="88c5e-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88c5e-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="88c5e-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88c5e-107">설명</span><span class="sxs-lookup"><span data-stu-id="88c5e-107">DESCRIPTION</span></span>
<span data-ttu-id="88c5e-108">**Get-AzBatchTaskCount** cmdlet은 Batch 작업에 대한 Azure Batch 태스크 수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="88c5e-109">*JobId* 매개 변수 또는 Job 매개 변수를 사용하여 *작업을 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="88c5e-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="88c5e-110">태스크 수는 활성, 실행 중 또는 완료된 작업 상태의 태스크 수와 성공 또는 실패한 태스크 수를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="88c5e-111">준비 상태의 작업은 실행 중으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="88c5e-112">validationStatus가 유효성 검사되지 않은 경우 Batch 서비스는 목록 작업 API에 보고된 태스크 상태와의 상태 수를 확인할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="88c5e-113">작업에 200,000개 이상의 태스크가 포함된 경우 validationStatus가 유효성 검사되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="88c5e-114">예제</span><span class="sxs-lookup"><span data-stu-id="88c5e-114">EXAMPLES</span></span>

### <span data-ttu-id="88c5e-115">예제 1: ID로 태스크 수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="88c5e-116">이 명령은 Job01에 대한 태스크 수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="88c5e-117">Get-AzBatchAccountKey cmdlet을 사용하여 $Context 변수에 컨텍스트를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="88c5e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88c5e-118">PARAMETERS</span></span>

### <span data-ttu-id="88c5e-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="88c5e-119">-BatchContext</span></span>
<span data-ttu-id="88c5e-120">Batch 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="88c5e-121">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="88c5e-122">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="88c5e-123">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="88c5e-124">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88c5e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c5e-125">-DefaultProfile</span></span>
<span data-ttu-id="88c5e-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88c5e-127">-Job</span><span class="sxs-lookup"><span data-stu-id="88c5e-127">-Job</span></span>
<span data-ttu-id="88c5e-128">이 cmdlet에서 얻을 수 있는 태스크가 포함된 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="88c5e-129">**PSCloudJob 개체를 얻습니다.** Get-AzBatchJob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88c5e-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="88c5e-130">-JobId</span></span>
<span data-ttu-id="88c5e-131">태스크 수를 구할 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c5e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c5e-132">CommonParameters</span></span>
<span data-ttu-id="88c5e-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88c5e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c5e-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88c5e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c5e-135">입력</span><span class="sxs-lookup"><span data-stu-id="88c5e-135">INPUTS</span></span>

### <span data-ttu-id="88c5e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="88c5e-136">System.String</span></span>

### <span data-ttu-id="88c5e-137">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="88c5e-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="88c5e-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="88c5e-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="88c5e-139">출력</span><span class="sxs-lookup"><span data-stu-id="88c5e-139">OUTPUTS</span></span>

### <span data-ttu-id="88c5e-140">Microsoft.Azure.Commands.Batch. Models.PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="88c5e-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="88c5e-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88c5e-141">NOTES</span></span>

## <span data-ttu-id="88c5e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88c5e-142">RELATED LINKS</span></span>

[<span data-ttu-id="88c5e-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="88c5e-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="88c5e-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="88c5e-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="88c5e-145">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="88c5e-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
