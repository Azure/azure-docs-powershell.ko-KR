---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338769"
---
# <span data-ttu-id="a7e13-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="a7e13-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="a7e13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7e13-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e13-103">Batch 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="a7e13-104">구문</span><span class="sxs-lookup"><span data-stu-id="a7e13-104">SYNTAX</span></span>

### <span data-ttu-id="a7e13-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="a7e13-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7e13-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="a7e13-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7e13-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="a7e13-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7e13-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="a7e13-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7e13-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="a7e13-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7e13-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="a7e13-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7e13-111">설명</span><span class="sxs-lookup"><span data-stu-id="a7e13-111">DESCRIPTION</span></span>
<span data-ttu-id="a7e13-112">**Get-AzBatchNodeFileContent** cmdlet은 Azure Batch 노드 파일을 다운로드하여 파일 또는 스트림으로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="a7e13-113">예제</span><span class="sxs-lookup"><span data-stu-id="a7e13-113">EXAMPLES</span></span>

### <span data-ttu-id="a7e13-114">예제 1: 태스크와 연결된 Batch 노드 파일을 다운로드하고 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a7e13-115">이 명령은 로컬 컴퓨터의 StdOut.txt 노드 파일을 E:\PowerShell\StdOut.txt 파일 경로에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="a7e13-116">StdOut.txt 노드 파일은 ID Job01이 있는 작업에 대한 ID Task01이 있는 태스크와 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="a7e13-117">Get-AzBatchAccountKey cmdlet을 사용하여 $Context 변수에 컨텍스트를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a7e13-118">예제 2: Batch 노드 파일을 다운로드하고 파이프라인을 사용하여 지정된 파일 경로에 저장</span><span class="sxs-lookup"><span data-stu-id="a7e13-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a7e13-119">이 명령은 Get-AzBatchNodeFile cmdlet을 사용하여 StdErr.txt 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="a7e13-120">이 명령은 파이프라인 연산자를 사용하여 해당 파일을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a7e13-121">현재 cmdlet은 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 파일 경로에 해당 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="a7e13-122">StdOut.txt 노드 파일은 ID Job02가 있는 작업에 대한 ID Task02가 있는 태스크와 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="a7e13-123">예제 3: 태스크와 연결된 Batch 노드 파일을 다운로드하여 스트림으로 전송</span><span class="sxs-lookup"><span data-stu-id="a7e13-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="a7e13-124">첫 번째 명령은 New-Object cmdlet을 사용하여 스트림을 만든 다음, $Stream 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="a7e13-125">두 번째 명령은 ID Job03이 StdOut.txt 작업의 ID Task11이 있는 태스크에서 이름이 지정되는 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="a7e13-126">이 명령은 파일 콘텐츠를 파일의 스트림으로 $Stream.</span><span class="sxs-lookup"><span data-stu-id="a7e13-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="a7e13-127">예제 4: 계산 노드에서 노드 파일 다운로드 및 저장</span><span class="sxs-lookup"><span data-stu-id="a7e13-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a7e13-128">이 명령은 ID Startup\StdOut.txt Pool01이 있는 풀에 ID ComputeNode01이 있는 계산 노드에서 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="a7e13-129">이 명령은 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 경로에 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="a7e13-130">예제 5: 계산 노드에서 노드 파일을 다운로드하고 파이프라인을 사용하여 저장</span><span class="sxs-lookup"><span data-stu-id="a7e13-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a7e13-131">이 명령은 computeNode01이 Startup\StdOut.txt 계산 Get-AzBatchNodeFile 사용하여 노드 파일을 Get-AzBatchNodeFile 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="a7e13-132">계산 노드는 ID Pool01이 있는 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="a7e13-133">이 명령은 해당 노드 파일을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="a7e13-134">이 cmdlet은 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 파일 경로에 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="a7e13-135">예제 6: 계산 노드에서 노드 파일을 다운로드하여 스트림으로 전송</span><span class="sxs-lookup"><span data-stu-id="a7e13-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="a7e13-136">첫 번째 명령은 New-Object cmdlet을 사용하여 스트림을 만든 다음, $Stream 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="a7e13-137">두 번째 명령은 ID pool01이 StdOut.txt ComputeNode01이 있는 계산 노드에서 이름이 지정되는 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="a7e13-138">이 명령은 파일 콘텐츠를 파일의 스트림으로 $Stream.</span><span class="sxs-lookup"><span data-stu-id="a7e13-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="a7e13-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7e13-139">PARAMETERS</span></span>

