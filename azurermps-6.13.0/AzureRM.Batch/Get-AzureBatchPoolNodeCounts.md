---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolnodecounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolNodeCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolNodeCounts.md
ms.openlocfilehash: 6cd15b6a8ee59982bf328f751a20807835f54513
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703180"
---
# <span data-ttu-id="e9791-101">Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="e9791-101">Get-AzureBatchPoolNodeCounts</span></span>

## <span data-ttu-id="e9791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9791-102">SYNOPSIS</span></span>
<span data-ttu-id="e9791-103">풀 id로 그룹화 된 노드 상태별로 일괄 처리 노드 개수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-103">Gets Batch node counts per node state grouped by pool id.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9791-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9791-104">SYNTAX</span></span>

### <span data-ttu-id="e9791-105">AzureBatchPoolNodeCounts (기본값)</span><span class="sxs-lookup"><span data-stu-id="e9791-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzureBatchPoolNodeCounts -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9791-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="e9791-106">PoolId</span></span>
```
Get-AzureBatchPoolNodeCounts [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9791-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="e9791-107">ParentObject</span></span>
```
Get-AzureBatchPoolNodeCounts [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9791-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="e9791-108">ODataFilter</span></span>
```
Get-AzureBatchPoolNodeCounts [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9791-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e9791-109">DESCRIPTION</span></span>
<span data-ttu-id="e9791-110">Get-AzureBatchPoolNodeCounts cmdlet을 사용 하면 고객이 풀 별로 그룹화 된 노드 상태별로 다시 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-110">The Get-AzureBatchPoolNodeCounts cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="e9791-111">노드 상태는 만들기, 유휴, leavingPool, 오프 라인, 선취, 다시 부팅, reimaging, 실행, 시작, startTaskFailed, unknown, 사용할 수 없음, waitingForStartTask입니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="e9791-112">Cmdlet은 PoolId 또는 Pool 매개 변수를 사용 하 여 풀 id가 지정 된 풀만 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="e9791-113">예제의</span><span class="sxs-lookup"><span data-stu-id="e9791-113">EXAMPLES</span></span>

### <span data-ttu-id="e9791-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9791-114">Example 1</span></span>

```powershell
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzureBatchPoolNodeCounts -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="e9791-115">현재 일괄 처리 계정 컨텍스트 아래에서 풀에 대 한 노드 상태별로 목록 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="e9791-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="e9791-116">Example 2</span></span>

```powershell
PS C:\> Get-AzureBatchPoolNodeCounts -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzureBatchPoolNodeCounts -BatchContext $batchContext -PoolId "contosopool1"
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

PS C:\> Get-AzureBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzureBatchPoolNodeCounts -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="e9791-117">지정 된 풀 id에 대 한 노드 상태별 노드 수를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="e9791-118">변수</span><span class="sxs-lookup"><span data-stu-id="e9791-118">PARAMETERS</span></span>

### <span data-ttu-id="e9791-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e9791-119">-BatchContext</span></span>
<span data-ttu-id="e9791-120">일괄 처리 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="e9791-121">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="e9791-122">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="e9791-123">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="e9791-124">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e9791-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9791-125">-DefaultProfile</span></span>
<span data-ttu-id="e9791-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9791-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e9791-127">-MaxCount</span></span>
<span data-ttu-id="e9791-128">반환할 최대 풀 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="e9791-129">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-129">The default value is 10.</span></span>

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

### <span data-ttu-id="e9791-130">-풀</span><span class="sxs-lookup"><span data-stu-id="e9791-130">-Pool</span></span>
<span data-ttu-id="e9791-131">노드 개수를 가져올 **Pscloudpool** 를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

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

### <span data-ttu-id="e9791-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e9791-132">-PoolId</span></span>
<span data-ttu-id="e9791-133">노드 개수를 가져올 풀의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-133">The id of the pool for which to get node counts.</span></span>

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

### <span data-ttu-id="e9791-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9791-134">CommonParameters</span></span>
<span data-ttu-id="e9791-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9791-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9791-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9791-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9791-137">입력</span><span class="sxs-lookup"><span data-stu-id="e9791-137">INPUTS</span></span>

### <span data-ttu-id="e9791-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e9791-138">System.String</span></span>

### <span data-ttu-id="e9791-139">Microsoft.Azure.Commands.Batch. PSCloudPool 모델</span><span class="sxs-lookup"><span data-stu-id="e9791-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="e9791-140">매개 변수: Pool (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e9791-140">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="e9791-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e9791-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e9791-142">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e9791-142">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e9791-143">출력</span><span class="sxs-lookup"><span data-stu-id="e9791-143">OUTPUTS</span></span>

### <span data-ttu-id="e9791-144">Microsoft.Azure.Commands.Batch. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="e9791-144">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="e9791-145">상속자</span><span class="sxs-lookup"><span data-stu-id="e9791-145">NOTES</span></span>

## <span data-ttu-id="e9791-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9791-146">RELATED LINKS</span></span>

[<span data-ttu-id="e9791-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e9791-147">Get-AzureRmBatchAccountKeys</span></span>]()

[<span data-ttu-id="e9791-148">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e9791-148">Get-AzureBatchJob</span></span>]()

[<span data-ttu-id="e9791-149">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e9791-149">Azure Batch Cmdlets</span></span>]()

