---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: db8ef62a158edaa3a697af9f77e7932dfa18c096
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205277"
---
# <span data-ttu-id="dea11-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="dea11-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="dea11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dea11-102">SYNOPSIS</span></span>
<span data-ttu-id="dea11-103">Batch 노드 파일의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="dea11-104">구문</span><span class="sxs-lookup"><span data-stu-id="dea11-104">SYNTAX</span></span>

### <span data-ttu-id="dea11-105">ComputeNode_Id(기본값)</span><span class="sxs-lookup"><span data-stu-id="dea11-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dea11-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="dea11-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dea11-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="dea11-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dea11-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="dea11-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dea11-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="dea11-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dea11-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="dea11-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dea11-111">설명</span><span class="sxs-lookup"><span data-stu-id="dea11-111">DESCRIPTION</span></span>
<span data-ttu-id="dea11-112">**Get-AzBatchNodeFile** cmdlet은 태스크 또는 계산 노드의 Azure Batch 노드 파일의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="dea11-113">결과 범위를 좁히기 위해 OData(Open Data Protocol) 필터를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="dea11-114">필터가 아닌 태스크를 지정하면 이 cmdlet은 해당 태스크에 대한 모든 노드 파일에 대한 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="dea11-115">계산 노드를 지정하지만 필터는 지정하지 않으면 이 cmdlet은 해당 계산 노드에 대한 모든 노드 파일에 대한 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="dea11-116">예제</span><span class="sxs-lookup"><span data-stu-id="dea11-116">EXAMPLES</span></span>

### <span data-ttu-id="dea11-117">예제 1: 태스크와 연결된 노드 파일의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="dea11-118">이 명령은 ID job-000001이 있는 작업에 id task26이 있는 태스크와 연결된 StdOut.txt 노드 파일의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="dea11-119">Get-AzBatchAccountKey cmdlet을 사용하여 $Context 변수에 컨텍스트를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-119">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="dea11-120">예제 2: 필터를 사용하여 태스크와 연결된 노드 파일의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="dea11-121">이 명령은 이름이 st로 시작하고 ID Job-00002가 있는 작업에서 ID Task26이 있는 태스크와 연결된 노드 파일의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="dea11-122">예제 3: 태스크와 연결된 노드 파일의 속성을 재발적으로 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        wd                                                               https://cmdletexample.westus.Batch.contoso...
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="dea11-123">이 명령은 job-00003에서 ID Task31이 있는 태스크와 연결된 모든 파일의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="dea11-124">이 명령은 재발 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="dea11-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="dea11-125">따라서 cmdlet은 재귀 파일 검색을 수행하고 wd\newFile.txt 노드 파일을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="dea11-126">예제 4: 계산 노드에서 단일 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="dea11-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="dea11-127">이 명령은 ID Startup\StdOut.txt Pool22가 있는 풀에 ID ComputeNode01이 있는 계산 노드에서 이름이 지정되는 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="dea11-128">예제 5: 계산 노드에서 폴더의 모든 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="dea11-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso...
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="dea11-129">이 명령은 ID Pool22가 있는 풀에 ID ComputeNode01이 있는 계산 노드에서 시작 폴더의 모든 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="dea11-130">이 cmdlet은 재발 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="dea11-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="dea11-131">예제 6: 계산 노드의 루트 폴더에서 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="dea11-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso...
True        startup                         https://cmdletexample.westus.Batch.contoso...
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="dea11-132">이 명령은 ID Pool22가 있는 풀에 ID ComputeNode01이 있는 계산 노드의 루트 폴더에 있는 모든 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="dea11-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dea11-133">PARAMETERS</span></span>

### <span data-ttu-id="dea11-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dea11-134">-BatchContext</span></span>
<span data-ttu-id="dea11-135">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dea11-136">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dea11-137">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-137">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dea11-138">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dea11-139">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dea11-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="dea11-140">-ComputeNode</span></span>
<span data-ttu-id="dea11-141">Batch 노드 파일을 포함하는 계산 노드를 **PSComputeNode** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="dea11-142">계산 노드 개체를 얻습니다. Get-AzBatchComputeNode cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="dea11-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="dea11-143">-ComputeNodeId</span></span>
<span data-ttu-id="dea11-144">Batch 노드 파일을 포함하는 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

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

### <span data-ttu-id="dea11-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea11-145">-DefaultProfile</span></span>
<span data-ttu-id="dea11-146">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dea11-147">-Filter</span><span class="sxs-lookup"><span data-stu-id="dea11-147">-Filter</span></span>
<span data-ttu-id="dea11-148">OData 필터 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="dea11-149">이 cmdlet은 이 매개 변수가 지정하는 필터와 일치하는 노드 파일에 대한 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

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

### <span data-ttu-id="dea11-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="dea11-150">-JobId</span></span>
<span data-ttu-id="dea11-151">대상 태스크를 포함하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-151">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="dea11-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="dea11-152">-MaxCount</span></span>
<span data-ttu-id="dea11-153">이 cmdlet이 속성을 반환하는 노드 파일의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="dea11-154">0 이하의 값을 지정하는 경우 cmdlet은 상한을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="dea11-155">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-155">The default value is 1000.</span></span>

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

### <span data-ttu-id="dea11-156">-Path</span><span class="sxs-lookup"><span data-stu-id="dea11-156">-Path</span></span>
<span data-ttu-id="dea11-157">이 cmdlet이 속성을 검색하는 노드 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="dea11-158">와일드카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea11-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="dea11-159">-PoolId</span></span>
<span data-ttu-id="dea11-160">노드 파일의 속성을 얻을 계산 노드를 포함하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

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

### <span data-ttu-id="dea11-161">-Recursive</span><span class="sxs-lookup"><span data-stu-id="dea11-161">-Recursive</span></span>
<span data-ttu-id="dea11-162">이 cmdlet이 재귀 파일 목록을 반환하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="dea11-163">그렇지 않으면 루트 폴더의 파일만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-163">Otherwise, it returns only the files in the root folder.</span></span>

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

### <span data-ttu-id="dea11-164">-Task</span><span class="sxs-lookup"><span data-stu-id="dea11-164">-Task</span></span>
<span data-ttu-id="dea11-165">노드 파일이 연결된 **PSCloudTask** 개체로 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="dea11-166">작업 개체를 얻습니다. Get-AzBatchTask cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="dea11-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="dea11-167">-TaskId</span></span>
<span data-ttu-id="dea11-168">이 cmdlet이 노드 파일의 속성을 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

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

### <span data-ttu-id="dea11-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea11-169">CommonParameters</span></span>
<span data-ttu-id="dea11-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dea11-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea11-171">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dea11-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea11-172">입력</span><span class="sxs-lookup"><span data-stu-id="dea11-172">INPUTS</span></span>

### <span data-ttu-id="dea11-173">System.String</span><span class="sxs-lookup"><span data-stu-id="dea11-173">System.String</span></span>

### <span data-ttu-id="dea11-174">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="dea11-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="dea11-175">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="dea11-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="dea11-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dea11-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dea11-177">출력</span><span class="sxs-lookup"><span data-stu-id="dea11-177">OUTPUTS</span></span>

### <span data-ttu-id="dea11-178">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="dea11-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="dea11-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dea11-179">NOTES</span></span>

## <span data-ttu-id="dea11-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dea11-180">RELATED LINKS</span></span>

[<span data-ttu-id="dea11-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="dea11-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="dea11-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="dea11-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="dea11-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="dea11-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="dea11-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="dea11-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="dea11-185">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dea11-185">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
