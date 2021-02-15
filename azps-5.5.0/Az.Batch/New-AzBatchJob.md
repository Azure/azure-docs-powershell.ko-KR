---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: f997c1574a81badf9d97bb4afecc104990aa725b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197044"
---
# <span data-ttu-id="dfddd-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfddd-101">New-AzBatchJob</span></span>

## <span data-ttu-id="dfddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfddd-102">SYNOPSIS</span></span>
<span data-ttu-id="dfddd-103">Batch 서비스에서 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="dfddd-104">구문</span><span class="sxs-lookup"><span data-stu-id="dfddd-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfddd-105">설명</span><span class="sxs-lookup"><span data-stu-id="dfddd-105">DESCRIPTION</span></span>
<span data-ttu-id="dfddd-106">**New-AzBatchJob** cmdlet은 *BatchAccountContext* 매개 변수로 지정된 계정의 Azure Batch 서비스에 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="dfddd-107">예제</span><span class="sxs-lookup"><span data-stu-id="dfddd-107">EXAMPLES</span></span>

### <span data-ttu-id="dfddd-108">예제 1: 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="dfddd-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $PoolInformation.PoolId = "Pool22"
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="dfddd-109">첫 번째 명령은 New-Object cmdlet을 사용하여 **PSPoolInformation** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="dfddd-110">이 명령은 해당 개체를 $PoolInformation 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="dfddd-111">두 번째 명령은 ID Pool22를 해당 개체의 **PoolId** 속성에 $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="dfddd-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="dfddd-112">마지막 명령은 ContosoJob35 ID가 있는 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="dfddd-113">작업에 추가된 태스크는 ID Pool22가 있는 풀에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="dfddd-114">Get-AzBatchAccountKey cmdlet을 사용하여 변수 변수에 컨텍스트를 $Context.</span><span class="sxs-lookup"><span data-stu-id="dfddd-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="dfddd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfddd-115">PARAMETERS</span></span>

### <span data-ttu-id="dfddd-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dfddd-116">-BatchContext</span></span>
<span data-ttu-id="dfddd-117">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dfddd-118">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dfddd-119">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dfddd-120">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dfddd-121">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dfddd-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="dfddd-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="dfddd-123">이 cmdlet이 작업의 모든 태스크에 대해 설정하는 공통 환경 변수를 키/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="dfddd-124">키는 환경 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-124">The key is the environment variable name.</span></span>
<span data-ttu-id="dfddd-125">값은 환경 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-125">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfddd-126">-Constraints</span><span class="sxs-lookup"><span data-stu-id="dfddd-126">-Constraints</span></span>
<span data-ttu-id="dfddd-127">작업의 실행 제약 조건을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-127">Specifies the execution constraints for the job.</span></span>

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

### <span data-ttu-id="dfddd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfddd-128">-DefaultProfile</span></span>
<span data-ttu-id="dfddd-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfddd-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dfddd-130">-DisplayName</span></span>
<span data-ttu-id="dfddd-131">작업의 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="dfddd-132">-Id</span><span class="sxs-lookup"><span data-stu-id="dfddd-132">-Id</span></span>
<span data-ttu-id="dfddd-133">작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="dfddd-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="dfddd-134">-JobManagerTask</span></span>
<span data-ttu-id="dfddd-135">작업 관리자 태스크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="dfddd-136">Batch 서비스는 작업이 시작되는 경우 작업 관리자 태스크를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-136">The Batch service runs the Job Manager task when the job is started.</span></span>

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

### <span data-ttu-id="dfddd-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="dfddd-137">-JobPreparationTask</span></span>
<span data-ttu-id="dfddd-138">작업 준비 태스크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="dfddd-139">Batch 서비스는 해당 계산 노드에서 해당 작업의 태스크를 시작하기 전에 계산 노드에서 작업 준비 태스크를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

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

### <span data-ttu-id="dfddd-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="dfddd-140">-JobReleaseTask</span></span>
<span data-ttu-id="dfddd-141">작업 릴리스 태스크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="dfddd-142">Batch 서비스는 작업이 종료될 때 작업 릴리스 태스크를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="dfddd-143">Batch 서비스는 작업의 태스크를 실행한 각 계산 노드에서 작업 릴리스 태스크를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

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

### <span data-ttu-id="dfddd-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="dfddd-144">-Metadata</span></span>
<span data-ttu-id="dfddd-145">작업에서 추가할 메타데이터를 키/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="dfddd-146">키는 메타데이터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-146">The key is the metadata name.</span></span>
<span data-ttu-id="dfddd-147">값은 메타데이터 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-147">The value is the metadata value.</span></span>

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

### <span data-ttu-id="dfddd-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="dfddd-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="dfddd-149">작업의 모든 태스크가 완료된 상태인 경우 Batch 서비스에서 수행하는 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

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

### <span data-ttu-id="dfddd-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="dfddd-150">-OnTaskFailure</span></span>
<span data-ttu-id="dfddd-151">작업의 태스크가 실패하는 경우 Batch 서비스가 취하는 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

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

### <span data-ttu-id="dfddd-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="dfddd-152">-PoolInformation</span></span>
<span data-ttu-id="dfddd-153">Batch 서비스가 작업의 태스크를 실행하는 풀의 세부 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

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

### <span data-ttu-id="dfddd-154">-Priority</span><span class="sxs-lookup"><span data-stu-id="dfddd-154">-Priority</span></span>
<span data-ttu-id="dfddd-155">작업의 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="dfddd-156">유효한 값은 -1000에서 1000까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="dfddd-157">-1000 값은 가장 낮은 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="dfddd-158">값이 1000이 가장 높은 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="dfddd-159">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-159">The default value is 0.</span></span>

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

### <span data-ttu-id="dfddd-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="dfddd-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="dfddd-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfddd-161">CommonParameters</span></span>
<span data-ttu-id="dfddd-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dfddd-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfddd-163">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dfddd-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfddd-164">입력</span><span class="sxs-lookup"><span data-stu-id="dfddd-164">INPUTS</span></span>

### <span data-ttu-id="dfddd-165">System.String</span><span class="sxs-lookup"><span data-stu-id="dfddd-165">System.String</span></span>

### <span data-ttu-id="dfddd-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dfddd-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dfddd-167">출력</span><span class="sxs-lookup"><span data-stu-id="dfddd-167">OUTPUTS</span></span>

### <span data-ttu-id="dfddd-168">System.Void</span><span class="sxs-lookup"><span data-stu-id="dfddd-168">System.Void</span></span>

## <span data-ttu-id="dfddd-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dfddd-169">NOTES</span></span>

## <span data-ttu-id="dfddd-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfddd-170">RELATED LINKS</span></span>

[<span data-ttu-id="dfddd-171">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfddd-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="dfddd-172">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfddd-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="dfddd-173">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="dfddd-173">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="dfddd-174">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfddd-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="dfddd-175">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dfddd-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="dfddd-176">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfddd-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="dfddd-177">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfddd-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="dfddd-178">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dfddd-178">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
