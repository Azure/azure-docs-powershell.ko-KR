---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: 63a8ba2d98bd81cbeca3286259920debc10723a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986986"
---
# <span data-ttu-id="8914f-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8914f-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="8914f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8914f-102">SYNOPSIS</span></span>
<span data-ttu-id="8914f-103">Batch 서비스에서 작업 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="8914f-104">구문</span><span class="sxs-lookup"><span data-stu-id="8914f-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8914f-105">설명</span><span class="sxs-lookup"><span data-stu-id="8914f-105">DESCRIPTION</span></span>
<span data-ttu-id="8914f-106">**New-AzBatchJobSchedule** cmdlet은 Azure Batch 서비스에서 작업 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="8914f-107">*BatchAccountContext* 매개 변수는 이 cmdlet이 일정을 만드는 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="8914f-108">예제</span><span class="sxs-lookup"><span data-stu-id="8914f-108">EXAMPLES</span></span>

### <span data-ttu-id="8914f-109">예제 1: 작업 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="8914f-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="8914f-110">이 예제에서는 작업 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-110">This example creates a job schedule.</span></span>
<span data-ttu-id="8914f-111">처음 5개의 명령은 **PSSchedule,** **PSJobSpecification** 및 **PSPoolInformation 개체를** 만들고 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-111">The first five commands create and modify **PSSchedule**, **PSJobSpecification**, and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="8914f-112">명령은 New-Object cmdlet 및 표준 Azure PowerShell 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="8914f-113">명령은 이러한 개체를 $Schedule 및 $JobSpecification 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="8914f-114">마지막 명령은 ID JobSchedule17이 있는 작업 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="8914f-115">이 일정은 1일의 반복 간격으로 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="8914f-116">작업은 다섯 번째 명령에 지정된 ID ContosoPool06이 있는 풀에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="8914f-117">**Get-AzBatchAccountKey** cmdlet을 사용하여 $Context 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-117">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="8914f-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8914f-118">PARAMETERS</span></span>

### <span data-ttu-id="8914f-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8914f-119">-BatchContext</span></span>
<span data-ttu-id="8914f-120">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8914f-121">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8914f-122">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8914f-123">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8914f-124">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8914f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8914f-125">-DefaultProfile</span></span>
<span data-ttu-id="8914f-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8914f-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8914f-127">-DisplayName</span></span>
<span data-ttu-id="8914f-128">작업 일정에 대한 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="8914f-129">-Id</span><span class="sxs-lookup"><span data-stu-id="8914f-129">-Id</span></span>
<span data-ttu-id="8914f-130">이 cmdlet이 만드는 작업 일정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8914f-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="8914f-131">-JobSpecification</span></span>
<span data-ttu-id="8914f-132">이 cmdlet이 작업 일정에 포함된 작업의 세부 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="8914f-133">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="8914f-133">-Metadata</span></span>
<span data-ttu-id="8914f-134">작업 일정에 추가하기 위해 메타데이터를 키/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="8914f-135">키는 메타데이터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-135">The key is the metadata name.</span></span>
<span data-ttu-id="8914f-136">값은 메타데이터 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="8914f-137">-Schedule</span><span class="sxs-lookup"><span data-stu-id="8914f-137">-Schedule</span></span>
<span data-ttu-id="8914f-138">작업을 만들 때를 결정하는 일정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-138">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="8914f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8914f-139">CommonParameters</span></span>
<span data-ttu-id="8914f-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8914f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8914f-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8914f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8914f-142">입력</span><span class="sxs-lookup"><span data-stu-id="8914f-142">INPUTS</span></span>

### <span data-ttu-id="8914f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8914f-143">System.String</span></span>

### <span data-ttu-id="8914f-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8914f-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8914f-145">출력</span><span class="sxs-lookup"><span data-stu-id="8914f-145">OUTPUTS</span></span>

### <span data-ttu-id="8914f-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="8914f-146">System.Void</span></span>

## <span data-ttu-id="8914f-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8914f-147">NOTES</span></span>

## <span data-ttu-id="8914f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8914f-148">RELATED LINKS</span></span>

[<span data-ttu-id="8914f-149">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8914f-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="8914f-150">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8914f-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="8914f-151">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8914f-151">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8914f-152">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8914f-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="8914f-153">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8914f-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="8914f-154">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8914f-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="8914f-155">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8914f-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
