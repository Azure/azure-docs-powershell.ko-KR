---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: a50329620944aa18458c3bb667e3a95ff45bc21f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311522"
---
# <span data-ttu-id="d7f08-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d7f08-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="d7f08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7f08-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f08-103">풀에서 일괄 처리를 계산 하는 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="d7f08-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7f08-104">SYNTAX</span></span>

### <span data-ttu-id="d7f08-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="d7f08-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7f08-106">I</span><span class="sxs-lookup"><span data-stu-id="d7f08-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7f08-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="d7f08-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7f08-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d7f08-108">DESCRIPTION</span></span>
<span data-ttu-id="d7f08-109">**AzBatchComputeNode** cmdlet은 풀에서 Azure 일괄 처리 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="d7f08-110">*PoolID* 또는 *Pool* 매개 변수 중 하나를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="d7f08-111">*Id* 매개 변수를 지정 하 여 단일 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="d7f08-112">*Filter* 매개 변수를 지정 하 여 OData (Open Data Protocol) 필터와 일치 하는 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="d7f08-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d7f08-113">EXAMPLES</span></span>

### <span data-ttu-id="d7f08-114">예제 1: ID로 계산 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="d7f08-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="d7f08-115">이 명령은 ID Pool06 있는 풀에서 tvm-2316545714_1-20150725t213220z 인 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d7f08-116">Get-AzBatchAccountKey cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d7f08-117">예제 2: 풀에서 모든 유휴 계산 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="d7f08-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :

Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM
IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="d7f08-118">이 명령은 ID Pool06가 있는 풀에 포함 된 모든 유휴 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d7f08-119">명령은 *Filter* 매개 변수를 사용 하 여 유휴 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="d7f08-120">예제 3: 지정 된 풀의 모든 계산 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="d7f08-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzBatchPool -Id "Pool07" -BatchContext $Context | Get-AzBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :


Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM

IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="d7f08-121">이 명령은 Get-AzBatchPool cmdlet을 사용 하 여 ID Pool07 있는 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="d7f08-122">이 명령은 파이프라인 연산자를 사용 하 여 해당 풀을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d7f08-123">해당 cmdlet은 해당 풀의 모든 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="d7f08-124">변수</span><span class="sxs-lookup"><span data-stu-id="d7f08-124">PARAMETERS</span></span>

### <span data-ttu-id="d7f08-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d7f08-125">-BatchContext</span></span>
<span data-ttu-id="d7f08-126">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d7f08-127">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d7f08-128">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d7f08-129">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d7f08-130">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d7f08-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f08-131">-DefaultProfile</span></span>
<span data-ttu-id="d7f08-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7f08-133">-필터</span><span class="sxs-lookup"><span data-stu-id="d7f08-133">-Filter</span></span>
<span data-ttu-id="d7f08-134">OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="d7f08-135">이 cmdlet은이 매개 변수에서 지정 하는 필터와 일치 하는 계산 노드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="d7f08-136">필터를 지정 하지 않으면이 cmdlet은 풀에 대 한 모든 계산 노드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f08-137">-Id</span><span class="sxs-lookup"><span data-stu-id="d7f08-137">-Id</span></span>
<span data-ttu-id="d7f08-138">이 cmdlet이 풀에서 가져온 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="d7f08-139">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-139">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f08-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d7f08-140">-MaxCount</span></span>
<span data-ttu-id="d7f08-141">반환할 계산 노드의 최대 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="d7f08-142">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="d7f08-143">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-143">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f08-144">-풀</span><span class="sxs-lookup"><span data-stu-id="d7f08-144">-Pool</span></span>
<span data-ttu-id="d7f08-145">계산 노드를 포함 하는 **Pscloudpool** 개체로 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="d7f08-146">**Pscloudpool** 개체를 가져오려면 Get-AzBatchPool cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f08-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d7f08-147">-PoolId</span></span>
<span data-ttu-id="d7f08-148">계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f08-149">-선택</span><span class="sxs-lookup"><span data-stu-id="d7f08-149">-Select</span></span>
<span data-ttu-id="d7f08-150">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="d7f08-151">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f08-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f08-152">CommonParameters</span></span>
<span data-ttu-id="d7f08-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f08-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f08-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d7f08-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f08-155">입력</span><span class="sxs-lookup"><span data-stu-id="d7f08-155">INPUTS</span></span>

### <span data-ttu-id="d7f08-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d7f08-156">System.String</span></span>

### <span data-ttu-id="d7f08-157">Microsoft.Azure.Commands.Batch. PSCloudPool 모델</span><span class="sxs-lookup"><span data-stu-id="d7f08-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="d7f08-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d7f08-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d7f08-159">출력</span><span class="sxs-lookup"><span data-stu-id="d7f08-159">OUTPUTS</span></span>

### <span data-ttu-id="d7f08-160">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d7f08-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="d7f08-161">상속자</span><span class="sxs-lookup"><span data-stu-id="d7f08-161">NOTES</span></span>

## <span data-ttu-id="d7f08-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7f08-162">RELATED LINKS</span></span>

[<span data-ttu-id="d7f08-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d7f08-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="d7f08-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="d7f08-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="d7f08-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="d7f08-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="d7f08-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d7f08-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="d7f08-167">다시 설정-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d7f08-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="d7f08-168">다시 시작-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d7f08-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="d7f08-169">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d7f08-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
