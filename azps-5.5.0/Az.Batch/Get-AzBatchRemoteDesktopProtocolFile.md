---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197100"
---
# <span data-ttu-id="d50d3-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="d50d3-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="d50d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d50d3-102">SYNOPSIS</span></span>
<span data-ttu-id="d50d3-103">계산 노드에서 RDP 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="d50d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="d50d3-104">SYNTAX</span></span>

### <span data-ttu-id="d50d3-105">Id_Path(기본값)</span><span class="sxs-lookup"><span data-stu-id="d50d3-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d50d3-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="d50d3-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d50d3-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="d50d3-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d50d3-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="d50d3-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d50d3-109">설명</span><span class="sxs-lookup"><span data-stu-id="d50d3-109">DESCRIPTION</span></span>
<span data-ttu-id="d50d3-110">**Get-AzBatchRemoteDesktopProtocolFile** cmdlet은 계산 노드에서 RDP(원격 데스크톱 프로토콜) 파일을 다운로드하여 파일 또는 사용자 제공 스트림으로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="d50d3-111">예제</span><span class="sxs-lookup"><span data-stu-id="d50d3-111">EXAMPLES</span></span>

### <span data-ttu-id="d50d3-112">예제 1: 지정된 계산 노드에서 RDP 파일 다운로드 및 파일 저장</span><span class="sxs-lookup"><span data-stu-id="d50d3-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="d50d3-113">이 명령은 ID Pool06이 있는 풀에 ID ComputeNode01이 있는 계산 노드에서 RDP 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d50d3-114">이 명령은 .rdp 파일을 C:\PowerShell\MyComputeNode.rdp로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="d50d3-115">Get-AzBatchAccountKey cmdlet을 사용하여 $Context 변수에 컨텍스트를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d50d3-116">예제 2: 계산 노드에서 RDP 파일 다운로드 및 파이프라인을 사용하여 파일 저장</span><span class="sxs-lookup"><span data-stu-id="d50d3-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="d50d3-117">이 명령은 ID Pool06이 있는 풀에 ComputeNode02 ID가 있는 계산 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d50d3-118">이 명령은 파이프라인 연산자를 사용하여 해당 계산 노드를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d50d3-119">현재 cmdlet은 계산 노드에서 .rpd 파일을 구한 다음, 콘텐츠를 C:\PowerShell\MyComputeNode02.rdp라는 파일로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="d50d3-120">예제 3: 지정된 계산 노드에서 RDP 파일을 다운로드하여 스트림으로 전송</span><span class="sxs-lookup"><span data-stu-id="d50d3-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="d50d3-121">첫 번째 명령은 New-Object cmdlet을 사용하여 스트림을 만든 다음, $Stream 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="d50d3-122">두 번째 명령은 ID Pool06이 있는 풀에 ID ComputeNode03이 있는 계산 노드에서 .rdp 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d50d3-123">이 명령은 파일 콘텐츠를 파일의 스트림으로 $Stream.</span><span class="sxs-lookup"><span data-stu-id="d50d3-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="d50d3-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d50d3-124">PARAMETERS</span></span>

### <span data-ttu-id="d50d3-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d50d3-125">-BatchContext</span></span>
<span data-ttu-id="d50d3-126">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d50d3-127">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d50d3-128">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d50d3-129">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d50d3-130">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d50d3-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d50d3-131">-ComputeNode</span></span>
<span data-ttu-id="d50d3-132">.rdp 파일이 지점을 지정하는 **PSComputeNode** 개체로 계산 노드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="d50d3-133">계산 노드 개체를 얻습니다. Get-AzBatchComputeNode cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d50d3-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="d50d3-134">-ComputeNodeId</span></span>
<span data-ttu-id="d50d3-135">.rdp 파일이 지점을 지정하는 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d50d3-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d50d3-136">-DefaultProfile</span></span>
<span data-ttu-id="d50d3-137">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d50d3-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="d50d3-138">-DestinationPath</span></span>
<span data-ttu-id="d50d3-139">이 cmdlet이 .rdp 파일을 저장하는 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d50d3-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="d50d3-140">-DestinationStream</span></span>
<span data-ttu-id="d50d3-141">이 cmdlet이 RDP 데이터를 지시하는 스트림을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="d50d3-142">이 cmdlet은 이 스트림을 닫거나 되감지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d50d3-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d50d3-143">-PoolId</span></span>
<span data-ttu-id="d50d3-144">이 cmdlet이 .rdp 파일을 얻을 계산 노드를 포함하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d50d3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d50d3-145">CommonParameters</span></span>
<span data-ttu-id="d50d3-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d50d3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d50d3-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d50d3-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d50d3-148">입력</span><span class="sxs-lookup"><span data-stu-id="d50d3-148">INPUTS</span></span>

### <span data-ttu-id="d50d3-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d50d3-149">System.String</span></span>

### <span data-ttu-id="d50d3-150">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d50d3-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="d50d3-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d50d3-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d50d3-152">출력</span><span class="sxs-lookup"><span data-stu-id="d50d3-152">OUTPUTS</span></span>

### <span data-ttu-id="d50d3-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="d50d3-153">System.Void</span></span>

## <span data-ttu-id="d50d3-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d50d3-154">NOTES</span></span>

## <span data-ttu-id="d50d3-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d50d3-155">RELATED LINKS</span></span>

[<span data-ttu-id="d50d3-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d50d3-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d50d3-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d50d3-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="d50d3-158">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d50d3-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