### <span data-ttu-id="a7e13-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a7e13-140">-BatchContext</span></span>
<span data-ttu-id="a7e13-141">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a7e13-142">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a7e13-143">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a7e13-144">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a7e13-145">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a7e13-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="a7e13-146">-ByteRangeEnd</span></span>
<span data-ttu-id="a7e13-147">다운로드할 byte 범위의 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-147">The end of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="a7e13-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="a7e13-148">-ByteRangeStart</span></span>
<span data-ttu-id="a7e13-149">다운로드할 byte 범위의 시작입니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-149">The start of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="a7e13-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="a7e13-150">-ComputeNodeId</span></span>
<span data-ttu-id="a7e13-151">이 cmdlet이 반환하는 노드 파일을 포함하는 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="a7e13-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e13-152">-DefaultProfile</span></span>
<span data-ttu-id="a7e13-153">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7e13-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="a7e13-154">-DestinationPath</span></span>
<span data-ttu-id="a7e13-155">이 cmdlet이 노드 파일을 저장하는 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-155">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="a7e13-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="a7e13-156">-DestinationStream</span></span>
<span data-ttu-id="a7e13-157">이 cmdlet이 노드 파일 콘텐츠를 쓰는 스트림을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="a7e13-158">이 cmdlet은 이 스트림을 닫거나 되감지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-158">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="a7e13-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7e13-159">-InputObject</span></span>
<span data-ttu-id="a7e13-160">이 cmdlet이 다운로드하는 파일을 **PSNodeFile** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="a7e13-161">노드 파일 개체를 얻습니다. Get-AzBatchNodeFile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="a7e13-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="a7e13-162">-JobId</span></span>
<span data-ttu-id="a7e13-163">대상 태스크를 포함하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-163">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="a7e13-164">-Path</span><span class="sxs-lookup"><span data-stu-id="a7e13-164">-Path</span></span>
<span data-ttu-id="a7e13-165">다운로드할 노드 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-165">The path of the node file to download.</span></span>

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

### <span data-ttu-id="a7e13-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a7e13-166">-PoolId</span></span>
<span data-ttu-id="a7e13-167">이 cmdlet에서 얻을 노드 파일을 포함하는 계산 노드를 포함하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7e13-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="a7e13-168">-TaskId</span></span>
<span data-ttu-id="a7e13-169">작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-169">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="a7e13-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e13-170">CommonParameters</span></span>
<span data-ttu-id="a7e13-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e13-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e13-172">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a7e13-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e13-173">입력</span><span class="sxs-lookup"><span data-stu-id="a7e13-173">INPUTS</span></span>

### <span data-ttu-id="a7e13-174">System.String</span><span class="sxs-lookup"><span data-stu-id="a7e13-174">System.String</span></span>

### <span data-ttu-id="a7e13-175">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="a7e13-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="a7e13-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a7e13-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a7e13-177">출력</span><span class="sxs-lookup"><span data-stu-id="a7e13-177">OUTPUTS</span></span>

### <span data-ttu-id="a7e13-178">System.Void</span><span class="sxs-lookup"><span data-stu-id="a7e13-178">System.Void</span></span>

## <span data-ttu-id="a7e13-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a7e13-179">NOTES</span></span>

## <span data-ttu-id="a7e13-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7e13-180">RELATED LINKS</span></span>

[<span data-ttu-id="a7e13-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a7e13-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a7e13-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="a7e13-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="a7e13-183">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a7e13-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
