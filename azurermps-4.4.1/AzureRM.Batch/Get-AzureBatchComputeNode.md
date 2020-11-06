---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
ms.openlocfilehash: f503352352c31369e594325c060cf0ab68490095
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537480"
---
# <span data-ttu-id="4c573-101">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4c573-101">Get-AzureBatchComputeNode</span></span>

## <span data-ttu-id="4c573-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c573-102">SYNOPSIS</span></span>
<span data-ttu-id="4c573-103">풀에서 일괄 처리를 계산 하는 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-103">Gets Batch compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c573-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4c573-104">SYNTAX</span></span>

### <span data-ttu-id="4c573-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="4c573-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c573-106">I</span><span class="sxs-lookup"><span data-stu-id="4c573-106">Id</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c573-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="4c573-107">ParentObject</span></span>
```
Get-AzureBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c573-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4c573-108">DESCRIPTION</span></span>
<span data-ttu-id="4c573-109">**AzureBatchComputeNode** cmdlet은 풀에서 Azure 일괄 처리 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-109">The **Get-AzureBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="4c573-110">*PoolID* 또는 *Pool* 매개 변수 중 하나를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="4c573-111">*Id* 매개 변수를 지정 하 여 단일 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="4c573-112">*Filter* 매개 변수를 지정 하 여 OData (Open Data Protocol) 필터와 일치 하는 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="4c573-113">예제의</span><span class="sxs-lookup"><span data-stu-id="4c573-113">EXAMPLES</span></span>

### <span data-ttu-id="4c573-114">예제 1: ID로 계산 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="4c573-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="4c573-115">이 명령은 ID Pool06 있는 풀에서 tvm-2316545714_1-20150725t213220z 인 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="4c573-116">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="4c573-117">예제 2: 풀에서 모든 유휴 계산 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="4c573-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
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
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="4c573-118">이 명령은 ID Pool06가 있는 풀에 포함 된 모든 유휴 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="4c573-119">명령은 *Filter* 매개 변수를 사용 하 여 유휴 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="4c573-120">예제 3: 지정 된 풀의 모든 계산 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="4c573-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzureBatchPool -Id "Pool07" -BatchContext $Context | Get-AzureBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
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
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="4c573-121">이 명령은 Get-AzureBatchPool cmdlet을 사용 하 여 ID Pool07 있는 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-121">This command gets the pool that has the ID Pool07 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="4c573-122">이 명령은 파이프라인 연산자를 사용 하 여 해당 풀을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4c573-123">해당 cmdlet은 해당 풀의 모든 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="4c573-124">변수</span><span class="sxs-lookup"><span data-stu-id="4c573-124">PARAMETERS</span></span>

### <span data-ttu-id="4c573-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4c573-125">-BatchContext</span></span>
<span data-ttu-id="4c573-126">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4c573-127">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-127">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="4c573-128">-필터</span><span class="sxs-lookup"><span data-stu-id="4c573-128">-Filter</span></span>
<span data-ttu-id="4c573-129">OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-129">Specifies an OData filter clause.</span></span>
<span data-ttu-id="4c573-130">이 cmdlet은이 매개 변수에서 지정 하는 필터와 일치 하는 계산 노드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-130">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="4c573-131">필터를 지정 하지 않으면이 cmdlet은 풀에 대 한 모든 계산 노드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-131">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="4c573-132">-Id</span><span class="sxs-lookup"><span data-stu-id="4c573-132">-Id</span></span>
<span data-ttu-id="4c573-133">이 cmdlet이 풀에서 가져온 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-133">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="4c573-134">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="4c573-135">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4c573-135">-MaxCount</span></span>
<span data-ttu-id="4c573-136">반환할 계산 노드의 최대 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-136">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="4c573-137">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-137">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="4c573-138">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-138">The default value is 1000.</span></span>

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

### <span data-ttu-id="4c573-139">-풀</span><span class="sxs-lookup"><span data-stu-id="4c573-139">-Pool</span></span>
<span data-ttu-id="4c573-140">계산 노드를 포함 하는 **Pscloudpool** 개체로 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-140">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="4c573-141">**Pscloudpool** 개체를 가져오려면 Get-AzureBatchPool cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-141">To obtain a **PSCloudPool** object, use the Get-AzureBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="4c573-142">-PoolId</span><span class="sxs-lookup"><span data-stu-id="4c573-142">-PoolId</span></span>
<span data-ttu-id="4c573-143">계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-143">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="4c573-144">-선택</span><span class="sxs-lookup"><span data-stu-id="4c573-144">-Select</span></span>
<span data-ttu-id="4c573-145">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-145">Specifies an OData select clause.</span></span>
<span data-ttu-id="4c573-146">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-146">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="4c573-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c573-147">-DefaultProfile</span></span>
<span data-ttu-id="4c573-148">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c573-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c573-149">CommonParameters</span></span>
<span data-ttu-id="4c573-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c573-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c573-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c573-152">입력</span><span class="sxs-lookup"><span data-stu-id="4c573-152">INPUTS</span></span>

### <span data-ttu-id="4c573-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4c573-153">BatchAccountContext</span></span>
<span data-ttu-id="4c573-154">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="4c573-155">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="4c573-155">PSCloudPool</span></span>
<span data-ttu-id="4c573-156">' Pool ' 매개 변수는 파이프라인에서 ' PSCloudPool ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c573-156">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="4c573-157">출력</span><span class="sxs-lookup"><span data-stu-id="4c573-157">OUTPUTS</span></span>

### <span data-ttu-id="4c573-158">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="4c573-158">PSComputeNode</span></span>

## <span data-ttu-id="4c573-159">상속자</span><span class="sxs-lookup"><span data-stu-id="4c573-159">NOTES</span></span>

## <span data-ttu-id="4c573-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c573-160">RELATED LINKS</span></span>

[<span data-ttu-id="4c573-161">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4c573-161">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="4c573-162">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="4c573-162">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="4c573-163">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="4c573-163">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="4c573-164">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="4c573-164">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="4c573-165">다시 설정-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4c573-165">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="4c573-166">다시 시작-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4c573-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="4c573-167">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4c573-167">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


