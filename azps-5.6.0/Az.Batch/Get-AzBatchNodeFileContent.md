---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 5790d217a63b7c2ef3aa7011d5f8a708df1dfbac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983456"
---
# <span data-ttu-id="14839-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="14839-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="14839-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14839-102">SYNOPSIS</span></span>
<span data-ttu-id="14839-103">Batch 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14839-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="14839-104">구문</span><span class="sxs-lookup"><span data-stu-id="14839-104">SYNTAX</span></span>

### <span data-ttu-id="14839-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="14839-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14839-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="14839-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14839-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="14839-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14839-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="14839-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14839-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="14839-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14839-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="14839-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14839-111">설명</span><span class="sxs-lookup"><span data-stu-id="14839-111">DESCRIPTION</span></span>
<span data-ttu-id="14839-112">**Get-AzBatchNodeFileContent** cmdlet은 Azure Batch 노드 파일을 얻게 하여 파일 또는 스트림으로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="14839-113">예제</span><span class="sxs-lookup"><span data-stu-id="14839-113">EXAMPLES</span></span>

### <span data-ttu-id="14839-114">예제 1: 태스크와 연결된 Batch 노드 파일 다운로드 및 파일 저장</span><span class="sxs-lookup"><span data-stu-id="14839-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="14839-115">이 명령은 이름의 노드 파일을 StdOut.txt 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 경로에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="14839-116">StdOut.txt 노드 파일은 ID Job01이 있는 작업에 대한 ID Task01이 있는 작업과 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="14839-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="14839-117">Get-AzBatchAccountKey cmdlet을 사용하여 변수 변수에 컨텍스트를 $Context 합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="14839-118">예제 2: Batch 노드 파일을 다운로드하고 파이프라인을 사용하여 지정된 파일 경로에 저장</span><span class="sxs-lookup"><span data-stu-id="14839-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="14839-119">이 명령은 StdErr.txt cmdlet을 사용하여 Get-AzBatchNodeFile 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14839-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="14839-120">명령은 파이프라인 연산자를 사용하여 해당 파일을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="14839-121">현재 cmdlet은 해당 파일을 로컬 E:\PowerShell\StdOut.txt 파일 경로에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="14839-122">StdOut.txt 노드 파일은 ID Job02가 있는 작업에 대한 ID Task02가 있는 작업과 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="14839-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="14839-123">예제 3: 태스크와 연결된 Batch 노드 파일을 다운로드하고 스트림으로 연결</span><span class="sxs-lookup"><span data-stu-id="14839-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="14839-124">첫 번째 명령은 New-Object cmdlet을 사용하여 스트림을 만든 다음, $Stream 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="14839-125">두 번째 명령은 ID Job03이 StdOut.txt 작업에 대한 ID Task11이 있는 작업에서 이름의 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14839-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="14839-126">명령은 파일 콘텐츠를 해당 스트림에 $Stream.</span><span class="sxs-lookup"><span data-stu-id="14839-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="14839-127">예제 4: 계산 노드에서 노드 파일 다운로드 및 저장</span><span class="sxs-lookup"><span data-stu-id="14839-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="14839-128">이 명령은 id pool01이 Startup\StdOut.txt 풀에 ID ComputeNode01이 있는 계산 노드에서 노드 파일을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="14839-129">명령은 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 파일 경로에 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="14839-130">예제 5: 계산 노드에서 노드 파일을 다운로드하고 파이프라인을 사용하여 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="14839-131">이 명령은 id ComputeNode01이 Startup\StdOut.txt Get-AzBatchNodeFile 노드에서 노드 파일을 Get-AzBatchNodeFile 파일을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="14839-132">계산 노드는 ID Pool01이 있는 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14839-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="14839-133">명령은 해당 노드 파일을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="14839-134">해당 cmdlet은 파일을 로컬 E:\PowerShell\StdOut.txt 파일 경로에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="14839-135">예제 6: 계산 노드에서 노드 파일을 다운로드하고 스트림으로 연결</span><span class="sxs-lookup"><span data-stu-id="14839-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="14839-136">첫 번째 명령은 New-Object cmdlet을 사용하여 스트림을 만든 다음, $Stream 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="14839-137">두 번째 명령은 ID pool01이 StdOut.txt 풀에 ID ComputeNode01이 있는 계산 노드에서 이름의 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14839-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="14839-138">명령은 파일 콘텐츠를 해당 스트림에 $Stream.</span><span class="sxs-lookup"><span data-stu-id="14839-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="14839-139">매개 변수</span><span class="sxs-lookup"><span data-stu-id="14839-139">PARAMETERS</span></span>

