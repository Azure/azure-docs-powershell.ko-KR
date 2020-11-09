---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310931"
---
# <span data-ttu-id="947cb-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="947cb-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="947cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="947cb-102">SYNOPSIS</span></span>
<span data-ttu-id="947cb-103">일괄 처리 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="947cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="947cb-104">SYNTAX</span></span>

### <span data-ttu-id="947cb-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="947cb-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="947cb-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="947cb-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="947cb-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="947cb-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="947cb-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="947cb-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="947cb-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="947cb-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="947cb-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="947cb-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="947cb-111">설명은</span><span class="sxs-lookup"><span data-stu-id="947cb-111">DESCRIPTION</span></span>
<span data-ttu-id="947cb-112">**AzBatchNodeFileContent** Cmdlet은 Azure Batch node 파일을 가져와 파일 또는 스트림으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="947cb-113">예제의</span><span class="sxs-lookup"><span data-stu-id="947cb-113">EXAMPLES</span></span>

### <span data-ttu-id="947cb-114">예제 1: 작업과 연결 된 일괄 노드 파일 가져오기 및 파일 저장</span><span class="sxs-lookup"><span data-stu-id="947cb-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="947cb-115">이 명령은 StdOut.txt 이라는 노드 파일을 가져와 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 파일 경로에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="947cb-116">StdOut.txt 노드 파일은 ID Job01 있는 작업에 대 한 ID Task01 인 작업과 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="947cb-117">Get-AzBatchAccountKey cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="947cb-118">예제 2: 일괄 처리 노드 파일을 가져오고 파이프라인을 사용 하 여 지정 된 파일 경로에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="947cb-119">이 명령은 Get-AzBatchNodeFile cmdlet을 사용 하 여 StdErr.txt 라는 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="947cb-120">이 명령은 파이프라인 연산자를 사용 하 여 해당 파일을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="947cb-121">현재 cmdlet은 해당 파일을 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 파일 경로에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="947cb-122">StdOut.txt 노드 파일은 ID Job02 있는 작업에 대 한 ID Task02 인 작업과 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="947cb-123">예제 3: 작업과 연결 된 일괄 처리 노드 파일 가져오기 및 스트림으로 이동</span><span class="sxs-lookup"><span data-stu-id="947cb-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="947cb-124">첫 번째 명령은 New-Object cmdlet을 사용 하 여 스트림을 만든 다음 $Stream 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="947cb-125">두 번째 명령은 ID Job03 인 작업에 대해 ID Task11이 있는 작업에서 StdOut.txt 라는 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="947cb-126">이 명령은 $Stream에서 스트림으로 파일 내용을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="947cb-127">예제 4: 계산 노드에서 노드 파일 가져오기 및 저장</span><span class="sxs-lookup"><span data-stu-id="947cb-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="947cb-128">이 명령은 ID Pool01 있는 풀에서 ID ComputeNode01이 있는 compute 노드에서 Startup\StdOut.txt 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="947cb-129">이 명령은 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 파일 경로에 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="947cb-130">예제 5: 계산 노드에서 노드 파일 가져오기 및 파이프라인을 사용 하 여 저장</span><span class="sxs-lookup"><span data-stu-id="947cb-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="947cb-131">이 명령은 ID ComputeNode01이 있는 compute 노드의 Get-AzBatchNodeFile를 사용 하 여 Startup\StdOut.txt 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="947cb-132">계산 노드는 ID Pool01를 가진 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="947cb-133">명령이 현재 cmdlet에 해당 노드 파일을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="947cb-134">해당 cmdlet은 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 파일 경로에 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="947cb-135">예제 6: 계산 노드에서 노드 파일 가져오기 및 스트림으로 이동</span><span class="sxs-lookup"><span data-stu-id="947cb-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="947cb-136">첫 번째 명령은 New-Object cmdlet을 사용 하 여 스트림을 만든 다음 $Stream 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="947cb-137">두 번째 명령은 ID Pool01 있는 풀에서 ID ComputeNode01이 있는 compute 노드에서 StdOut.txt 이라는 이름의 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="947cb-138">이 명령은 $Stream에서 스트림으로 파일 내용을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="947cb-139">변수</span><span class="sxs-lookup"><span data-stu-id="947cb-139">PARAMETERS</span></span>

### <span data-ttu-id="947cb-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="947cb-140">-BatchContext</span></span>
<span data-ttu-id="947cb-141">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="947cb-142">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="947cb-143">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="947cb-144">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="947cb-145">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="947cb-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="947cb-146">-ByteRangeEnd</span></span>
<span data-ttu-id="947cb-147">다운로드할 바이트 범위의 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-147">The end of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="947cb-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="947cb-148">-ByteRangeStart</span></span>
<span data-ttu-id="947cb-149">다운로드할 바이트 범위의 시작 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-149">The start of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="947cb-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="947cb-150">-ComputeNodeId</span></span>
<span data-ttu-id="947cb-151">이 cmdlet이 반환 하는 노드 파일을 포함 하는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="947cb-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="947cb-152">-DefaultProfile</span></span>
<span data-ttu-id="947cb-153">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="947cb-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="947cb-154">-DestinationPath</span></span>
<span data-ttu-id="947cb-155">이 cmdlet이 노드 파일을 저장 하는 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-155">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="947cb-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="947cb-156">-DestinationStream</span></span>
<span data-ttu-id="947cb-157">이 cmdlet이 노드 파일 콘텐츠를 쓰는 스트림을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="947cb-158">이 cmdlet은이 스트림을 닫거나 되감을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-158">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="947cb-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="947cb-159">-InputObject</span></span>
<span data-ttu-id="947cb-160">이 cmdlet이 가져오는 파일을 **Psnodefile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="947cb-161">노드 파일 개체를 가져오려면 Get-AzBatchNodeFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="947cb-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="947cb-162">-JobId</span></span>
<span data-ttu-id="947cb-163">대상 작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-163">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="947cb-164">-Path</span><span class="sxs-lookup"><span data-stu-id="947cb-164">-Path</span></span>
<span data-ttu-id="947cb-165">다운로드할 노드 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-165">The path of the node file to download.</span></span>

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

### <span data-ttu-id="947cb-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="947cb-166">-PoolId</span></span>
<span data-ttu-id="947cb-167">이 cmdlet이 가져오는 노드 파일을 포함 하는 계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="947cb-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="947cb-168">-TaskId</span></span>
<span data-ttu-id="947cb-169">작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-169">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="947cb-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="947cb-170">CommonParameters</span></span>
<span data-ttu-id="947cb-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="947cb-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="947cb-172">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="947cb-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="947cb-173">입력</span><span class="sxs-lookup"><span data-stu-id="947cb-173">INPUTS</span></span>

### <span data-ttu-id="947cb-174">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="947cb-174">System.String</span></span>

### <span data-ttu-id="947cb-175">Microsoft.Azure.Commands.Batch. PSNodeFile 모델</span><span class="sxs-lookup"><span data-stu-id="947cb-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="947cb-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="947cb-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="947cb-177">출력</span><span class="sxs-lookup"><span data-stu-id="947cb-177">OUTPUTS</span></span>

### <span data-ttu-id="947cb-178">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="947cb-178">System.Void</span></span>

## <span data-ttu-id="947cb-179">상속자</span><span class="sxs-lookup"><span data-stu-id="947cb-179">NOTES</span></span>

## <span data-ttu-id="947cb-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="947cb-180">RELATED LINKS</span></span>

[<span data-ttu-id="947cb-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="947cb-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="947cb-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="947cb-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="947cb-183">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="947cb-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
