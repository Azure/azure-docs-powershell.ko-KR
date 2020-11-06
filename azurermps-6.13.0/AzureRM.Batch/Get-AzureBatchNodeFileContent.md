---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: c399c967fbff477d487a27e944929855e9268744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534468"
---
# <span data-ttu-id="ab126-101">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="ab126-101">Get-AzureBatchNodeFileContent</span></span>

## <span data-ttu-id="ab126-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab126-102">SYNOPSIS</span></span>
<span data-ttu-id="ab126-103">일괄 처리 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-103">Gets a Batch node file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab126-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab126-104">SYNTAX</span></span>

### <span data-ttu-id="ab126-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="ab126-105">Task_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab126-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="ab126-106">Task_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab126-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="ab126-107">ComputeNode_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab126-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="ab126-108">ComputeNode_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab126-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="ab126-109">InputObject_Path</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab126-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="ab126-110">InputObject_Stream</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab126-111">설명은</span><span class="sxs-lookup"><span data-stu-id="ab126-111">DESCRIPTION</span></span>
<span data-ttu-id="ab126-112">**AzureBatchNodeFileContent** Cmdlet은 Azure Batch node 파일을 가져와 파일 또는 스트림으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-112">The **Get-AzureBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="ab126-113">예제의</span><span class="sxs-lookup"><span data-stu-id="ab126-113">EXAMPLES</span></span>

### <span data-ttu-id="ab126-114">예제 1: 작업과 연결 된 일괄 노드 파일 가져오기 및 파일 저장</span><span class="sxs-lookup"><span data-stu-id="ab126-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="ab126-115">이 명령은 StdOut.txt 이라는 노드 파일을 가져와 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 파일 경로에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="ab126-116">StdOut.txt 노드 파일은 ID Job01 있는 작업에 대 한 ID Task01 인 작업과 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="ab126-117">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ab126-118">예제 2: 일괄 처리 노드 파일을 가져오고 파이프라인을 사용 하 여 지정 된 파일 경로에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="ab126-119">이 명령은 Get-AzureBatchNodeFile cmdlet을 사용 하 여 StdErr.txt 라는 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-119">This command gets the node file that is named StdErr.txt by using the Get-AzureBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="ab126-120">이 명령은 파이프라인 연산자를 사용 하 여 해당 파일을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ab126-121">현재 cmdlet은 해당 파일을 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 파일 경로에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="ab126-122">StdOut.txt 노드 파일은 ID Job02 있는 작업에 대 한 ID Task02 인 작업과 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="ab126-123">예제 3: 작업과 연결 된 일괄 처리 노드 파일 가져오기 및 스트림으로 이동</span><span class="sxs-lookup"><span data-stu-id="ab126-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="ab126-124">첫 번째 명령은 New-Object cmdlet을 사용 하 여 스트림을 만든 다음 $Stream 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="ab126-125">두 번째 명령은 ID Job03 인 작업에 대해 ID Task11이 있는 작업에서 StdOut.txt 라는 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="ab126-126">이 명령은 $Stream에서 스트림으로 파일 내용을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="ab126-127">예제 4: 계산 노드에서 노드 파일 가져오기 및 저장</span><span class="sxs-lookup"><span data-stu-id="ab126-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="ab126-128">이 명령은 ID Pool01 있는 풀에서 ID ComputeNode01이 있는 compute 노드에서 Startup\StdOut.txt 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="ab126-129">이 명령은 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 파일 경로에 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="ab126-130">예제 5: 계산 노드에서 노드 파일 가져오기 및 파이프라인을 사용 하 여 저장</span><span class="sxs-lookup"><span data-stu-id="ab126-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="ab126-131">이 명령은 ID ComputeNode01이 있는 compute 노드의 Get-AzureBatchNodeFile를 사용 하 여 Startup\StdOut.txt 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-131">This command gets the node file Startup\StdOut.txt by using Get-AzureBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="ab126-132">계산 노드는 ID Pool01를 가진 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="ab126-133">명령이 현재 cmdlet에 해당 노드 파일을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="ab126-134">해당 cmdlet은 로컬 컴퓨터의 E:\PowerShell\StdOut.txt 파일 경로에 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="ab126-135">예제 6: 계산 노드에서 노드 파일 가져오기 및 스트림으로 이동</span><span class="sxs-lookup"><span data-stu-id="ab126-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="ab126-136">첫 번째 명령은 New-Object cmdlet을 사용 하 여 스트림을 만든 다음 $Stream 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="ab126-137">두 번째 명령은 ID Pool01 있는 풀에서 ID ComputeNode01이 있는 compute 노드에서 StdOut.txt 이라는 이름의 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="ab126-138">이 명령은 $Stream에서 스트림으로 파일 내용을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="ab126-139">변수</span><span class="sxs-lookup"><span data-stu-id="ab126-139">PARAMETERS</span></span>

