---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531189"
---
# <span data-ttu-id="66236-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="66236-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="66236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66236-102">SYNOPSIS</span></span>
<span data-ttu-id="66236-103">작업 아래에 일괄 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66236-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66236-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66236-104">SYNTAX</span></span>

### <span data-ttu-id="66236-105">JobId_Single (기본값)</span><span class="sxs-lookup"><span data-stu-id="66236-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66236-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="66236-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66236-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="66236-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66236-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="66236-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66236-109">설명은</span><span class="sxs-lookup"><span data-stu-id="66236-109">DESCRIPTION</span></span>
<span data-ttu-id="66236-110">**새-AzureBatchTask** Cmdlet은 *JobId* 매개 변수 또는 *작업* 매개 변수에 의해 지정 된 작업 아래에 Azure Batch 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66236-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="66236-111">예제의</span><span class="sxs-lookup"><span data-stu-id="66236-111">EXAMPLES</span></span>

### <span data-ttu-id="66236-112">예제 1: 일괄 처리 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="66236-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="66236-113">이 명령은 ID 작업이 000001 인 작업 아래에 ID Task23 있는 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66236-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="66236-114">작업이 지정 된 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-114">The task runs the specified command.</span></span>
<span data-ttu-id="66236-115">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzureRmBatchAccountKeys** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="66236-116">예제 2: 일괄 처리 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="66236-116">Example 2: Create a Batch task</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

<span data-ttu-id="66236-117">이 명령은 **가져오기-AzureBatchJob** cmdlet을 사용 하 여 000001 ID 작업을 포함 하는 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="66236-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="66236-118">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="66236-119">이 명령은 해당 작업 아래에 ID Task26 있는 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66236-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="66236-120">작업에서 높은 권한을 사용 하 여 지정 된 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="66236-121">예제 3: 파이프라인을 사용 하 여 지정 된 작업에 작업 컬렉션 추가</span><span class="sxs-lookup"><span data-stu-id="66236-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="66236-122">첫 번째 명령은 **Get-AzureRmBatchAccountKeys** 를 사용 하 여 ContosoBatchAccount 라는 일괄 계정에 대 한 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66236-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="66236-123">명령이이 개체 참조를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="66236-124">다음 두 명령은 New-Object cmdlet을 사용 하 여 **Pscloudtask** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66236-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="66236-125">이 명령은 $Task 01 및 $Task 02 변수에 작업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="66236-126">마지막 명령은 **가져오기-AzureBatchJob** 을 사용 하 여 ID 작업이 있는 일괄 작업을 가져옵니다. 000001</span><span class="sxs-lookup"><span data-stu-id="66236-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="66236-127">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="66236-128">이 명령은 해당 작업 아래에 작업 컬렉션을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="66236-129">이 명령은 $Context에 저장 된 컨텍스트를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="66236-130">예제 4: 지정 된 작업에 작업 컬렉션 추가</span><span class="sxs-lookup"><span data-stu-id="66236-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="66236-131">첫 번째 명령은 **Get-AzureRmBatchAccountKeys** 를 사용 하 여 ContosoBatchAccount 라는 일괄 계정에 대 한 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66236-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="66236-132">명령이이 개체 참조를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="66236-133">다음 두 명령은 New-Object cmdlet을 사용 하 여 **Pscloudtask** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66236-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="66236-134">이 명령은 $Task 01 및 $Task 02 변수에 작업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="66236-135">마지막 명령은 ID 작업이 000001 인 작업 아래에 $Task 01 및 $Task 02에 저장 된 작업을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

## <span data-ttu-id="66236-136">변수</span><span class="sxs-lookup"><span data-stu-id="66236-136">PARAMETERS</span></span>

