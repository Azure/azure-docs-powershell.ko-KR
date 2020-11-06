---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: a081e6da07557033430033adc8ef28cb4b63da8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528628"
---
# <span data-ttu-id="656f4-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="656f4-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="656f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="656f4-102">SYNOPSIS</span></span>
<span data-ttu-id="656f4-103">작업 아래에 일괄 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="656f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="656f4-104">SYNTAX</span></span>

### <span data-ttu-id="656f4-105">JobId_Single (기본값)</span><span class="sxs-lookup"><span data-stu-id="656f4-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="656f4-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="656f4-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="656f4-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="656f4-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="656f4-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="656f4-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="656f4-109">설명은</span><span class="sxs-lookup"><span data-stu-id="656f4-109">DESCRIPTION</span></span>
<span data-ttu-id="656f4-110">**새-AzureBatchTask** Cmdlet은 *JobId* 매개 변수 또는 *작업* 매개 변수에 의해 지정 된 작업 아래에 Azure Batch 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="656f4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="656f4-111">EXAMPLES</span></span>

### <span data-ttu-id="656f4-112">예제 1: 일괄 처리 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="656f4-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="656f4-113">이 명령은 ID 작업이 000001 인 작업 아래에 ID Task23 있는 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="656f4-114">작업이 지정 된 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-114">The task runs the specified command.</span></span>
<span data-ttu-id="656f4-115">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzureRmBatchAccountKeys** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="656f4-116">예제 2: 일괄 처리 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="656f4-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="656f4-117">이 명령은 **가져오기-AzureBatchJob** cmdlet을 사용 하 여 000001 ID 작업을 포함 하는 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="656f4-118">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="656f4-119">이 명령은 해당 작업 아래에 ID Task26 있는 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="656f4-120">작업에서 높은 권한을 사용 하 여 지정 된 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="656f4-121">예제 3: 파이프라인을 사용 하 여 지정 된 작업에 작업 컬렉션 추가</span><span class="sxs-lookup"><span data-stu-id="656f4-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="656f4-122">첫 번째 명령은 **Get-AzureRmBatchAccountKeys** 를 사용 하 여 ContosoBatchAccount 라는 일괄 계정에 대 한 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="656f4-123">명령이이 개체 참조를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="656f4-124">다음 두 명령은 New-Object cmdlet을 사용 하 여 **Pscloudtask** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="656f4-125">이 명령은 $Task 01 및 $Task 02 변수에 작업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="656f4-126">마지막 명령은 **가져오기-AzureBatchJob** 을 사용 하 여 ID 작업이 있는 일괄 작업을 가져옵니다. 000001</span><span class="sxs-lookup"><span data-stu-id="656f4-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="656f4-127">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="656f4-128">이 명령은 해당 작업 아래에 작업 컬렉션을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="656f4-129">이 명령은 $Context에 저장 된 컨텍스트를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="656f4-130">예제 4: 지정 된 작업에 작업 컬렉션 추가</span><span class="sxs-lookup"><span data-stu-id="656f4-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="656f4-131">첫 번째 명령은 **Get-AzureRmBatchAccountKeys** 를 사용 하 여 ContosoBatchAccount 라는 일괄 계정에 대 한 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="656f4-132">명령이이 개체 참조를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="656f4-133">다음 두 명령은 New-Object cmdlet을 사용 하 여 **Pscloudtask** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="656f4-134">이 명령은 $Task 01 및 $Task 02 변수에 작업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="656f4-135">마지막 명령은 ID 작업이 000001 인 작업 아래에 $Task 01 및 $Task 02에 저장 된 작업을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="656f4-136">예제 5: 출력 파일이 있는 작업 추가</span><span class="sxs-lookup"><span data-stu-id="656f4-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="656f4-137">예제 6: 인증 토큰 설정이 있는 작업 추가</span><span class="sxs-lookup"><span data-stu-id="656f4-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="656f4-138">예제 7: 컨테이너에서 실행 되는 작업 추가</span><span class="sxs-lookup"><span data-stu-id="656f4-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="656f4-139">변수</span><span class="sxs-lookup"><span data-stu-id="656f4-139">PARAMETERS</span></span>

### <span data-ttu-id="656f4-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="656f4-140">-AffinityInformation</span></span>
<span data-ttu-id="656f4-141">일괄 처리 서비스가 작업을 실행할 노드를 선택 하는 데 사용 하는 지역 힌트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="656f4-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="656f4-142">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="656f4-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="656f4-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="656f4-144">작업에서 일괄 처리 서비스 작업을 수행 하는 데 사용할 수 있는 인증 토큰에 대 한 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="656f4-145">이 설정을 선택 하면 일괄 처리 서비스에서 계정 액세스 키 없이 일괄 처리 서비스 작업을 인증 하는 데 사용할 수 있는 인증 토큰이 있는 작업을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="656f4-146">토큰은 AZ_BATCH_AUTHENTICATION_TOKEN 환경 변수를 통해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="656f4-147">토큰을 사용 하 여 수행할 수 있는 작업은 설정에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="656f4-148">예를 들어 작업에 다른 작업을 추가 하거나 작업 또는 다른 작업의 상태를 확인 하기 위해 작업이 작업 권한을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

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

