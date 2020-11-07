---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: 09e2d3effbe99c6f0f126b0665330b077f27af80
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880218"
---
# <span data-ttu-id="26188-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26188-101">New-AzBatchJob</span></span>

## <span data-ttu-id="26188-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26188-102">SYNOPSIS</span></span>
<span data-ttu-id="26188-103">일괄 처리 서비스에 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26188-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="26188-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26188-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26188-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26188-105">DESCRIPTION</span></span>
<span data-ttu-id="26188-106">**AzBatchJob** Cmdlet은 *batchaccountcontext* 매개 변수에 지정 된 계정의 Azure 일괄 처리 서비스에서 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26188-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="26188-107">예제의</span><span class="sxs-lookup"><span data-stu-id="26188-107">EXAMPLES</span></span>

### <span data-ttu-id="26188-108">예제 1: 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="26188-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="26188-109">첫 번째 명령은 New-Object cmdlet을 사용 하 여 **PSPoolInformation** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26188-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="26188-110">명령이 $PoolInformation 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="26188-111">두 번째 명령은 $PoolInformation에 있는 개체의 **PoolId** 속성에 ID Pool22를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="26188-112">마지막 명령은 ID ContosoJob35를 가진 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26188-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="26188-113">작업에 추가 된 작업은 ID Pool22를 가진 풀에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26188-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="26188-114">Get-AzBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-114">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="26188-115">변수</span><span class="sxs-lookup"><span data-stu-id="26188-115">PARAMETERS</span></span>

### <span data-ttu-id="26188-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="26188-116">-BatchContext</span></span>
<span data-ttu-id="26188-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="26188-118">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26188-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="26188-119">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26188-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="26188-120">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26188-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="26188-121">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="26188-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="26188-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="26188-123">이 cmdlet이 작업의 모든 작업에 대해 설정 하는 공통 환경 변수를 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="26188-124">키는 환경 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26188-124">The key is the environment variable name.</span></span>
<span data-ttu-id="26188-125">값은 환경 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="26188-125">The value is the environment variable value.</span></span>

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

### <span data-ttu-id="26188-126">-제약 조건</span><span class="sxs-lookup"><span data-stu-id="26188-126">-Constraints</span></span>
<span data-ttu-id="26188-127">작업에 대 한 실행 제약 조건을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-127">Specifies the execution constraints for the job.</span></span>

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

### <span data-ttu-id="26188-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26188-128">-DefaultProfile</span></span>
<span data-ttu-id="26188-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26188-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26188-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="26188-130">-DisplayName</span></span>
<span data-ttu-id="26188-131">작업의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="26188-132">-Id</span><span class="sxs-lookup"><span data-stu-id="26188-132">-Id</span></span>
<span data-ttu-id="26188-133">작업에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="26188-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="26188-134">-JobManagerTask</span></span>
<span data-ttu-id="26188-135">작업 관리자 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="26188-136">작업이 시작 되 면 일괄 처리 서비스가 작업 관리자 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-136">The Batch service runs the Job Manager task when the job is started.</span></span>

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

### <span data-ttu-id="26188-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="26188-137">-JobPreparationTask</span></span>
<span data-ttu-id="26188-138">작업 준비 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="26188-139">일괄 처리 서비스는 계산 노드에서 작업 준비 작업을 실행 한 후 해당 작업의 계산 노드에서 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

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

### <span data-ttu-id="26188-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="26188-140">-JobReleaseTask</span></span>
<span data-ttu-id="26188-141">작업 릴리스 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="26188-142">일괄 처리 서비스는 작업이 종료 될 때 작업 릴리스 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="26188-143">일괄 처리 서비스는 작업의 작업을 실행 한 각 계산 노드에서 작업 릴리스 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

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

### <span data-ttu-id="26188-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="26188-144">-Metadata</span></span>
<span data-ttu-id="26188-145">작업에 추가할 메타 데이터를 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="26188-146">키는 메타 데이터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26188-146">The key is the metadata name.</span></span>
<span data-ttu-id="26188-147">값은 메타 데이터 값입니다.</span><span class="sxs-lookup"><span data-stu-id="26188-147">The value is the metadata value.</span></span>

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

### <span data-ttu-id="26188-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="26188-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="26188-149">작업의 모든 작업이 완료 됨 상태인 경우 일괄 처리 서비스에서 수행 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

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

### <span data-ttu-id="26188-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="26188-150">-OnTaskFailure</span></span>
<span data-ttu-id="26188-151">작업의 작업이 실패 하는 경우 일괄 처리 서비스에서 수행 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

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

### <span data-ttu-id="26188-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="26188-152">-PoolInformation</span></span>
<span data-ttu-id="26188-153">일괄 처리 서비스가 작업의 작업을 실행 하는 풀의 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

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

### <span data-ttu-id="26188-154">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="26188-154">-Priority</span></span>
<span data-ttu-id="26188-155">작업의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="26188-156">유효한 값은-1000에서 1000 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="26188-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="26188-157">값-1000은 가장 낮은 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="26188-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="26188-158">1000의 값은 가장 높은 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="26188-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="26188-159">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="26188-159">The default value is 0.</span></span>

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

### <span data-ttu-id="26188-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="26188-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="26188-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26188-161">CommonParameters</span></span>
<span data-ttu-id="26188-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26188-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26188-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26188-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26188-164">입력</span><span class="sxs-lookup"><span data-stu-id="26188-164">INPUTS</span></span>

### <span data-ttu-id="26188-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="26188-165">System.String</span></span>

### <span data-ttu-id="26188-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="26188-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="26188-167">출력</span><span class="sxs-lookup"><span data-stu-id="26188-167">OUTPUTS</span></span>

### <span data-ttu-id="26188-168">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="26188-168">System.Void</span></span>

## <span data-ttu-id="26188-169">상속자</span><span class="sxs-lookup"><span data-stu-id="26188-169">NOTES</span></span>

## <span data-ttu-id="26188-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26188-170">RELATED LINKS</span></span>

[<span data-ttu-id="26188-171">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26188-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="26188-172">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26188-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="26188-173">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="26188-173">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="26188-174">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26188-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="26188-175">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="26188-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="26188-176">제거-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26188-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="26188-177">중지-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26188-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="26188-178">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26188-178">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