### <span data-ttu-id="66236-137">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="66236-137">-AffinityInformation</span></span>
<span data-ttu-id="66236-138">일괄 처리 서비스가 작업을 실행할 노드를 선택 하는 데 사용 하는 지역 힌트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-138">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-139">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="66236-139">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="66236-140">-BatchContext</span></span>
<span data-ttu-id="66236-141">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="66236-142">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="66236-143">-명령줄</span><span class="sxs-lookup"><span data-stu-id="66236-143">-CommandLine</span></span>
<span data-ttu-id="66236-144">작업의 명령줄을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-144">Specifies the command line for the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-145">-제약 조건</span><span class="sxs-lookup"><span data-stu-id="66236-145">-Constraints</span></span>
<span data-ttu-id="66236-146">이 작업에 적용 되는 실행 제한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-146">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-147">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="66236-147">-DependsOn</span></span>
<span data-ttu-id="66236-148">작업이 다른 작업에 의존 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-148">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="66236-149">작업은 모든 종속 작업을 성공적으로 완료할 때까지 예약 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66236-149">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-150">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="66236-150">-DisplayName</span></span>
<span data-ttu-id="66236-151">작업의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-151">Specifies the display name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-152">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="66236-152">-EnvironmentSettings</span></span>
<span data-ttu-id="66236-153">이 cmdlet이 작업에 추가 하는 환경 설정을 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-153">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="66236-154">키는 환경 설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66236-154">The key is the environment setting name.</span></span>
<span data-ttu-id="66236-155">값은 환경 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="66236-155">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-156">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="66236-156">-ExitConditions</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-157">-Id</span><span class="sxs-lookup"><span data-stu-id="66236-157">-Id</span></span>
<span data-ttu-id="66236-158">작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-158">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-159">-작업</span><span class="sxs-lookup"><span data-stu-id="66236-159">-Job</span></span>
<span data-ttu-id="66236-160">이 cmdlet이 작업을 만드는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-160">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="66236-161">**Pscloudjob** 개체를 가져오려면 Get-AzureBatchJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-161">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66236-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="66236-162">-JobId</span></span>
<span data-ttu-id="66236-163">이 cmdlet이 작업을 만드는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-163">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-164">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="66236-164">-MultiInstanceSettings</span></span>
<span data-ttu-id="66236-165">다중 인스턴스 작업을 실행 하는 방법에 대 한 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-165">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-166">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="66236-166">-ResourceFiles</span></span>
<span data-ttu-id="66236-167">작업에 필요한 리소스 파일을 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-167">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="66236-168">키는 리소스 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="66236-168">The key is the resource file path.</span></span>
<span data-ttu-id="66236-169">값은 리소스 파일 blob 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="66236-169">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-170">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="66236-170">-RunElevated</span></span>
<span data-ttu-id="66236-171">작업 프로세스가 관리자 권한으로 실행 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="66236-171">Indicates that the task process runs with administrator privileges.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-172">-작업</span><span class="sxs-lookup"><span data-stu-id="66236-172">-Tasks</span></span>
<span data-ttu-id="66236-173">추가할 작업 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-173">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="66236-174">각 작업에는 고유 ID가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-174">Each task must have a unique ID.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66236-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66236-175">-DefaultProfile</span></span>
<span data-ttu-id="66236-176">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66236-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66236-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66236-177">CommonParameters</span></span>
<span data-ttu-id="66236-178">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66236-179">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66236-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66236-180">입력</span><span class="sxs-lookup"><span data-stu-id="66236-180">INPUTS</span></span>

### <span data-ttu-id="66236-181">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="66236-181">BatchAccountContext</span></span>
<span data-ttu-id="66236-182">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-182">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="66236-183">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="66236-183">PSCloudJob</span></span>
<span data-ttu-id="66236-184">' Job ' 매개 변수는 파이프라인에서 ' PSCloudJob ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="66236-184">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="66236-185">출력</span><span class="sxs-lookup"><span data-stu-id="66236-185">OUTPUTS</span></span>

## <span data-ttu-id="66236-186">상속자</span><span class="sxs-lookup"><span data-stu-id="66236-186">NOTES</span></span>

## <span data-ttu-id="66236-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66236-187">RELATED LINKS</span></span>

[<span data-ttu-id="66236-188">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="66236-188">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="66236-189">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="66236-189">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="66236-190">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="66236-190">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="66236-191">새-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="66236-191">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="66236-192">-AzureBatchTask 제거</span><span class="sxs-lookup"><span data-stu-id="66236-192">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="66236-193">중지-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="66236-193">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="66236-194">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="66236-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


