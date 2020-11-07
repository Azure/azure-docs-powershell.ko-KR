---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
ms.openlocfilehash: 0a027bd15d4b207baf9c69fcb9104428c2881872
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704087"
---
# <span data-ttu-id="ae1ac-101">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="ae1ac-101">Get-AzureBatchNodeFile</span></span>

## <span data-ttu-id="ae1ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae1ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1ac-103">일괄 처리 노드 파일의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-103">Gets the properties of Batch node files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae1ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae1ac-104">SYNTAX</span></span>

### <span data-ttu-id="ae1ac-105">ComputeNode_Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="ae1ac-105">ComputeNode_Id (Default)</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Name] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae1ac-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="ae1ac-106">Task_Id</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [[-Name] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae1ac-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="ae1ac-107">Task_ODataFilter</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae1ac-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="ae1ac-108">ParentTask</span></span>
```
Get-AzureBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae1ac-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="ae1ac-109">ComputeNode_ODataFilter</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae1ac-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="ae1ac-110">ParentComputeNode</span></span>
```
Get-AzureBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae1ac-111">설명은</span><span class="sxs-lookup"><span data-stu-id="ae1ac-111">DESCRIPTION</span></span>
<span data-ttu-id="ae1ac-112">**Get-AzureBatchNodeFile** cmdlet은 작업 또는 계산 노드의 Azure 일괄 처리 노드 파일의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-112">The **Get-AzureBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="ae1ac-113">결과 범위를 좁히려면 OData (Open Data Protocol) 필터를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="ae1ac-114">작업을 지정 하지만 필터가 아닌 경우이 cmdlet은 해당 작업의 모든 노드 파일에 대 한 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="ae1ac-115">Compute 노드를 지정 하지만 필터가 아닌 경우이 cmdlet은 해당 계산 노드에 대 한 모든 노드 파일에 대 한 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="ae1ac-116">예제의</span><span class="sxs-lookup"><span data-stu-id="ae1ac-116">EXAMPLES</span></span>

### <span data-ttu-id="ae1ac-117">예제 1: 작업과 연결 된 노드 파일의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="ae1ac-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ae1ac-118">이 명령은 ID 작업이 000001 인 작업에서 ID Task26를 가진 작업과 연결 된 StdOut.txt 노드 파일의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="ae1ac-119">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-119">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ae1ac-120">예제 2: 필터를 사용 하 여 작업과 연결 된 노드 파일의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="ae1ac-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ae1ac-121">이 명령은 이름이 st로 시작 하는 노드 파일의 속성을 가져오고 ID 작업이 있는 작업 아래에 ID Task26 인 작업을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="ae1ac-122">예제 3: 작업과 연결 된 노드 파일의 속성을 재귀적으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="ae1ac-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzureBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzureBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ae1ac-123">이 명령은 job Job-00003 ID Task31를 가진 작업과 연결 된 모든 파일의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="ae1ac-124">이 명령은 *Recursive* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="ae1ac-125">따라서 cmdlet은 재귀적 파일 검색을 수행 하 고 wd\newFile.txt 노드 파일을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="ae1ac-126">예제 4: 계산 노드에서 단일 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="ae1ac-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ae1ac-127">이 명령은 ID Pool22 있는 풀에서 ID ComputeNode01이 있는 compute 노드에서 Startup\StdOut.txt 라는 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="ae1ac-128">예제 5: 계산 노드에서 폴더 아래의 모든 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="ae1ac-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ae1ac-129">이 명령은 ID Pool22 있는 풀에서 ID ComputeNode01를 가진 compute 노드의 시작 폴더 아래에 있는 모든 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="ae1ac-130">이 cmdlet은 *Recursive* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="ae1ac-131">예제 6: 계산 노드의 루트 폴더에서 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="ae1ac-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzureBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzureBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ae1ac-132">이 명령은 ID Pool22 있는 풀에서 ID ComputeNode01를 가진 compute 노드의 루트 폴더에 있는 모든 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="ae1ac-133">변수</span><span class="sxs-lookup"><span data-stu-id="ae1ac-133">PARAMETERS</span></span>

