---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 0d33ce7e41fb8058acb36a4668eeb337d54f187e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972976"
---
# <span data-ttu-id="eee34-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="eee34-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="eee34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eee34-102">SYNOPSIS</span></span>
<span data-ttu-id="eee34-103">Batch 작업 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="eee34-104">구문</span><span class="sxs-lookup"><span data-stu-id="eee34-104">SYNTAX</span></span>

### <span data-ttu-id="eee34-105">ODataFilter(기본값)</span><span class="sxs-lookup"><span data-stu-id="eee34-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eee34-106">ID</span><span class="sxs-lookup"><span data-stu-id="eee34-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eee34-107">설명</span><span class="sxs-lookup"><span data-stu-id="eee34-107">DESCRIPTION</span></span>
<span data-ttu-id="eee34-108">**Get-AzBatchJobSchedule** cmdlet은 *BatchContext* 매개 변수에 의해 지정된 Batch 계정에 대한 Azure Batch 작업 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="eee34-109">ID를 지정하여 단일 작업 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="eee34-110">필터 *매개* 변수를 지정하여 OData(Open Data Protocol) 필터와 일치하는 작업 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="eee34-111">예제</span><span class="sxs-lookup"><span data-stu-id="eee34-111">EXAMPLES</span></span>

### <span data-ttu-id="eee34-112">예제 1: ID를 지정하여 작업 일정을 구합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-112">Example 1: Get a job schedule by specifying an ID</span></span>
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

<span data-ttu-id="eee34-113">이 명령은 ID JobSchedule23이 있는 작업 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="eee34-114">Get-AzBatchAccountKey cmdlet을 사용하여 변수 변수에 컨텍스트를 $Context 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="eee34-115">예제 2: 필터를 사용하여 작업 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-115">Example 2: Get job schedules by using a filter</span></span>
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

<span data-ttu-id="eee34-116">이 명령은 필터 매개 변수를 지정하여 작업으로 시작하는 ID가 있는 모든 작업 *일정을 제공합니다.*</span><span class="sxs-lookup"><span data-stu-id="eee34-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="eee34-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="eee34-117">PARAMETERS</span></span>

### <span data-ttu-id="eee34-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="eee34-118">-BatchContext</span></span>
<span data-ttu-id="eee34-119">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eee34-120">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="eee34-121">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="eee34-122">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="eee34-123">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="eee34-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee34-124">-DefaultProfile</span></span>
<span data-ttu-id="eee34-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eee34-126">-확장</span><span class="sxs-lookup"><span data-stu-id="eee34-126">-Expand</span></span>
<span data-ttu-id="eee34-127">OData(Open Data Protocol) 확장 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="eee34-128">이 매개 변수에 대한 값을 지정하여 얻을 주 엔터티의 관련 엔터티를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="eee34-129">-Filter</span><span class="sxs-lookup"><span data-stu-id="eee34-129">-Filter</span></span>
<span data-ttu-id="eee34-130">OData 필터 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="eee34-131">이 cmdlet은 이 매개 변수가 지정하는 필터와 일치하는 작업 일정을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="eee34-132">필터를 지정하지 않으면 이 cmdlet은 Batch 컨텍스트에 대한 모든 작업 일정을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="eee34-133">-Id</span><span class="sxs-lookup"><span data-stu-id="eee34-133">-Id</span></span>
<span data-ttu-id="eee34-134">이 cmdlet이 얻을 작업 일정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="eee34-135">와일드카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="eee34-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="eee34-136">-MaxCount</span></span>
<span data-ttu-id="eee34-137">반환할 최대 작업 일정 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="eee34-138">0(0) 이하의 값을 지정하는 경우 cmdlet은 상한을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="eee34-139">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="eee34-140">-Select</span><span class="sxs-lookup"><span data-stu-id="eee34-140">-Select</span></span>
<span data-ttu-id="eee34-141">OData select 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="eee34-142">이 매개 변수에 대한 값을 지정하여 모든 개체 속성이 아닌 특정 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="eee34-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee34-143">CommonParameters</span></span>
<span data-ttu-id="eee34-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eee34-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee34-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eee34-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee34-146">입력</span><span class="sxs-lookup"><span data-stu-id="eee34-146">INPUTS</span></span>

### <span data-ttu-id="eee34-147">System.String</span><span class="sxs-lookup"><span data-stu-id="eee34-147">System.String</span></span>

### <span data-ttu-id="eee34-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eee34-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="eee34-149">출력</span><span class="sxs-lookup"><span data-stu-id="eee34-149">OUTPUTS</span></span>

### <span data-ttu-id="eee34-150">Microsoft.Azure.Commands.Bat. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="eee34-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="eee34-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eee34-151">NOTES</span></span>

## <span data-ttu-id="eee34-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eee34-152">RELATED LINKS</span></span>

[<span data-ttu-id="eee34-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="eee34-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="eee34-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="eee34-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="eee34-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="eee34-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="eee34-156">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="eee34-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="eee34-157">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="eee34-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="eee34-158">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="eee34-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="eee34-159">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eee34-159">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
