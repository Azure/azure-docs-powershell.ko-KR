---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: 94a35c3923debf5ea983e9d1ad276b124ae8c89c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531192"
---
# <span data-ttu-id="02462-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="02462-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="02462-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02462-102">SYNOPSIS</span></span>
<span data-ttu-id="02462-103">일괄 처리 서비스에 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02462-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02462-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02462-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02462-105">설명은</span><span class="sxs-lookup"><span data-stu-id="02462-105">DESCRIPTION</span></span>
<span data-ttu-id="02462-106">**새-AzureBatchJob** Cmdlet은 *batchaccountcontext* 매개 변수에 지정 된 계정의 Azure 일괄 처리 서비스에서 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02462-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="02462-107">예제의</span><span class="sxs-lookup"><span data-stu-id="02462-107">EXAMPLES</span></span>

### <span data-ttu-id="02462-108">예제 1: 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="02462-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="02462-109">첫 번째 명령은 New-Object cmdlet을 사용 하 여 **PSPoolInformation** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02462-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="02462-110">명령이 $PoolInformation 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="02462-111">두 번째 명령은 $PoolInformation에 있는 개체의 **PoolId** 속성에 ID Pool22를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="02462-112">마지막 명령은 ID ContosoJob35를 가진 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02462-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="02462-113">작업에 추가 된 작업은 ID Pool22를 가진 풀에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02462-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="02462-114">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="02462-115">변수</span><span class="sxs-lookup"><span data-stu-id="02462-115">PARAMETERS</span></span>

### <span data-ttu-id="02462-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="02462-116">-BatchContext</span></span>
<span data-ttu-id="02462-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="02462-118">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="02462-119">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="02462-119">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="02462-120">이 cmdlet이 작업의 모든 작업에 대해 설정 하는 공통 환경 변수를 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-120">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="02462-121">키는 환경 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02462-121">The key is the environment variable name.</span></span>
<span data-ttu-id="02462-122">값은 환경 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="02462-122">The value is the environment variable value.</span></span>

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

### <span data-ttu-id="02462-123">-제약 조건</span><span class="sxs-lookup"><span data-stu-id="02462-123">-Constraints</span></span>
<span data-ttu-id="02462-124">작업에 대 한 실행 제약 조건을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-124">Specifies the execution constraints for the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02462-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="02462-125">-DisplayName</span></span>
<span data-ttu-id="02462-126">작업의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-126">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="02462-127">-Id</span><span class="sxs-lookup"><span data-stu-id="02462-127">-Id</span></span>
<span data-ttu-id="02462-128">작업에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-128">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="02462-129">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="02462-129">-JobManagerTask</span></span>
<span data-ttu-id="02462-130">작업 관리자 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-130">Specifies the Job Manager task.</span></span>
<span data-ttu-id="02462-131">작업이 시작 되 면 일괄 처리 서비스가 작업 관리자 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-131">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02462-132">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="02462-132">-JobPreparationTask</span></span>
<span data-ttu-id="02462-133">작업 준비 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-133">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="02462-134">일괄 처리 서비스는 계산 노드에서 작업 준비 작업을 실행 한 후 해당 작업의 계산 노드에서 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-134">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02462-135">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="02462-135">-JobReleaseTask</span></span>
<span data-ttu-id="02462-136">작업 릴리스 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-136">Specifies the Job Release task.</span></span>
<span data-ttu-id="02462-137">일괄 처리 서비스는 작업이 종료 될 때 작업 릴리스 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-137">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="02462-138">일괄 처리 서비스는 작업의 작업을 실행 한 각 계산 노드에서 작업 릴리스 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-138">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02462-139">-Metadata</span><span class="sxs-lookup"><span data-stu-id="02462-139">-Metadata</span></span>
<span data-ttu-id="02462-140">작업에 추가할 메타 데이터를 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-140">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="02462-141">키는 메타 데이터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02462-141">The key is the metadata name.</span></span>
<span data-ttu-id="02462-142">값은 메타 데이터 값입니다.</span><span class="sxs-lookup"><span data-stu-id="02462-142">The value is the metadata value.</span></span>

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

### <span data-ttu-id="02462-143">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="02462-143">-OnAllTasksComplete</span></span>
<span data-ttu-id="02462-144">작업의 모든 작업이 완료 됨 상태인 경우 일괄 처리 서비스에서 수행 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-144">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnAllTasksComplete]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02462-145">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="02462-145">-OnTaskFailure</span></span>
<span data-ttu-id="02462-146">작업의 작업이 실패 하는 경우 일괄 처리 서비스에서 수행 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-146">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnTaskFailure]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02462-147">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="02462-147">-PoolInformation</span></span>
<span data-ttu-id="02462-148">일괄 처리 서비스가 작업의 작업을 실행 하는 풀의 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-148">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02462-149">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="02462-149">-Priority</span></span>
<span data-ttu-id="02462-150">작업의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-150">Specifies the priority of the job.</span></span>
<span data-ttu-id="02462-151">유효한 값은-1000에서 1000 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="02462-151">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="02462-152">값-1000은 가장 낮은 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="02462-152">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="02462-153">1000의 값은 가장 높은 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="02462-153">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="02462-154">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="02462-154">The default value is 0.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02462-155">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="02462-155">-UsesTaskDependencies</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02462-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02462-156">-DefaultProfile</span></span>
<span data-ttu-id="02462-157">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02462-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02462-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02462-158">CommonParameters</span></span>
<span data-ttu-id="02462-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02462-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02462-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02462-161">입력</span><span class="sxs-lookup"><span data-stu-id="02462-161">INPUTS</span></span>

### <span data-ttu-id="02462-162">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="02462-162">BatchAccountContext</span></span>
<span data-ttu-id="02462-163">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="02462-163">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="02462-164">출력</span><span class="sxs-lookup"><span data-stu-id="02462-164">OUTPUTS</span></span>

## <span data-ttu-id="02462-165">상속자</span><span class="sxs-lookup"><span data-stu-id="02462-165">NOTES</span></span>

## <span data-ttu-id="02462-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02462-166">RELATED LINKS</span></span>

[<span data-ttu-id="02462-167">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="02462-167">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="02462-168">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="02462-168">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="02462-169">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="02462-169">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="02462-170">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="02462-170">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="02462-171">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="02462-171">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="02462-172">-AzureBatchJob 제거</span><span class="sxs-lookup"><span data-stu-id="02462-172">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="02462-173">중지-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="02462-173">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="02462-174">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="02462-174">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


