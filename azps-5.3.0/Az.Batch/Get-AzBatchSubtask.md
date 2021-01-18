---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 4a1278734e6c9f40dc7495acb92f847d7b2cd32d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494132"
---
# <span data-ttu-id="05f4a-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="05f4a-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="05f4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="05f4a-103">지정된 작업의 하위 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="05f4a-104">구문</span><span class="sxs-lookup"><span data-stu-id="05f4a-104">SYNTAX</span></span>

### <span data-ttu-id="05f4a-105">ODataFilter(기본값)</span><span class="sxs-lookup"><span data-stu-id="05f4a-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05f4a-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="05f4a-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05f4a-107">설명</span><span class="sxs-lookup"><span data-stu-id="05f4a-107">DESCRIPTION</span></span>
<span data-ttu-id="05f4a-108">**Get-AzBatchSubtask** cmdlet은 지정된 작업에 대한 하위 작업 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="05f4a-109">하위 작업은 개별 작업에 대한 병렬 처리를 제공하고 작업 실행 및 진행 상황을 정확하게 모니터링할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="05f4a-110">예제</span><span class="sxs-lookup"><span data-stu-id="05f4a-110">EXAMPLES</span></span>

### <span data-ttu-id="05f4a-111">예제 1: 지정된 작업에 대한 모든 하위 작업 반환</span><span class="sxs-lookup"><span data-stu-id="05f4a-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="05f4a-112">이러한 명령은 id myTask를 사용하여 작업에 대한 모든 하위 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="05f4a-113">이를 위해 예제의 첫 번째 명령은 배치 계정 contosobatchaccount에 대한 계정 키에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="05f4a-114">이 개체 참조는 $context.</span><span class="sxs-lookup"><span data-stu-id="05f4a-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="05f4a-115">그런 다음, 두 번째 명령은 해당 개체 참조 및 **Get-AzBatchSubtask** cmdlet을 사용하여 job-01의 일부로 실행되는 태스크인 myTask에 대한 모든 하위 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="05f4a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05f4a-116">PARAMETERS</span></span>

### <span data-ttu-id="05f4a-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="05f4a-117">-BatchContext</span></span>
<span data-ttu-id="05f4a-118">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="05f4a-119">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="05f4a-120">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="05f4a-121">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="05f4a-122">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="05f4a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05f4a-123">-DefaultProfile</span></span>
<span data-ttu-id="05f4a-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05f4a-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="05f4a-125">-JobId</span></span>
<span data-ttu-id="05f4a-126">이 cmdlet을 포함하는 하위 작업을 포함하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="05f4a-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="05f4a-127">-MaxCount</span></span>
<span data-ttu-id="05f4a-128">반환할 하위의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="05f4a-129">0 이하의 값을 지정하는 경우 cmdlet은 상한을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="05f4a-130">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="05f4a-131">-Task</span><span class="sxs-lookup"><span data-stu-id="05f4a-131">-Task</span></span>
<span data-ttu-id="05f4a-132">이 cmdlet이 반환하는 하위 작업을 포함하는 작업에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="05f4a-133">이 개체 참조는 Get-AzBatchTask cmdlet을 사용하고 반환된 개체를 변수에 저장하여 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="05f4a-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="05f4a-134">-TaskId</span></span>
<span data-ttu-id="05f4a-135">이 cmdlet이 반환하는 하위 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="05f4a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f4a-136">CommonParameters</span></span>
<span data-ttu-id="05f4a-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="05f4a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f4a-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05f4a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f4a-139">입력</span><span class="sxs-lookup"><span data-stu-id="05f4a-139">INPUTS</span></span>

### <span data-ttu-id="05f4a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="05f4a-140">System.String</span></span>

### <span data-ttu-id="05f4a-141">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="05f4a-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="05f4a-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="05f4a-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="05f4a-143">출력</span><span class="sxs-lookup"><span data-stu-id="05f4a-143">OUTPUTS</span></span>

### <span data-ttu-id="05f4a-144">Microsoft.Azure.Commands.Batch. Models.PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="05f4a-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="05f4a-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="05f4a-145">NOTES</span></span>

## <span data-ttu-id="05f4a-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05f4a-146">RELATED LINKS</span></span>

[<span data-ttu-id="05f4a-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="05f4a-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