### <span data-ttu-id="14839-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="14839-140">-BatchContext</span></span>
<span data-ttu-id="14839-141">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="14839-142">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="14839-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="14839-143">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14839-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="14839-144">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="14839-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="14839-145">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="14839-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="14839-146">-ByteRangeEnd</span></span>
<span data-ttu-id="14839-147">다운로드할 byte 범위의 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="14839-147">The end of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14839-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="14839-148">-ByteRangeStart</span></span>
<span data-ttu-id="14839-149">다운로드할 byte 범위의 시작입니다.</span><span class="sxs-lookup"><span data-stu-id="14839-149">The start of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14839-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="14839-150">-ComputeNodeId</span></span>
<span data-ttu-id="14839-151">이 cmdlet이 반환하는 노드 파일이 포함된 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14839-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14839-152">-DefaultProfile</span></span>
<span data-ttu-id="14839-153">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14839-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14839-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="14839-154">-DestinationPath</span></span>
<span data-ttu-id="14839-155">이 cmdlet이 노드 파일을 저장하는 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14839-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="14839-156">-DestinationStream</span></span>
<span data-ttu-id="14839-157">이 cmdlet이 노드 파일 내용을 쓰는 스트림을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="14839-158">이 cmdlet은 이 스트림을 닫거나 되감기하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14839-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14839-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14839-159">-InputObject</span></span>
<span data-ttu-id="14839-160">**PSNodeFile** 개체로 이 cmdlet이 얻을 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="14839-161">노드 파일 개체를 얻으면 Get-AzBatchNodeFile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14839-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="14839-162">-JobId</span></span>
<span data-ttu-id="14839-163">대상 작업을 포함하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14839-164">-Path</span><span class="sxs-lookup"><span data-stu-id="14839-164">-Path</span></span>
<span data-ttu-id="14839-165">다운로드할 노드 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="14839-165">The path of the node file to download.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14839-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="14839-166">-PoolId</span></span>
<span data-ttu-id="14839-167">이 cmdlet에서 얻을 노드 파일이 포함된 계산 노드가 포함된 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14839-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="14839-168">-TaskId</span></span>
<span data-ttu-id="14839-169">작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-169">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14839-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14839-170">CommonParameters</span></span>
<span data-ttu-id="14839-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14839-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14839-172">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14839-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14839-173">입력</span><span class="sxs-lookup"><span data-stu-id="14839-173">INPUTS</span></span>

### <span data-ttu-id="14839-174">System.String</span><span class="sxs-lookup"><span data-stu-id="14839-174">System.String</span></span>

### <span data-ttu-id="14839-175">Microsoft.Azure.Commands.Bat. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="14839-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="14839-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="14839-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="14839-177">출력</span><span class="sxs-lookup"><span data-stu-id="14839-177">OUTPUTS</span></span>

### <span data-ttu-id="14839-178">System.Void</span><span class="sxs-lookup"><span data-stu-id="14839-178">System.Void</span></span>

## <span data-ttu-id="14839-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14839-179">NOTES</span></span>

## <span data-ttu-id="14839-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14839-180">RELATED LINKS</span></span>

[<span data-ttu-id="14839-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="14839-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="14839-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="14839-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="14839-183">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="14839-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
