---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 254c9290b2cc838dc7ec53c2590d8505c24c1b69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992959"
---
# <span data-ttu-id="88c02-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88c02-101">New-AzBatchTask</span></span>

## <span data-ttu-id="88c02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88c02-102">SYNOPSIS</span></span>
<span data-ttu-id="88c02-103">작업 아래에 Batch 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="88c02-104">구문</span><span class="sxs-lookup"><span data-stu-id="88c02-104">SYNTAX</span></span>

### <span data-ttu-id="88c02-105">JobId_Single(기본값)</span><span class="sxs-lookup"><span data-stu-id="88c02-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88c02-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="88c02-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88c02-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="88c02-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88c02-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="88c02-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88c02-109">설명</span><span class="sxs-lookup"><span data-stu-id="88c02-109">DESCRIPTION</span></span>
<span data-ttu-id="88c02-110">**New-AzBatchTask** cmdlet은 *JobId* 매개 변수 또는 작업 매개 변수에 의해 지정된 작업에서 Azure Batch *작업을 만듭니다.*</span><span class="sxs-lookup"><span data-stu-id="88c02-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="88c02-111">예제</span><span class="sxs-lookup"><span data-stu-id="88c02-111">EXAMPLES</span></span>

### <span data-ttu-id="88c02-112">예제 1: Batch 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="88c02-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="88c02-113">이 명령은 ID 작업-0000001이 있는 작업 아래에 ID Task23이 있는 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="88c02-114">태스크는 지정된 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-114">The task runs the specified command.</span></span>
<span data-ttu-id="88c02-115">**Get-AzBatchAccountKey** cmdlet을 사용하여 $Context 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-115">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="88c02-116">예제 2: Batch 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="88c02-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="88c02-117">이 명령은 **Get-AzBatchJob** cmdlet을 사용하여 ID Job-000001이 있는 Batch 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="88c02-118">명령은 파이프라인 연산자를 사용하여 현재 cmdlet에 이 작업을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="88c02-119">명령은 이 작업 아래에 ID Task26이 있는 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="88c02-120">태스크는 권한 상승된 권한을 사용하여 지정된 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="88c02-121">예제 3: 파이프라인을 사용하여 지정된 작업에 작업 컬렉션 추가</span><span class="sxs-lookup"><span data-stu-id="88c02-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="88c02-122">첫 번째 명령은 **Get-AzBatchAccountKey를 사용하여 ContosoBatchAccount라는** 일괄 처리 계정에 대한 계정 키에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="88c02-123">명령은 이 개체 참조를 $Context 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="88c02-124">다음 두 명령은 New-Object cmdlet을 사용하여 **PSCloudTask** 개체를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="88c02-125">명령은 $Task 01 및 $Task 02 변수에 작업을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="88c02-126">마지막 명령은 **Get-AzBatchJob** 을 사용하여 ID Job-000001이 있는 Batch 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="88c02-127">그런 다음, 명령은 파이프라인 연산자를 사용하여 해당 작업을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="88c02-128">명령은 해당 작업의 작업 컬렉션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="88c02-129">명령은 에 저장된 컨텍스트를 $Context.</span><span class="sxs-lookup"><span data-stu-id="88c02-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="88c02-130">예제 4: 지정된 작업에 작업 컬렉션 추가</span><span class="sxs-lookup"><span data-stu-id="88c02-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="88c02-131">첫 번째 명령은 **Get-AzBatchAccountKey를 사용하여 ContosoBatchAccount라는** 일괄 처리 계정에 대한 계정 키에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="88c02-132">명령은 이 개체 참조를 $Context 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="88c02-133">다음 두 명령은 New-Object cmdlet을 사용하여 **PSCloudTask** 개체를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="88c02-134">명령은 $Task 01 및 $Task 02 변수에 작업을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="88c02-135">최종 명령은 ID Job-000001이 있는 작업 아래에 $Task 01 및 $Task 02에 저장된 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="88c02-136">예제 5: 출력 파일이 있는 작업 추가</span><span class="sxs-lookup"><span data-stu-id="88c02-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="88c02-137">예제 6: 인증 토큰 설정이 있는 작업 추가</span><span class="sxs-lookup"><span data-stu-id="88c02-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="88c02-138">예제 7: 컨테이너에서 실행되는 작업 추가</span><span class="sxs-lookup"><span data-stu-id="88c02-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="88c02-139">매개 변수</span><span class="sxs-lookup"><span data-stu-id="88c02-139">PARAMETERS</span></span>

