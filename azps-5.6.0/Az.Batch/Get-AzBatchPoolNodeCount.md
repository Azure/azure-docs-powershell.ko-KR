---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: 10338e63ed060c1b93c67a2050d28346641f1911
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009792"
---
# <span data-ttu-id="8b331-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="8b331-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="8b331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b331-102">SYNOPSIS</span></span>
<span data-ttu-id="8b331-103">풀 ID로 그룹화된 노드 상태당 Batch 노드 수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="8b331-104">구문</span><span class="sxs-lookup"><span data-stu-id="8b331-104">SYNTAX</span></span>

### <span data-ttu-id="8b331-105">AzureBatchPoolNodeCounts(기본값)</span><span class="sxs-lookup"><span data-stu-id="8b331-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b331-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="8b331-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b331-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="8b331-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b331-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="8b331-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b331-109">설명</span><span class="sxs-lookup"><span data-stu-id="8b331-109">DESCRIPTION</span></span>
<span data-ttu-id="8b331-110">Get-AzBatchPoolNodeCount cmdlet을 사용하면 고객이 풀로 그룹화된 노드 상태당 노드 수를 되돌려 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="8b331-111">가능한 노드 상태는 만들기, 유휴 상태, 오프라인, 선점, 재부팅, 다시 시작, 실행, startTaskFailed, 알 수 없음, 사용할 수 없음 및 대기ForStartTask를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="8b331-112">cmdlet은 PoolId 또는 Pool 매개 변수를 사용하여 풀 ID가 지정된 풀만 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="8b331-113">예제</span><span class="sxs-lookup"><span data-stu-id="8b331-113">EXAMPLES</span></span>

### <span data-ttu-id="8b331-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b331-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="8b331-115">현재 일괄 처리 계정 컨텍스트에서 풀에 대한 노드 상태당 노드 수를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="8b331-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="8b331-116">Example 2</span></span>

```powershell
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"
PS C:\> $poolnodecounts.Dedicated

Creating            : 1
Idle                : 1
LeavingPool         : 0
Offline             : 0
Preempted           : 0
Rebooting           : 1
Reimaging           : 0
Running             : 5
Starting            : 0
StartTaskFailed     : 0
Total               : 8
Unknown             : 0
Unusable            : 0
WaitingForStartTask : 0

PS C:\> Get-AzBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="8b331-117">주어진 풀 ID에 대한 노드 상태당 노드 수를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="8b331-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8b331-118">PARAMETERS</span></span>

### <span data-ttu-id="8b331-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8b331-119">-BatchContext</span></span>
<span data-ttu-id="8b331-120">Batch 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="8b331-121">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="8b331-122">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="8b331-123">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="8b331-124">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8b331-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b331-125">-DefaultProfile</span></span>
<span data-ttu-id="8b331-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b331-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8b331-127">-MaxCount</span></span>
<span data-ttu-id="8b331-128">반환할 최대 풀 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="8b331-129">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-129">The default value is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b331-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="8b331-130">-Pool</span></span>
<span data-ttu-id="8b331-131">노드 수를 얻을 **PSCloudPool을** 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b331-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="8b331-132">-PoolId</span></span>
<span data-ttu-id="8b331-133">노드 수를 얻을 풀의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-133">The id of the pool for which to get node counts.</span></span>

```yaml
Type: System.String
Parameter Sets: PoolId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b331-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b331-134">CommonParameters</span></span>
<span data-ttu-id="8b331-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b331-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b331-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b331-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b331-137">입력</span><span class="sxs-lookup"><span data-stu-id="8b331-137">INPUTS</span></span>

### <span data-ttu-id="8b331-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8b331-138">System.String</span></span>

### <span data-ttu-id="8b331-139">Microsoft.Azure.Commands.Bat. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="8b331-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="8b331-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8b331-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8b331-141">출력</span><span class="sxs-lookup"><span data-stu-id="8b331-141">OUTPUTS</span></span>

### <span data-ttu-id="8b331-142">Microsoft.Azure.Commands.Bat. Models.PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="8b331-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="8b331-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b331-143">NOTES</span></span>

## <span data-ttu-id="8b331-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b331-144">RELATED LINKS</span></span>

[<span data-ttu-id="8b331-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8b331-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="8b331-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="8b331-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="8b331-147">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8b331-147">Azure Batch Cmdlets</span></span>]()

