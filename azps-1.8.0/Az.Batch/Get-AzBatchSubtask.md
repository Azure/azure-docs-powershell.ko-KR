---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 463f19b5ed459f0c2b2f4a4fdeff40bf69db2682
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701465"
---
# <span data-ttu-id="16d6f-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="16d6f-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="16d6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="16d6f-103">지정 된 작업의 하위 작업 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="16d6f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16d6f-104">SYNTAX</span></span>

### <span data-ttu-id="16d6f-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="16d6f-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d6f-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="16d6f-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16d6f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="16d6f-107">DESCRIPTION</span></span>
<span data-ttu-id="16d6f-108">**AzBatchSubtask** cmdlet은 지정 된 작업에 대 한 하위 작업 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="16d6f-109">하위 작업은 개별 작업에 대 한 병렬 처리를 제공 하 고 작업 실행 및 진행률을 정밀 하 게 모니터링할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="16d6f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="16d6f-110">EXAMPLES</span></span>

### <span data-ttu-id="16d6f-111">예제 1: 지정 된 작업에 대 한 모든 하위 작업 반환</span><span class="sxs-lookup"><span data-stu-id="16d6f-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="16d6f-112">이러한 명령은 ID myTask를 사용 하 여 작업에 대 한 모든 하위 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="16d6f-113">이렇게 하려면 예제의 첫 번째 명령은 batch 계정 contosobatchaccount의 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="16d6f-114">이 개체 참조는 $context 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="16d6f-115">그런 다음 두 번째 명령은 해당 개체 참조 및 **AzBatchSubtask** cmdlet을 사용 하 여 작업 작업의 일부로 실행 되는 mytask의 모든 하위 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="16d6f-116">변수</span><span class="sxs-lookup"><span data-stu-id="16d6f-116">PARAMETERS</span></span>

### <span data-ttu-id="16d6f-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="16d6f-117">-BatchContext</span></span>
<span data-ttu-id="16d6f-118">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="16d6f-119">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="16d6f-120">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="16d6f-121">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="16d6f-122">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="16d6f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d6f-123">-DefaultProfile</span></span>
<span data-ttu-id="16d6f-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16d6f-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="16d6f-125">-JobId</span></span>
<span data-ttu-id="16d6f-126">하위 작업이이 cmdlet을 가져올 작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d6f-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="16d6f-127">-MaxCount</span></span>
<span data-ttu-id="16d6f-128">반환할 하위 작업의 최대 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="16d6f-129">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="16d6f-130">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-130">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d6f-131">-작업</span><span class="sxs-lookup"><span data-stu-id="16d6f-131">-Task</span></span>
<span data-ttu-id="16d6f-132">이 cmdlet이 반환 하는 하위 작업을 포함 하는 작업에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="16d6f-133">이 개체 참조는 Get-AzBatchTask cmdlet을 사용 하 여 만들고 반환 된 개체를 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16d6f-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="16d6f-134">-TaskId</span></span>
<span data-ttu-id="16d6f-135">하위 작업이이 cmdlet이 반환 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d6f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d6f-136">CommonParameters</span></span>
<span data-ttu-id="16d6f-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d6f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d6f-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d6f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d6f-139">입력</span><span class="sxs-lookup"><span data-stu-id="16d6f-139">INPUTS</span></span>

### <span data-ttu-id="16d6f-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="16d6f-140">System.String</span></span>

### <span data-ttu-id="16d6f-141">Microsoft.Azure.Commands.Batch. PSCloudTask에 대 한 모델</span><span class="sxs-lookup"><span data-stu-id="16d6f-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="16d6f-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="16d6f-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="16d6f-143">출력</span><span class="sxs-lookup"><span data-stu-id="16d6f-143">OUTPUTS</span></span>

### <span data-ttu-id="16d6f-144">Microsoft.Azure.Commands.Batch. PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="16d6f-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="16d6f-145">상속자</span><span class="sxs-lookup"><span data-stu-id="16d6f-145">NOTES</span></span>

## <span data-ttu-id="16d6f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16d6f-146">RELATED LINKS</span></span>

[<span data-ttu-id="16d6f-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="16d6f-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