### <span data-ttu-id="88c02-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="88c02-140">-AffinityInformation</span></span>
<span data-ttu-id="88c02-141">Batch 서비스가 태스크를 실행할 노드를 선택하는 데 사용하는 지역성 힌트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="88c02-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="88c02-142">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c02-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="88c02-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="88c02-144">태스크가 Batch 서비스 작업을 수행하는 데 사용할 수 있는 인증 토큰에 대한 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="88c02-145">이 설정이 설정된 경우 Batch 서비스는 계정 액세스 키 없이 Batch 서비스 작업을 인증하는 데 사용할 수 있는 인증 토큰을 태스크에 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="88c02-146">토큰은 AZ_BATCH_AUTHENTICATION_TOKEN 변수를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="88c02-147">토큰을 사용하여 태스크가 수행될 수 있는 작업은 설정에 따라 달라 니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="88c02-148">예를 들어 태스크는 작업에 다른 작업을 추가하거나 작업 또는 다른 작업의 상태를 확인하기 위해 작업 권한을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c02-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="88c02-149">-BatchContext</span></span>
<span data-ttu-id="88c02-150">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88c02-151">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="88c02-152">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-152">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="88c02-153">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="88c02-154">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="88c02-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="88c02-155">-CommandLine</span></span>
<span data-ttu-id="88c02-156">작업에 대한 명령줄을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="88c02-157">-제약 조건</span><span class="sxs-lookup"><span data-stu-id="88c02-157">-Constraints</span></span>
<span data-ttu-id="88c02-158">이 작업에 적용되는 실행 제약 조건을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="88c02-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="88c02-159">-ContainerSettings</span></span>
<span data-ttu-id="88c02-160">작업이 실행되는 컨테이너에 대한 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="88c02-161">이 작업을 실행할 풀에 containerConfiguration 집합이 있는 경우 이 설정도 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="88c02-162">이 작업을 실행할 풀에 containerConfiguration 집합이 없는 경우 이 집합을 설정하지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="88c02-163">이 지정이 지정되면 모든 AZ_BATCH_NODE_ROOT_DIR(노드의 Azure Batch AZ_BATCH_NODE_ROOT_DIR 루트)는 컨테이너에 매핑되고, 모든 작업 환경 변수가 컨테이너에 매핑되고 작업 명령줄이 컨테이너에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c02-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c02-164">-DefaultProfile</span></span>
<span data-ttu-id="88c02-165">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88c02-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="88c02-166">-DependsOn</span></span>
<span data-ttu-id="88c02-167">작업이 다른 작업에 종속되는지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="88c02-168">모든 종속된 작업이 성공적으로 완료될 때까지 작업이 예약되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="88c02-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="88c02-169">-DisplayName</span></span>
<span data-ttu-id="88c02-170">작업의 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="88c02-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="88c02-171">-EnvironmentSettings</span></span>
<span data-ttu-id="88c02-172">이 cmdlet이 작업에 추가하는 환경 설정을 키/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="88c02-173">키는 환경 설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-173">The key is the environment setting name.</span></span>
<span data-ttu-id="88c02-174">값은 환경 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-174">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c02-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="88c02-175">-ExitConditions</span></span>
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

### <span data-ttu-id="88c02-176">-Id</span><span class="sxs-lookup"><span data-stu-id="88c02-176">-Id</span></span>
<span data-ttu-id="88c02-177">작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="88c02-178">-Job</span><span class="sxs-lookup"><span data-stu-id="88c02-178">-Job</span></span>
<span data-ttu-id="88c02-179">이 cmdlet에서 작업을 만드는 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="88c02-180">**PSCloudJob** 개체를 얻은 경우 Get-AzBatchJob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="88c02-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="88c02-181">-JobId</span></span>
<span data-ttu-id="88c02-182">이 cmdlet에서 작업을 만드는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="88c02-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="88c02-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="88c02-184">다중 인스턴스 작업을 실행하는 방법에 대한 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="88c02-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="88c02-185">-OutputFile</span></span>
<span data-ttu-id="88c02-186">명령줄을 실행한 후 Batch 서비스가 계산 노드에서 업로드할 파일 목록을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="88c02-187">다중 인스턴스 작업의 경우 파일은 기본 작업이 실행되는 계산 노드에서만 업로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c02-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="88c02-188">-ResourceFiles</span></span>
<span data-ttu-id="88c02-189">작업에 필요한 키/값 쌍으로 리소스 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="88c02-190">키는 리소스 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-190">The key is the resource file path.</span></span>
<span data-ttu-id="88c02-191">값은 리소스 파일 Blob 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-191">The value is the resource file blob source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSResourceFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c02-192">-작업</span><span class="sxs-lookup"><span data-stu-id="88c02-192">-Tasks</span></span>
<span data-ttu-id="88c02-193">추가할 작업의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="88c02-194">각 작업에는 고유한 ID가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="88c02-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="88c02-195">-UserIdentity</span></span>
<span data-ttu-id="88c02-196">작업이 실행되는 사용자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-196">The user identity under which the task runs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c02-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c02-197">CommonParameters</span></span>
<span data-ttu-id="88c02-198">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88c02-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c02-199">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88c02-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c02-200">입력</span><span class="sxs-lookup"><span data-stu-id="88c02-200">INPUTS</span></span>

### <span data-ttu-id="88c02-201">Microsoft.Azure.Commands.Bat. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="88c02-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="88c02-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="88c02-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="88c02-203">출력</span><span class="sxs-lookup"><span data-stu-id="88c02-203">OUTPUTS</span></span>

### <span data-ttu-id="88c02-204">System.Void</span><span class="sxs-lookup"><span data-stu-id="88c02-204">System.Void</span></span>

## <span data-ttu-id="88c02-205">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88c02-205">NOTES</span></span>

## <span data-ttu-id="88c02-206">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88c02-206">RELATED LINKS</span></span>

[<span data-ttu-id="88c02-207">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="88c02-207">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="88c02-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="88c02-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="88c02-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88c02-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="88c02-210">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88c02-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="88c02-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88c02-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="88c02-212">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88c02-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="88c02-213">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="88c02-213">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
