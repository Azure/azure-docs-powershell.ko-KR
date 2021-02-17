---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: a50329620944aa18458c3bb667e3a95ff45bc21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197121"
---
# <span data-ttu-id="ef688-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ef688-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="ef688-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef688-102">SYNOPSIS</span></span>
<span data-ttu-id="ef688-103">풀에서 Batch 계산 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="ef688-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef688-104">SYNTAX</span></span>

### <span data-ttu-id="ef688-105">ODataFilter(기본값)</span><span class="sxs-lookup"><span data-stu-id="ef688-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef688-106">ID</span><span class="sxs-lookup"><span data-stu-id="ef688-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef688-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ef688-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef688-108">설명</span><span class="sxs-lookup"><span data-stu-id="ef688-108">DESCRIPTION</span></span>
<span data-ttu-id="ef688-109">**Get-AzBatchComputeNode** cmdlet은 풀에서 Azure Batch 계산 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="ef688-110">*PoolID* 또는 Pool 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="ef688-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="ef688-111">Id 매개 *변수를* 지정하여 단일 계산 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="ef688-112">Open *Data* Protocol(OData) 필터와 일치하는 계산 노드를 얻게 하는 Filter 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="ef688-113">예제</span><span class="sxs-lookup"><span data-stu-id="ef688-113">EXAMPLES</span></span>

### <span data-ttu-id="ef688-114">예제 1: ID로 계산 노드를 얻게</span><span class="sxs-lookup"><span data-stu-id="ef688-114">Example 1: Get a compute node by ID</span></span>
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

<span data-ttu-id="ef688-115">이 명령은 ID 풀06이 있는 풀에서 ID tvm-2316545714_1-20150725t213220z가 있는 계산 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="ef688-116">Get-AzBatchAccountKey cmdlet을 사용하여 $Context 변수에 컨텍스트를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ef688-117">예제 2: 풀에서 모든 유휴 계산 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-117">Example 2: Get all idle compute nodes from a pool</span></span>
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

<span data-ttu-id="ef688-118">이 명령은 ID Pool06이 있는 풀에 포함된 모든 유휴 계산 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="ef688-119">이 명령은 Filter 매개 변수를 사용하여 유휴 상태를 *지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="ef688-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="ef688-120">예제 3: 지정된 풀의 모든 계산 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-120">Example 3: Get all compute nodes in a specified pool</span></span>
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

<span data-ttu-id="ef688-121">이 명령은 Get-AzBatchPool cmdlet을 사용하여 ID Pool07이 있는 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="ef688-122">이 명령은 파이프라인 연산자를 사용하여 풀을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ef688-123">해당 cmdlet은 해당 풀에서 모든 계산 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="ef688-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef688-124">PARAMETERS</span></span>

### <span data-ttu-id="ef688-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ef688-125">-BatchContext</span></span>
<span data-ttu-id="ef688-126">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ef688-127">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ef688-128">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ef688-129">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ef688-130">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ef688-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef688-131">-DefaultProfile</span></span>
<span data-ttu-id="ef688-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef688-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="ef688-133">-Filter</span></span>
<span data-ttu-id="ef688-134">OData 필터 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="ef688-135">이 cmdlet은 이 매개 변수가 지정하는 필터와 일치하는 계산 노드를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="ef688-136">필터를 지정하지 않으면 이 cmdlet은 풀에 대한 모든 계산 노드를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="ef688-137">-Id</span><span class="sxs-lookup"><span data-stu-id="ef688-137">-Id</span></span>
<span data-ttu-id="ef688-138">이 cmdlet이 풀에서 얻을 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="ef688-139">와일드카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-139">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ef688-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ef688-140">-MaxCount</span></span>
<span data-ttu-id="ef688-141">반환할 계산 노드의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="ef688-142">0 이하의 값을 지정하는 경우 cmdlet은 상한을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ef688-143">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="ef688-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="ef688-144">-Pool</span></span>
<span data-ttu-id="ef688-145">계산 노드를 포함하는 **PSCloudPool** 개체로 풀을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="ef688-146">**PSCloudPool 개체를** 얻습니다. Get-AzBatchPool cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="ef688-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ef688-147">-PoolId</span></span>
<span data-ttu-id="ef688-148">계산 노드를 포함하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="ef688-149">-Select</span><span class="sxs-lookup"><span data-stu-id="ef688-149">-Select</span></span>
<span data-ttu-id="ef688-150">OData select 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="ef688-151">이 매개 변수에 대한 값을 지정하여 모든 개체 속성이 아닌 특정 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="ef688-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef688-152">CommonParameters</span></span>
<span data-ttu-id="ef688-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef688-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef688-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ef688-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef688-155">입력</span><span class="sxs-lookup"><span data-stu-id="ef688-155">INPUTS</span></span>

### <span data-ttu-id="ef688-156">System.String</span><span class="sxs-lookup"><span data-stu-id="ef688-156">System.String</span></span>

### <span data-ttu-id="ef688-157">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="ef688-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="ef688-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ef688-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ef688-159">출력</span><span class="sxs-lookup"><span data-stu-id="ef688-159">OUTPUTS</span></span>

### <span data-ttu-id="ef688-160">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ef688-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="ef688-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef688-161">NOTES</span></span>

## <span data-ttu-id="ef688-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef688-162">RELATED LINKS</span></span>

[<span data-ttu-id="ef688-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ef688-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="ef688-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="ef688-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="ef688-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="ef688-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="ef688-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ef688-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="ef688-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ef688-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="ef688-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ef688-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="ef688-169">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef688-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
