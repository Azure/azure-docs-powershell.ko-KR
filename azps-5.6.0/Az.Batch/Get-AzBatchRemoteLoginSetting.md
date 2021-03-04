---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 9cb2207381e7f874884bc53b5b85572fdffbd1a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952843"
---
# <span data-ttu-id="c5051-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="c5051-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="c5051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5051-102">SYNOPSIS</span></span>
<span data-ttu-id="c5051-103">계산 노드에 대한 원격 로그온 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="c5051-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5051-104">SYNTAX</span></span>

### <span data-ttu-id="c5051-105">ID(기본값)</span><span class="sxs-lookup"><span data-stu-id="c5051-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5051-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c5051-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5051-107">설명</span><span class="sxs-lookup"><span data-stu-id="c5051-107">DESCRIPTION</span></span>
<span data-ttu-id="c5051-108">**Get-AzBatchRemoteLoginSetting** cmdlet은 가상 머신 인프라 기반 풀의 계산 노드에 대한 원격 로그온 설정을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="c5051-109">예제</span><span class="sxs-lookup"><span data-stu-id="c5051-109">EXAMPLES</span></span>

### <span data-ttu-id="c5051-110">예제 1: 풀의 모든 노드에 대한 원격 로그온 설정 사용</span><span class="sxs-lookup"><span data-stu-id="c5051-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="c5051-111">첫 번째 명령은 **Get-AzBatchAccountKey** 를 사용하여 구독에 대한 액세스 키를 포함하는 일괄 처리 계정 컨텍스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="c5051-112">명령은 다음 명령에서 사용할 $Context 변수에 컨텍스트를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="c5051-113">두 번째 명령은 **Get-AzBatchComputeNode** 를 사용하여 ID ContosoPool이 있는 풀의 각 계산 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="c5051-114">명령은 파이프라인 연산자를 사용하여 각 컴퓨터 노드를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c5051-115">명령은 각 계산 노드에 대한 원격 로그온 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="c5051-116">예제 2: 노드에 대한 원격 로그온 설정 얻기</span><span class="sxs-lookup"><span data-stu-id="c5051-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="c5051-117">첫 번째 명령은 구독에 대한 액세스 키를 포함하는 일괄 처리 계정 컨텍스트를 얻은 다음, $Context 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="c5051-118">두 번째 명령은 ID ContosoPool이 있는 풀에 지정된 ID가 있는 계산 노드에 대한 원격 로그온 설정을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="c5051-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c5051-119">PARAMETERS</span></span>

### <span data-ttu-id="c5051-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c5051-120">-BatchContext</span></span>
<span data-ttu-id="c5051-121">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c5051-122">구독에 대한 액세스 키가 포함된 **BatchAccountContext를** 얻하려면 Get-AzBatchAccountKey cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="c5051-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

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

### <span data-ttu-id="c5051-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c5051-123">-ComputeNode</span></span>
<span data-ttu-id="c5051-124">이 cmdlet은 원격 로그온 설정을 얻을 수 있는 **PSComputeNode** 개체로 계산 노드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="c5051-125">계산 노드 개체를 얻으면 Get-AzBatchComputeNode cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5051-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c5051-126">-ComputeNodeId</span></span>
<span data-ttu-id="c5051-127">원격 로그온 설정을 얻을 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="c5051-128">이 cmdlet에서 원격 로그온 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5051-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5051-129">-DefaultProfile</span></span>
<span data-ttu-id="c5051-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5051-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c5051-131">-PoolId</span></span>
<span data-ttu-id="c5051-132">가상 머신을 포함하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5051-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5051-133">CommonParameters</span></span>
<span data-ttu-id="c5051-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5051-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5051-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5051-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5051-136">입력</span><span class="sxs-lookup"><span data-stu-id="c5051-136">INPUTS</span></span>

### <span data-ttu-id="c5051-137">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c5051-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="c5051-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c5051-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c5051-139">출력</span><span class="sxs-lookup"><span data-stu-id="c5051-139">OUTPUTS</span></span>

### <span data-ttu-id="c5051-140">Microsoft.Azure.Commands.Bat. Models.PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="c5051-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="c5051-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5051-141">NOTES</span></span>

## <span data-ttu-id="c5051-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5051-142">RELATED LINKS</span></span>

[<span data-ttu-id="c5051-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c5051-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c5051-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c5051-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="c5051-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="c5051-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="c5051-146">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c5051-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
