---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308159"
---
# <span data-ttu-id="a9d1a-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="a9d1a-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="a9d1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d1a-103">계산 노드에서 RDP 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="a9d1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9d1a-104">SYNTAX</span></span>

### <span data-ttu-id="a9d1a-105">Id_Path (기본값)</span><span class="sxs-lookup"><span data-stu-id="a9d1a-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d1a-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="a9d1a-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d1a-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="a9d1a-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d1a-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="a9d1a-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9d1a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a9d1a-109">DESCRIPTION</span></span>
<span data-ttu-id="a9d1a-110">**AzBatchRemoteDesktopProtocolFile** cmdlet은 계산 노드의 RDP (원격 데스크톱 프로토콜) 파일을 가져와 파일 또는 사용자가 제공한 스트림으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="a9d1a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a9d1a-111">EXAMPLES</span></span>

### <span data-ttu-id="a9d1a-112">예제 1: 지정 된 계산 노드에서 RDP 파일 가져오기 및 파일 저장</span><span class="sxs-lookup"><span data-stu-id="a9d1a-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="a9d1a-113">이 명령은 ID Pool06 있는 풀에서 ID ComputeNode01이 있는 compute 노드에서 RDP 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="a9d1a-114">이 명령은 .rdp 파일을 C:\PowerShell\MyComputeNode.rdp.로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="a9d1a-115">Get-AzBatchAccountKey cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a9d1a-116">예제 2: 계산 노드에서 RDP 파일 가져오기 및 파이프라인을 사용 하 여 파일 저장</span><span class="sxs-lookup"><span data-stu-id="a9d1a-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="a9d1a-117">이 명령은 ID Pool06 있는 풀에서 ID ComputeNode02이 있는 compute 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="a9d1a-118">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 대 한 계산 노드를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a9d1a-119">현재 cmdlet은 compute 노드에서 rpd 파일을 가져온 다음 해당 콘텐츠를 C:\PowerShell\MyComputeNode02.rdp. 라는 파일로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="a9d1a-120">예제 3: 지정 된 계산 노드에서 RDP 파일을 가져오고이를 스트림으로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="a9d1a-121">첫 번째 명령은 New-Object cmdlet을 사용 하 여 스트림을 만든 다음 $Stream 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="a9d1a-122">두 번째 명령은 ID Pool06 있는 풀에서 ID ComputeNode03이 있는 compute 노드에서 .rdp 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="a9d1a-123">이 명령은 $Stream에서 스트림으로 파일 내용을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="a9d1a-124">변수</span><span class="sxs-lookup"><span data-stu-id="a9d1a-124">PARAMETERS</span></span>

### <span data-ttu-id="a9d1a-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a9d1a-125">-BatchContext</span></span>
<span data-ttu-id="a9d1a-126">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a9d1a-127">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a9d1a-128">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a9d1a-129">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a9d1a-130">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a9d1a-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a9d1a-131">-ComputeNode</span></span>
<span data-ttu-id="a9d1a-132">**PSComputeNode** 개체 (.rdp 파일이 가리키는 연산 노드)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="a9d1a-133">계산 노드 개체를 가져오려면 Get-AzBatchComputeNode cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="a9d1a-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="a9d1a-134">-ComputeNodeId</span></span>
<span data-ttu-id="a9d1a-135">.Rdp 파일이 가리키는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="a9d1a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d1a-136">-DefaultProfile</span></span>
<span data-ttu-id="a9d1a-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9d1a-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="a9d1a-138">-DestinationPath</span></span>
<span data-ttu-id="a9d1a-139">이 cmdlet이 .rdp 파일을 저장 하는 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="a9d1a-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="a9d1a-140">-DestinationStream</span></span>
<span data-ttu-id="a9d1a-141">이 cmdlet이 RDP 데이터를 보내는 스트림을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="a9d1a-142">이 cmdlet은이 스트림을 닫거나 되감을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-142">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="a9d1a-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a9d1a-143">-PoolId</span></span>
<span data-ttu-id="a9d1a-144">이 cmdlet이 .rdp 파일을 가져오는 계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="a9d1a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d1a-145">CommonParameters</span></span>
<span data-ttu-id="a9d1a-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d1a-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a9d1a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d1a-148">입력</span><span class="sxs-lookup"><span data-stu-id="a9d1a-148">INPUTS</span></span>

### <span data-ttu-id="a9d1a-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a9d1a-149">System.String</span></span>

### <span data-ttu-id="a9d1a-150">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a9d1a-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="a9d1a-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a9d1a-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a9d1a-152">출력</span><span class="sxs-lookup"><span data-stu-id="a9d1a-152">OUTPUTS</span></span>

### <span data-ttu-id="a9d1a-153">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="a9d1a-153">System.Void</span></span>

## <span data-ttu-id="a9d1a-154">상속자</span><span class="sxs-lookup"><span data-stu-id="a9d1a-154">NOTES</span></span>

## <span data-ttu-id="a9d1a-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9d1a-155">RELATED LINKS</span></span>

[<span data-ttu-id="a9d1a-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a9d1a-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a9d1a-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a9d1a-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="a9d1a-158">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a9d1a-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