### <span data-ttu-id="ab126-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ab126-140">-BatchContext</span></span>
<span data-ttu-id="ab126-141">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ab126-142">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-142">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ab126-143">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-143">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ab126-144">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ab126-145">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ab126-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="ab126-146">-ByteRangeEnd</span></span>
<span data-ttu-id="ab126-147">다운로드할 바이트 범위의 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-147">The end of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="ab126-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="ab126-148">-ByteRangeStart</span></span>
<span data-ttu-id="ab126-149">다운로드할 바이트 범위의 시작 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-149">The start of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="ab126-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ab126-150">-ComputeNodeId</span></span>
<span data-ttu-id="ab126-151">이 cmdlet이 반환 하는 노드 파일을 포함 하는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="ab126-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab126-152">-DefaultProfile</span></span>
<span data-ttu-id="ab126-153">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab126-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="ab126-154">-DestinationPath</span></span>
<span data-ttu-id="ab126-155">이 cmdlet이 노드 파일을 저장 하는 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-155">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="ab126-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="ab126-156">-DestinationStream</span></span>
<span data-ttu-id="ab126-157">이 cmdlet이 노드 파일 콘텐츠를 쓰는 스트림을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="ab126-158">이 cmdlet은이 스트림을 닫거나 되감을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-158">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="ab126-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab126-159">-InputObject</span></span>
<span data-ttu-id="ab126-160">이 cmdlet이 가져오는 파일을 **Psnodefile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="ab126-161">노드 파일 개체를 가져오려면 Get-AzureBatchNodeFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-161">To obtain a node file object, use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="ab126-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="ab126-162">-JobId</span></span>
<span data-ttu-id="ab126-163">대상 작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-163">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="ab126-164">-Path</span><span class="sxs-lookup"><span data-stu-id="ab126-164">-Path</span></span>
<span data-ttu-id="ab126-165">다운로드할 노드 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-165">The path of the node file to download.</span></span>

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

### <span data-ttu-id="ab126-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ab126-166">-PoolId</span></span>
<span data-ttu-id="ab126-167">이 cmdlet이 가져오는 노드 파일을 포함 하는 계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ab126-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="ab126-168">-TaskId</span></span>
<span data-ttu-id="ab126-169">작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-169">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="ab126-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab126-170">CommonParameters</span></span>
<span data-ttu-id="ab126-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab126-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab126-172">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab126-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab126-173">입력</span><span class="sxs-lookup"><span data-stu-id="ab126-173">INPUTS</span></span>

### <span data-ttu-id="ab126-174">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ab126-174">System.String</span></span>

### <span data-ttu-id="ab126-175">Microsoft.Azure.Commands.Batch. PSNodeFile 모델</span><span class="sxs-lookup"><span data-stu-id="ab126-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>
<span data-ttu-id="ab126-176">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab126-176">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ab126-177">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ab126-177">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="ab126-178">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab126-178">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="ab126-179">출력</span><span class="sxs-lookup"><span data-stu-id="ab126-179">OUTPUTS</span></span>

### <span data-ttu-id="ab126-180">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ab126-180">System.Void</span></span>

## <span data-ttu-id="ab126-181">상속자</span><span class="sxs-lookup"><span data-stu-id="ab126-181">NOTES</span></span>

## <span data-ttu-id="ab126-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab126-182">RELATED LINKS</span></span>

[<span data-ttu-id="ab126-183">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ab126-183">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ab126-184">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="ab126-184">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="ab126-185">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab126-185">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