### <span data-ttu-id="ae1ac-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ae1ac-134">-BatchContext</span></span>
<span data-ttu-id="ae1ac-135">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ae1ac-136">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-136">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ae1ac-137">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ae1ac-137">-ComputeNode</span></span>
<span data-ttu-id="ae1ac-138">처리 노드 파일을 포함 하는 **PSComputeNode** 개체로 계산 노드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-138">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="ae1ac-139">계산 노드 개체를 가져오려면 Get-AzureBatchComputeNode cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-139">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentComputeNode
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1ac-140">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ae1ac-140">-ComputeNodeId</span></span>
<span data-ttu-id="ae1ac-141">일괄 처리 노드 파일을 포함 하는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-141">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1ac-142">-필터</span><span class="sxs-lookup"><span data-stu-id="ae1ac-142">-Filter</span></span>
<span data-ttu-id="ae1ac-143">OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-143">Specifies an OData filter clause.</span></span>
<span data-ttu-id="ae1ac-144">이 cmdlet은이 매개 변수에서 지정 하는 필터와 일치 하는 노드 파일의 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-144">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae1ac-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="ae1ac-145">-JobId</span></span>
<span data-ttu-id="ae1ac-146">대상 작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-146">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1ac-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ae1ac-147">-MaxCount</span></span>
<span data-ttu-id="ae1ac-148">이 cmdlet이 속성을 반환 하는 최대 노드 파일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-148">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="ae1ac-149">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-149">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ae1ac-150">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-150">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae1ac-151">-이름</span><span class="sxs-lookup"><span data-stu-id="ae1ac-151">-Name</span></span>
<span data-ttu-id="ae1ac-152">이 cmdlet이 속성을 검색 하는 노드 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-152">Specifies the name of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="ae1ac-153">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-153">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae1ac-154">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ae1ac-154">-PoolId</span></span>
<span data-ttu-id="ae1ac-155">노드 파일의 속성을 가져올 계산 노드가 포함 된 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-155">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1ac-156">-Recursive</span><span class="sxs-lookup"><span data-stu-id="ae1ac-156">-Recursive</span></span>
<span data-ttu-id="ae1ac-157">이 cmdlet이 재귀적 파일 목록을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-157">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="ae1ac-158">그렇지 않으면 루트 폴더에 있는 파일만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-158">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae1ac-159">-작업</span><span class="sxs-lookup"><span data-stu-id="ae1ac-159">-Task</span></span>
<span data-ttu-id="ae1ac-160">노드 파일이 연결 된 **Pscloudtask** 개체로 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-160">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="ae1ac-161">작업 개체를 가져오려면 Get-AzureBatchTask cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-161">To obtain a task object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentTask
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1ac-162">-TaskId</span><span class="sxs-lookup"><span data-stu-id="ae1ac-162">-TaskId</span></span>
<span data-ttu-id="ae1ac-163">이 cmdlet이 노드 파일의 속성을 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-163">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1ac-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae1ac-164">-DefaultProfile</span></span>
<span data-ttu-id="ae1ac-165">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae1ac-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1ac-166">CommonParameters</span></span>
<span data-ttu-id="ae1ac-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1ac-168">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae1ac-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1ac-169">입력</span><span class="sxs-lookup"><span data-stu-id="ae1ac-169">INPUTS</span></span>

### <span data-ttu-id="ae1ac-170">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ae1ac-170">BatchAccountContext</span></span>
<span data-ttu-id="ae1ac-171">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-171">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ae1ac-172">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ae1ac-172">PSComputeNode</span></span>
<span data-ttu-id="ae1ac-173">' ComputeNode ' 매개 변수는 파이프라인에서 ' PSComputeNode ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-173">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

### <span data-ttu-id="ae1ac-174">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="ae1ac-174">PSCloudTask</span></span>
<span data-ttu-id="ae1ac-175">' Task ' 매개 변수는 파이프라인에서 ' PSCloudTask ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-175">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="ae1ac-176">출력</span><span class="sxs-lookup"><span data-stu-id="ae1ac-176">OUTPUTS</span></span>

### <span data-ttu-id="ae1ac-177">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="ae1ac-177">PSNodeFile</span></span>

## <span data-ttu-id="ae1ac-178">상속자</span><span class="sxs-lookup"><span data-stu-id="ae1ac-178">NOTES</span></span>

## <span data-ttu-id="ae1ac-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae1ac-179">RELATED LINKS</span></span>

[<span data-ttu-id="ae1ac-180">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ae1ac-180">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ae1ac-181">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ae1ac-181">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="ae1ac-182">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="ae1ac-182">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="ae1ac-183">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ae1ac-183">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="ae1ac-184">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ae1ac-184">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