### <span data-ttu-id="656f4-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="656f4-149">-BatchContext</span></span>
<span data-ttu-id="656f4-150">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="656f4-151">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-151">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="656f4-152">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-152">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="656f4-153">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="656f4-154">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="656f4-155">-명령줄</span><span class="sxs-lookup"><span data-stu-id="656f4-155">-CommandLine</span></span>
<span data-ttu-id="656f4-156">작업의 명령줄을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="656f4-157">-제약 조건</span><span class="sxs-lookup"><span data-stu-id="656f4-157">-Constraints</span></span>
<span data-ttu-id="656f4-158">이 작업에 적용 되는 실행 제한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="656f4-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="656f4-159">-ContainerSettings</span></span>
<span data-ttu-id="656f4-160">작업이 실행 되는 컨테이너에 대 한 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="656f4-161">이 작업을 실행 하는 풀에 containerConfiguration가 설정 되어 있는 경우에도이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="656f4-162">이 작업을 실행 하는 풀에 containerConfiguration가 설정 되어 있지 않으면이를 설정 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="656f4-163">이를 지정 하면 AZ_BATCH_NODE_ROOT_DIR 아래에 재귀적으로 모든 디렉터리가 컨테이너에 매핑되고, 모든 작업 환경 변수는 컨테이너에 매핑되고, 작업 명령줄이 컨테이너에서 실행 됩니다..</span><span class="sxs-lookup"><span data-stu-id="656f4-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

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

### <span data-ttu-id="656f4-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="656f4-164">-DefaultProfile</span></span>
<span data-ttu-id="656f4-165">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="656f4-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="656f4-166">-DependsOn</span></span>
<span data-ttu-id="656f4-167">작업이 다른 작업에 의존 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="656f4-168">작업은 모든 종속 작업을 성공적으로 완료할 때까지 예약 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="656f4-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="656f4-169">-DisplayName</span></span>
<span data-ttu-id="656f4-170">작업의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="656f4-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="656f4-171">-EnvironmentSettings</span></span>
<span data-ttu-id="656f4-172">이 cmdlet이 작업에 추가 하는 환경 설정을 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="656f4-173">키는 환경 설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-173">The key is the environment setting name.</span></span>
<span data-ttu-id="656f4-174">값은 환경 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-174">The value is the environment setting.</span></span>

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

### <span data-ttu-id="656f4-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="656f4-175">-ExitConditions</span></span>
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

### <span data-ttu-id="656f4-176">-Id</span><span class="sxs-lookup"><span data-stu-id="656f4-176">-Id</span></span>
<span data-ttu-id="656f4-177">작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="656f4-178">-작업</span><span class="sxs-lookup"><span data-stu-id="656f4-178">-Job</span></span>
<span data-ttu-id="656f4-179">이 cmdlet이 작업을 만드는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="656f4-180">**Pscloudjob** 개체를 가져오려면 Get-AzureBatchJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-180">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="656f4-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="656f4-181">-JobId</span></span>
<span data-ttu-id="656f4-182">이 cmdlet이 작업을 만드는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="656f4-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="656f4-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="656f4-184">다중 인스턴스 작업을 실행 하는 방법에 대 한 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="656f4-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="656f4-185">-OutputFile</span></span>
<span data-ttu-id="656f4-186">명령줄을 실행 한 후 계산 노드에서 일괄 처리 서비스를 업로드할 파일 목록을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="656f4-187">다중 인스턴스 작업의 경우 기본 작업이 실행 되는 계산 노드에서만 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

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

### <span data-ttu-id="656f4-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="656f4-188">-ResourceFiles</span></span>
<span data-ttu-id="656f4-189">작업에 필요한 리소스 파일을 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="656f4-190">키는 리소스 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-190">The key is the resource file path.</span></span>
<span data-ttu-id="656f4-191">값은 리소스 파일 blob 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-191">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="656f4-192">-작업</span><span class="sxs-lookup"><span data-stu-id="656f4-192">-Tasks</span></span>
<span data-ttu-id="656f4-193">추가할 작업 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="656f4-194">각 작업에는 고유 ID가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="656f4-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="656f4-195">-UserIdentity</span></span>
<span data-ttu-id="656f4-196">작업이 실행 되는 사용자 id입니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-196">The user identity under which the task runs.</span></span>

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

### <span data-ttu-id="656f4-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="656f4-197">CommonParameters</span></span>
<span data-ttu-id="656f4-198">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="656f4-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="656f4-199">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="656f4-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="656f4-200">입력</span><span class="sxs-lookup"><span data-stu-id="656f4-200">INPUTS</span></span>

### <span data-ttu-id="656f4-201">Microsoft.Azure.Commands.Batch. PSCloudJob 모델</span><span class="sxs-lookup"><span data-stu-id="656f4-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="656f4-202">매개 변수: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="656f4-202">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="656f4-203">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="656f4-203">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="656f4-204">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="656f4-204">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="656f4-205">출력</span><span class="sxs-lookup"><span data-stu-id="656f4-205">OUTPUTS</span></span>

### <span data-ttu-id="656f4-206">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="656f4-206">System.Void</span></span>

## <span data-ttu-id="656f4-207">상속자</span><span class="sxs-lookup"><span data-stu-id="656f4-207">NOTES</span></span>

## <span data-ttu-id="656f4-208">관련 링크</span><span class="sxs-lookup"><span data-stu-id="656f4-208">RELATED LINKS</span></span>

[<span data-ttu-id="656f4-209">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="656f4-209">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="656f4-210">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="656f4-210">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="656f4-211">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="656f4-211">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="656f4-212">새-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="656f4-212">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="656f4-213">-AzureBatchTask 제거</span><span class="sxs-lookup"><span data-stu-id="656f4-213">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="656f4-214">중지-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="656f4-214">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="656f4-215">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="656f4-215">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


