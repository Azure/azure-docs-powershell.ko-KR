---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213705"
---
# <span data-ttu-id="386e8-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="386e8-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="386e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="386e8-102">SYNOPSIS</span></span>
<span data-ttu-id="386e8-103">지정 된 작업에 대 한 작업 개수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="386e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="386e8-104">SYNTAX</span></span>

### <span data-ttu-id="386e8-105">I</span><span class="sxs-lookup"><span data-stu-id="386e8-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="386e8-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="386e8-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="386e8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="386e8-107">DESCRIPTION</span></span>
<span data-ttu-id="386e8-108">**AzBatchTaskCount** Cmdlet은 일괄 작업에 대 한 Azure 일괄 처리 작업 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="386e8-109">*JobId* 매개 변수 또는 *작업* 매개 변수 중 하나를 통해 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="386e8-110">작업 수는 활성, 진행 중 또는 완료 된 작업 상태와 성공 또는 실패 한 작업의 수를 기준으로 작업 개수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="386e8-111">준비 상태의 작업은 실행 중으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="386e8-112">ValidationStatus가 unvalidated 인 경우 일괄 처리 서비스는 목록 작업 API에 보고 된 대로 작업 상태에 대 한 상태 개수를 확인할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="386e8-113">작업에 20만 이상의 작업이 포함 된 경우에는 validationStatus unvalidated 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="386e8-114">예제의</span><span class="sxs-lookup"><span data-stu-id="386e8-114">EXAMPLES</span></span>

### <span data-ttu-id="386e8-115">예제 1: ID 별 작업 개수 가져오기</span><span class="sxs-lookup"><span data-stu-id="386e8-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="386e8-116">이 명령은 job Job01의 작업 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="386e8-117">Get-AzBatchAccountKey cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="386e8-118">변수</span><span class="sxs-lookup"><span data-stu-id="386e8-118">PARAMETERS</span></span>

### <span data-ttu-id="386e8-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="386e8-119">-BatchContext</span></span>
<span data-ttu-id="386e8-120">일괄 처리 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="386e8-121">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="386e8-122">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="386e8-123">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="386e8-124">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="386e8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386e8-125">-DefaultProfile</span></span>
<span data-ttu-id="386e8-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="386e8-127">-작업</span><span class="sxs-lookup"><span data-stu-id="386e8-127">-Job</span></span>
<span data-ttu-id="386e8-128">이 cmdlet이 가져오는 작업을 포함 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="386e8-129">**Pscloudjob** 개체를 가져오려면 Get-AzBatchJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="386e8-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="386e8-130">-JobId</span></span>
<span data-ttu-id="386e8-131">작업 개수를 가져올 작업의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="386e8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386e8-132">CommonParameters</span></span>
<span data-ttu-id="386e8-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="386e8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="386e8-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="386e8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386e8-135">입력</span><span class="sxs-lookup"><span data-stu-id="386e8-135">INPUTS</span></span>

### <span data-ttu-id="386e8-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="386e8-136">System.String</span></span>

### <span data-ttu-id="386e8-137">Microsoft.Azure.Commands.Batch. PSCloudJob 모델</span><span class="sxs-lookup"><span data-stu-id="386e8-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="386e8-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="386e8-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="386e8-139">출력</span><span class="sxs-lookup"><span data-stu-id="386e8-139">OUTPUTS</span></span>

### <span data-ttu-id="386e8-140">Microsoft.Azure.Commands.Batch. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="386e8-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="386e8-141">상속자</span><span class="sxs-lookup"><span data-stu-id="386e8-141">NOTES</span></span>

## <span data-ttu-id="386e8-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="386e8-142">RELATED LINKS</span></span>

[<span data-ttu-id="386e8-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="386e8-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="386e8-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="386e8-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="386e8-145">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="386e8-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
