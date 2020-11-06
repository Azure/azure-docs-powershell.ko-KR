---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: 139282332fb1c5d0ace02ddd7b998c1875af931a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530807"
---
# <span data-ttu-id="54674-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="54674-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="54674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54674-102">SYNOPSIS</span></span>
<span data-ttu-id="54674-103">일괄 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54674-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54674-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54674-104">SYNTAX</span></span>

### <span data-ttu-id="54674-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="54674-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54674-106">I</span><span class="sxs-lookup"><span data-stu-id="54674-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54674-107">설명은</span><span class="sxs-lookup"><span data-stu-id="54674-107">DESCRIPTION</span></span>
<span data-ttu-id="54674-108">**Get-AzureBatchJobSchedule** Cmdlet은 *batchcontext* 매개 변수에 의해 지정 된 일괄 처리 계정에 대 한 Azure 일괄 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54674-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="54674-109">단일 작업 일정을 가져오려면 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="54674-110">*Filter* 매개 변수를 지정 하 여 열려 있는 데이터 프로토콜 (OData) 필터와 일치 하는 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54674-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="54674-111">예제의</span><span class="sxs-lookup"><span data-stu-id="54674-111">EXAMPLES</span></span>

### <span data-ttu-id="54674-112">예제 1: ID를 지정 하 여 작업 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="54674-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

<span data-ttu-id="54674-113">이 명령은 ID JobSchedule23가 있는 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54674-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="54674-114">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="54674-115">예제 2: 필터를 사용 하 여 작업 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="54674-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 : 
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

<span data-ttu-id="54674-116">이 명령은 *필터* 매개 변수를 지정 하 여 작업으로 시작 하는 id가 있는 모든 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54674-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="54674-117">변수</span><span class="sxs-lookup"><span data-stu-id="54674-117">PARAMETERS</span></span>

### <span data-ttu-id="54674-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="54674-118">-BatchContext</span></span>
<span data-ttu-id="54674-119">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="54674-120">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="54674-121">-확장</span><span class="sxs-lookup"><span data-stu-id="54674-121">-Expand</span></span>
<span data-ttu-id="54674-122">OData (Open Data Protocol) expand 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-122">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="54674-123">이 매개 변수에 대 한 값을 지정 하 여 가져올 기본 엔터티의 연결 된 엔터티를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54674-123">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="54674-124">-필터</span><span class="sxs-lookup"><span data-stu-id="54674-124">-Filter</span></span>
<span data-ttu-id="54674-125">OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-125">Specifies an OData filter clause.</span></span>
<span data-ttu-id="54674-126">이 cmdlet은이 매개 변수에서 지정 하는 필터와 일치 하는 작업 일정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-126">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="54674-127">필터를 지정 하지 않으면이 cmdlet은 일괄 처리 컨텍스트에 대 한 모든 작업 일정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-127">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="54674-128">-Id</span><span class="sxs-lookup"><span data-stu-id="54674-128">-Id</span></span>
<span data-ttu-id="54674-129">이 cmdlet이 가져오는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-129">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="54674-130">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="54674-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="54674-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="54674-131">-MaxCount</span></span>
<span data-ttu-id="54674-132">반환할 최대 작업 일정 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-132">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="54674-133">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54674-133">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="54674-134">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="54674-134">The default value is 1000.</span></span>

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

### <span data-ttu-id="54674-135">-선택</span><span class="sxs-lookup"><span data-stu-id="54674-135">-Select</span></span>
<span data-ttu-id="54674-136">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-136">Specifies an OData select clause.</span></span>
<span data-ttu-id="54674-137">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54674-137">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="54674-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54674-138">-DefaultProfile</span></span>
<span data-ttu-id="54674-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54674-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54674-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54674-140">CommonParameters</span></span>
<span data-ttu-id="54674-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54674-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54674-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54674-143">입력</span><span class="sxs-lookup"><span data-stu-id="54674-143">INPUTS</span></span>

### <span data-ttu-id="54674-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="54674-144">BatchAccountContext</span></span>
<span data-ttu-id="54674-145">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="54674-146">이름</span><span class="sxs-lookup"><span data-stu-id="54674-146">String</span></span>
<span data-ttu-id="54674-147">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="54674-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="54674-148">출력</span><span class="sxs-lookup"><span data-stu-id="54674-148">OUTPUTS</span></span>

### <span data-ttu-id="54674-149">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="54674-149">PSCloudJobSchedule</span></span>

## <span data-ttu-id="54674-150">상속자</span><span class="sxs-lookup"><span data-stu-id="54674-150">NOTES</span></span>

## <span data-ttu-id="54674-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54674-151">RELATED LINKS</span></span>

[<span data-ttu-id="54674-152">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="54674-152">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="54674-153">-AzureBatchJobSchedule 사용</span><span class="sxs-lookup"><span data-stu-id="54674-153">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="54674-154">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="54674-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="54674-155">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="54674-155">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="54674-156">-AzureBatchJobSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="54674-156">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="54674-157">중지-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="54674-157">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="54674-158">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54674-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


