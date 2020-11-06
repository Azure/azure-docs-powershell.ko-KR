---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 58bed6fda4040c1af48469f4aa85f717c26c898c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537883"
---
# <span data-ttu-id="a7a98-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="a7a98-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="a7a98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7a98-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a98-103">지정 된 작업의 하위 작업 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7a98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7a98-104">SYNTAX</span></span>

### <span data-ttu-id="a7a98-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="a7a98-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7a98-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="a7a98-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7a98-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a7a98-107">DESCRIPTION</span></span>
<span data-ttu-id="a7a98-108">**Get-AzureBatchSubtask 작업** cmdlet은 지정 된 작업에 대 한 하위 작업 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="a7a98-109">하위 작업은 개별 작업에 대 한 병렬 처리를 제공 하 고 작업 실행 및 진행률을 정밀 하 게 모니터링할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="a7a98-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a7a98-110">EXAMPLES</span></span>

### <span data-ttu-id="a7a98-111">예제 1: 지정 된 작업에 대 한 모든 하위 작업 반환</span><span class="sxs-lookup"><span data-stu-id="a7a98-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="a7a98-112">이러한 명령은 ID myTask를 사용 하 여 작업에 대 한 모든 하위 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="a7a98-113">이렇게 하려면 예제의 첫 번째 명령은 batch 계정 contosobatchaccount의 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="a7a98-114">이 개체 참조는 $context 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="a7a98-115">그런 다음 두 번째 명령은 해당 개체 참조와 **가져오기-AzureBatchSubtask 작업** cmdlet을 사용 하 여 작업 작업-01의 일부로 실행 되는 작업의 mytask에 대 한 모든 하위 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="a7a98-116">변수</span><span class="sxs-lookup"><span data-stu-id="a7a98-116">PARAMETERS</span></span>

### <span data-ttu-id="a7a98-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a7a98-117">-BatchContext</span></span>
<span data-ttu-id="a7a98-118">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a7a98-119">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a7a98-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="a7a98-120">-JobId</span></span>
<span data-ttu-id="a7a98-121">하위 작업이이 cmdlet을 가져올 작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-121">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7a98-122">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a7a98-122">-MaxCount</span></span>
<span data-ttu-id="a7a98-123">반환할 하위 작업의 최대 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-123">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="a7a98-124">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-124">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="a7a98-125">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-125">The default value is 1000.</span></span>

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

### <span data-ttu-id="a7a98-126">-작업</span><span class="sxs-lookup"><span data-stu-id="a7a98-126">-Task</span></span>
<span data-ttu-id="a7a98-127">이 cmdlet이 반환 하는 하위 작업을 포함 하는 작업에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-127">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="a7a98-128">이 개체 참조는 Get-AzureBatchTask cmdlet을 사용 하 여 만들고 반환 된 개체를 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-128">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="a7a98-129">-TaskId</span><span class="sxs-lookup"><span data-stu-id="a7a98-129">-TaskId</span></span>
<span data-ttu-id="a7a98-130">하위 작업이이 cmdlet이 반환 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-130">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="a7a98-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a98-131">-DefaultProfile</span></span>
<span data-ttu-id="a7a98-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7a98-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a98-133">CommonParameters</span></span>
<span data-ttu-id="a7a98-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a98-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a98-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a98-136">입력</span><span class="sxs-lookup"><span data-stu-id="a7a98-136">INPUTS</span></span>

### <span data-ttu-id="a7a98-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a7a98-137">BatchAccountContext</span></span>
<span data-ttu-id="a7a98-138">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a7a98-139">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="a7a98-139">PSCloudTask</span></span>
<span data-ttu-id="a7a98-140">' Task ' 매개 변수는 파이프라인에서 ' PSCloudTask ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-140">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="a7a98-141">출력</span><span class="sxs-lookup"><span data-stu-id="a7a98-141">OUTPUTS</span></span>

###  
<span data-ttu-id="a7a98-142">이 cmdlet은 **PSSubtaskInformation** 개체의 인스턴스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a98-142">This cmdlet returns instances of the **PSSubtaskInformation** object.</span></span>

## <span data-ttu-id="a7a98-143">상속자</span><span class="sxs-lookup"><span data-stu-id="a7a98-143">NOTES</span></span>

## <span data-ttu-id="a7a98-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7a98-144">RELATED LINKS</span></span>

[<span data-ttu-id="a7a98-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a7a98-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


