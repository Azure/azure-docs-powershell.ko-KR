---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 6f89e7db5d2df2c475be1ac9875fd1e87217db77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711786"
---
# <span data-ttu-id="3d1f0-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="3d1f0-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="3d1f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="3d1f0-103">지정 된 Batch 계정으로 일괄 처리 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d1f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d1f0-104">SYNTAX</span></span>

### <span data-ttu-id="3d1f0-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="3d1f0-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d1f0-106">I</span><span class="sxs-lookup"><span data-stu-id="3d1f0-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d1f0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3d1f0-107">DESCRIPTION</span></span>
<span data-ttu-id="3d1f0-108">**Get-AzureBatchPool** Cmdlet은 *batchcontext* 매개 변수를 사용 하 여 지정 된 Batch 계정 아래에서 Azure 일괄 처리 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="3d1f0-109">*Id* 매개 변수를 사용 하 여 단일 풀을 가져오거나 *filter* 매개 변수를 사용 하 여 OData (Open Data Protocol) 필터와 일치 하는 풀을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="3d1f0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3d1f0-110">EXAMPLES</span></span>

### <span data-ttu-id="3d1f0-111">예제 1: ID로 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="3d1f0-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzureBatchPool -Id "MyPool" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="3d1f0-112">이 명령은 ID MyPool를 사용 하 여 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="3d1f0-113">예제 2: OData 필터를 사용 하 여 모든 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="3d1f0-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzureBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="3d1f0-114">이 명령은 Id가 My로 시작 하는 풀을 *필터* 매개 변수를 사용 하 여 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="3d1f0-115">변수</span><span class="sxs-lookup"><span data-stu-id="3d1f0-115">PARAMETERS</span></span>

### <span data-ttu-id="3d1f0-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3d1f0-116">-BatchContext</span></span>
<span data-ttu-id="3d1f0-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3d1f0-118">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="3d1f0-119">-확장</span><span class="sxs-lookup"><span data-stu-id="3d1f0-119">-Expand</span></span>
<span data-ttu-id="3d1f0-120">OData (Open Data Protocol) expand 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-120">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="3d1f0-121">이 매개 변수에 대 한 값을 지정 하 여 가져올 기본 엔터티의 연결 된 엔터티를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-121">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="3d1f0-122">-필터</span><span class="sxs-lookup"><span data-stu-id="3d1f0-122">-Filter</span></span>
<span data-ttu-id="3d1f0-123">풀을 쿼리할 때 사용할 OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-123">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="3d1f0-124">필터를 지정 하지 않으면 *Batchcontext* 매개 변수를 사용 하 여 지정 된 일괄 처리 계정 아래에 있는 모든 풀이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-124">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d1f0-125">-Id</span><span class="sxs-lookup"><span data-stu-id="3d1f0-125">-Id</span></span>
<span data-ttu-id="3d1f0-126">가져올 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-126">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="3d1f0-127">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-127">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d1f0-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3d1f0-128">-MaxCount</span></span>
<span data-ttu-id="3d1f0-129">반환할 최대 풀 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-129">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="3d1f0-130">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-130">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="3d1f0-131">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-131">The default value is 1000.</span></span>

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

### <span data-ttu-id="3d1f0-132">-선택</span><span class="sxs-lookup"><span data-stu-id="3d1f0-132">-Select</span></span>
<span data-ttu-id="3d1f0-133">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-133">Specifies an OData select clause.</span></span>
<span data-ttu-id="3d1f0-134">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-134">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="3d1f0-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d1f0-135">-DefaultProfile</span></span>
<span data-ttu-id="3d1f0-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d1f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d1f0-137">CommonParameters</span></span>
<span data-ttu-id="3d1f0-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d1f0-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d1f0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d1f0-140">입력</span><span class="sxs-lookup"><span data-stu-id="3d1f0-140">INPUTS</span></span>

### <span data-ttu-id="3d1f0-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3d1f0-141">BatchAccountContext</span></span>
<span data-ttu-id="3d1f0-142">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="3d1f0-143">이름</span><span class="sxs-lookup"><span data-stu-id="3d1f0-143">String</span></span>
<span data-ttu-id="3d1f0-144">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f0-144">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3d1f0-145">출력</span><span class="sxs-lookup"><span data-stu-id="3d1f0-145">OUTPUTS</span></span>

### <span data-ttu-id="3d1f0-146">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="3d1f0-146">PSCloudPool</span></span>

## <span data-ttu-id="3d1f0-147">상속자</span><span class="sxs-lookup"><span data-stu-id="3d1f0-147">NOTES</span></span>

## <span data-ttu-id="3d1f0-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d1f0-148">RELATED LINKS</span></span>

[<span data-ttu-id="3d1f0-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3d1f0-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3d1f0-150">새-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="3d1f0-150">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="3d1f0-151">-AzureBatchPool 제거</span><span class="sxs-lookup"><span data-stu-id="3d1f0-151">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="3d1f0-152">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d1f0-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


