---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0a31b787b1be6d45caca74d01ee5d15d00071641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531190"
---
# <span data-ttu-id="cbd6b-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbd6b-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="cbd6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbd6b-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd6b-103">일괄 처리 서비스에서 작업 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbd6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cbd6b-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbd6b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cbd6b-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd6b-106">**새-AzureBatchJobSchedule** Cmdlet은 Azure Batch 서비스에서 작업 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="cbd6b-107">*Batchaccountcontext* 매개 변수는이 cmdlet이 일정을 만드는 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="cbd6b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="cbd6b-108">EXAMPLES</span></span>

### <span data-ttu-id="cbd6b-109">예제 1: 작업 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="cbd6b-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="cbd6b-110">이 예제에서는 작업 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-110">This example creates a job schedule.</span></span>

<span data-ttu-id="cbd6b-111">처음 5 개 명령은 **Psschedule** , **PSJobSpecification** 및 **PSPoolInformation** 개체를 만들고 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="cbd6b-112">명령에는 New-Object cmdlet 및 표준 Azure PowerShell 구문이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="cbd6b-113">명령은 $Schedule 및 $JobSpecification 변수에 이러한 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="cbd6b-114">마지막 명령은 ID JobSchedule17를 가진 작업 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="cbd6b-115">이 일정은 되풀이 간격 1 일이 포함 된 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="cbd6b-116">이 작업은 다섯 번째 명령에 지정 된 대로 ID ContosoPool06가 있는 풀에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="cbd6b-117">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzureRmBatchAccountKeys** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="cbd6b-118">변수</span><span class="sxs-lookup"><span data-stu-id="cbd6b-118">PARAMETERS</span></span>

### <span data-ttu-id="cbd6b-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cbd6b-119">-BatchContext</span></span>
<span data-ttu-id="cbd6b-120">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cbd6b-121">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="cbd6b-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cbd6b-122">-DisplayName</span></span>
<span data-ttu-id="cbd6b-123">작업 일정의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-123">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="cbd6b-124">-Id</span><span class="sxs-lookup"><span data-stu-id="cbd6b-124">-Id</span></span>
<span data-ttu-id="cbd6b-125">이 cmdlet이 만드는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-125">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd6b-126">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="cbd6b-126">-JobSpecification</span></span>
<span data-ttu-id="cbd6b-127">작업 일정에이 cmdlet에 포함 된 작업의 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-127">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd6b-128">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cbd6b-128">-Metadata</span></span>
<span data-ttu-id="cbd6b-129">작업 일정에 추가할 메타 데이터를 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-129">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="cbd6b-130">키는 메타 데이터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-130">The key is the metadata name.</span></span>
<span data-ttu-id="cbd6b-131">값은 메타 데이터 값입니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-131">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd6b-132">-일정</span><span class="sxs-lookup"><span data-stu-id="cbd6b-132">-Schedule</span></span>
<span data-ttu-id="cbd6b-133">작업을 만들 시기를 결정 하는 일정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-133">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd6b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd6b-134">-DefaultProfile</span></span>
<span data-ttu-id="cbd6b-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbd6b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd6b-136">CommonParameters</span></span>
<span data-ttu-id="cbd6b-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd6b-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd6b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd6b-139">입력</span><span class="sxs-lookup"><span data-stu-id="cbd6b-139">INPUTS</span></span>

### <span data-ttu-id="cbd6b-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cbd6b-140">BatchAccountContext</span></span>
<span data-ttu-id="cbd6b-141">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="cbd6b-142">출력</span><span class="sxs-lookup"><span data-stu-id="cbd6b-142">OUTPUTS</span></span>

## <span data-ttu-id="cbd6b-143">상속자</span><span class="sxs-lookup"><span data-stu-id="cbd6b-143">NOTES</span></span>

## <span data-ttu-id="cbd6b-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbd6b-144">RELATED LINKS</span></span>

[<span data-ttu-id="cbd6b-145">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbd6b-145">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="cbd6b-146">-AzureBatchJobSchedule 사용</span><span class="sxs-lookup"><span data-stu-id="cbd6b-146">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="cbd6b-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cbd6b-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cbd6b-148">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbd6b-148">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="cbd6b-149">-AzureBatchJobSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="cbd6b-149">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="cbd6b-150">중지-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbd6b-150">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="cbd6b-151">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cbd6b-151">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


