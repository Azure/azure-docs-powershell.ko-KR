---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 9daa0e1a1b1bc6ec980f3c3f65d79840648fdaf8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048496"
---
# <span data-ttu-id="262d8-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="262d8-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="262d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="262d8-102">SYNOPSIS</span></span>
<span data-ttu-id="262d8-103">일괄 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="262d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="262d8-104">SYNTAX</span></span>

### <span data-ttu-id="262d8-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="262d8-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="262d8-106">I</span><span class="sxs-lookup"><span data-stu-id="262d8-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="262d8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="262d8-107">DESCRIPTION</span></span>
<span data-ttu-id="262d8-108">**AzBatchJobSchedule** Cmdlet은 *batchcontext* 매개 변수에 의해 지정 된 일괄 처리 계정에 대 한 Azure 일괄 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="262d8-109">단일 작업 일정을 가져오려면 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="262d8-110">*Filter* 매개 변수를 지정 하 여 열려 있는 데이터 프로토콜 (OData) 필터와 일치 하는 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="262d8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="262d8-111">EXAMPLES</span></span>

### <span data-ttu-id="262d8-112">예제 1: ID를 지정 하 여 작업 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="262d8-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
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

<span data-ttu-id="262d8-113">이 명령은 ID JobSchedule23가 있는 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="262d8-114">Get-AzBatchAccountKey cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="262d8-115">예제 2: 필터를 사용 하 여 작업 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="262d8-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
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

<span data-ttu-id="262d8-116">이 명령은 *필터* 매개 변수를 지정 하 여 작업으로 시작 하는 id가 있는 모든 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="262d8-117">변수</span><span class="sxs-lookup"><span data-stu-id="262d8-117">PARAMETERS</span></span>

### <span data-ttu-id="262d8-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="262d8-118">-BatchContext</span></span>
<span data-ttu-id="262d8-119">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="262d8-120">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="262d8-121">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="262d8-122">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="262d8-123">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="262d8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262d8-124">-DefaultProfile</span></span>
<span data-ttu-id="262d8-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="262d8-126">-확장</span><span class="sxs-lookup"><span data-stu-id="262d8-126">-Expand</span></span>
<span data-ttu-id="262d8-127">OData (Open Data Protocol) expand 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="262d8-128">이 매개 변수에 대 한 값을 지정 하 여 가져올 기본 엔터티의 연결 된 엔터티를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="262d8-129">-필터</span><span class="sxs-lookup"><span data-stu-id="262d8-129">-Filter</span></span>
<span data-ttu-id="262d8-130">OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="262d8-131">이 cmdlet은이 매개 변수에서 지정 하는 필터와 일치 하는 작업 일정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="262d8-132">필터를 지정 하지 않으면이 cmdlet은 일괄 처리 컨텍스트에 대 한 모든 작업 일정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="262d8-133">-Id</span><span class="sxs-lookup"><span data-stu-id="262d8-133">-Id</span></span>
<span data-ttu-id="262d8-134">이 cmdlet이 가져오는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="262d8-135">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="262d8-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="262d8-136">-MaxCount</span></span>
<span data-ttu-id="262d8-137">반환할 최대 작업 일정 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="262d8-138">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="262d8-139">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="262d8-140">-선택</span><span class="sxs-lookup"><span data-stu-id="262d8-140">-Select</span></span>
<span data-ttu-id="262d8-141">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="262d8-142">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="262d8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262d8-143">CommonParameters</span></span>
<span data-ttu-id="262d8-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="262d8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262d8-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="262d8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262d8-146">입력</span><span class="sxs-lookup"><span data-stu-id="262d8-146">INPUTS</span></span>

### <span data-ttu-id="262d8-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="262d8-147">System.String</span></span>

### <span data-ttu-id="262d8-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="262d8-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="262d8-149">출력</span><span class="sxs-lookup"><span data-stu-id="262d8-149">OUTPUTS</span></span>

### <span data-ttu-id="262d8-150">Microsoft.Azure.Commands.Batch. PSCloudJobSchedule 모델</span><span class="sxs-lookup"><span data-stu-id="262d8-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="262d8-151">상속자</span><span class="sxs-lookup"><span data-stu-id="262d8-151">NOTES</span></span>

## <span data-ttu-id="262d8-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="262d8-152">RELATED LINKS</span></span>

[<span data-ttu-id="262d8-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="262d8-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="262d8-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="262d8-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="262d8-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="262d8-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="262d8-156">새로운 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="262d8-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="262d8-157">제거-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="262d8-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="262d8-158">중지-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="262d8-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="262d8-159">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="262d8-159">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
