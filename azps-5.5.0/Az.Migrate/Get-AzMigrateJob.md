---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190188"
---
# <span data-ttu-id="a3df8-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="a3df8-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="a3df8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3df8-102">SYNOPSIS</span></span>
<span data-ttu-id="a3df8-103">Azure Migrate 작업의 상태를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="a3df8-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3df8-104">SYNTAX</span></span>

### <span data-ttu-id="a3df8-105">ListByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a3df8-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3df8-106">GetById</span><span class="sxs-lookup"><span data-stu-id="a3df8-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3df8-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a3df8-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3df8-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="a3df8-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3df8-109">ListById</span><span class="sxs-lookup"><span data-stu-id="a3df8-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a3df8-110">설명</span><span class="sxs-lookup"><span data-stu-id="a3df8-110">DESCRIPTION</span></span>
<span data-ttu-id="a3df8-111">Get-AzMigrateJob cmdlet은 Azure Migrate 작업의 상태를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="a3df8-112">예제</span><span class="sxs-lookup"><span data-stu-id="a3df8-112">EXAMPLES</span></span>

### <span data-ttu-id="a3df8-113">예제 1: 작업 ID로 얻기</span><span class="sxs-lookup"><span data-stu-id="a3df8-113">Example 1: Get By Job Id</span></span>
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="a3df8-114">ID로 작업을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="a3df8-115">예제 2: 리소스 그룹 및 프로젝트로 나열</span><span class="sxs-lookup"><span data-stu-id="a3df8-115">Example 2: List by resource group and project</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="a3df8-116">그러면 프로젝트의 모든 작업이 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="a3df8-117">예제 3: 리소스 그룹, 프로젝트 및 작업 이름에 따라 얻기</span><span class="sxs-lookup"><span data-stu-id="a3df8-117">Example 3: Get by resource group, project and job name</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="a3df8-118">특정 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-118">This gets a specific job.</span></span>

## <span data-ttu-id="a3df8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3df8-119">PARAMETERS</span></span>

### <span data-ttu-id="a3df8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3df8-120">-DefaultProfile</span></span>
<span data-ttu-id="a3df8-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3df8-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="a3df8-122">-Filter</span></span>
<span data-ttu-id="a3df8-123">OData 필터 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-123">OData filter options.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3df8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3df8-124">-InputObject</span></span>
<span data-ttu-id="a3df8-125">복제 서버의 작업 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="a3df8-126">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a3df8-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3df8-127">-JobID</span><span class="sxs-lookup"><span data-stu-id="a3df8-127">-JobID</span></span>
<span data-ttu-id="a3df8-128">세부 정보를 검색해야 하는 작업 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-128">Specifies the job id for which the details needs to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3df8-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="a3df8-129">-JobName</span></span>
<span data-ttu-id="a3df8-130">작업 식별자</span><span class="sxs-lookup"><span data-stu-id="a3df8-130">Job identifier</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3df8-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="a3df8-131">-ProjectID</span></span>
<span data-ttu-id="a3df8-132">서버가 복제되는 Azure Migrate 프로젝트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3df8-133">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="a3df8-133">-ProjectName</span></span>
<span data-ttu-id="a3df8-134">마이그레이션 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-134">The name of the migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3df8-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="a3df8-135">-ResourceGroupID</span></span>
<span data-ttu-id="a3df8-136">현재 구독에서 Azure Migrate 프로젝트의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3df8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3df8-137">-ResourceGroupName</span></span>
<span data-ttu-id="a3df8-138">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-138">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3df8-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3df8-139">-SubscriptionId</span></span>
<span data-ttu-id="a3df8-140">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-140">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3df8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3df8-141">CommonParameters</span></span>
<span data-ttu-id="a3df8-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3df8-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3df8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3df8-144">입력</span><span class="sxs-lookup"><span data-stu-id="a3df8-144">INPUTS</span></span>

## <span data-ttu-id="a3df8-145">출력</span><span class="sxs-lookup"><span data-stu-id="a3df8-145">OUTPUTS</span></span>

### <span data-ttu-id="a3df8-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="a3df8-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="a3df8-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3df8-147">NOTES</span></span>

<span data-ttu-id="a3df8-148">별칭</span><span class="sxs-lookup"><span data-stu-id="a3df8-148">ALIASES</span></span>

<span data-ttu-id="a3df8-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a3df8-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3df8-150">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3df8-151">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3df8-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3df8-152">INPUTOBJECT: 복제 서버의 <IJob> 작업 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="a3df8-153">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="a3df8-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="a3df8-154">`[ActivityId <String>]`: 활동 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="a3df8-155">`[AllowedAction <String[]>]`: 작업이 허용되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="a3df8-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: 워크플로 개체 세부 정보를 기반으로 원본 서버, 원본 클라우드, 대상 서버, 대상 클라우드와 같은 영향을 받는 개체 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="a3df8-157">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a3df8-158">`[EndTime <DateTime?>]`: 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="a3df8-159">`[Error <IJobErrorDetails[]>]`: 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="a3df8-160">`[CreationTime <DateTime?>]`: 작업 오류의 생성 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="a3df8-161">`[ErrorLevel <String>]`: 오류 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="a3df8-162">`[ProviderErrorDetailErrorCode <Int32?>]`: 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="a3df8-163">`[ProviderErrorDetailErrorId <String>]`: 공급자 오류 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="a3df8-164">`[ProviderErrorDetailErrorMessage <String>]`: 오류 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="a3df8-165">`[ProviderErrorDetailPossibleCaus <String>]`: 오류의 가능한 원인입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="a3df8-166">`[ProviderErrorDetailRecommendedAction <String>]`: 오류를 해결하는 데 권장되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="a3df8-167">`[ServiceErrorDetailActivityId <String>]`: 활동 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="a3df8-168">`[ServiceErrorDetailCode <String>]`: 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="a3df8-169">`[ServiceErrorDetailMessage <String>]`: 오류 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="a3df8-170">`[ServiceErrorDetailPossibleCaus <String>]`: 오류의 가능한 원인입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="a3df8-171">`[ServiceErrorDetailRecommendedAction <String>]`: 오류를 해결하기 위한 권장 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="a3df8-172">`[TaskId <String>]`: 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="a3df8-173">`[FriendlyName <String>]`: DisplayName입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="a3df8-174">`[ScenarioName <String>]`: ScenarioName입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="a3df8-175">`[StartTime <DateTime?>]`: 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="a3df8-176">`[State <String>]`: 작업의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="a3df8-177">NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended 또는 Other 값 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="a3df8-178">`[StateDescription <String>]`: 작업의 상태 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="a3df8-179">예: 성공 상태의 경우 설명은 Completed, PartiallySucceeded, CompletedWithInformation 또는 Skipped일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="a3df8-180">`[TargetInstanceType <String>]`: {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} 클래스인 영향을 받는 개체의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="a3df8-181">`[TargetObjectId <String>]`: 영향을 받는 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="a3df8-182">`[TargetObjectName <String>]`: 영향을 받는 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="a3df8-183">`[Task <IAsrTask[]>]`: 작업.</span><span class="sxs-lookup"><span data-stu-id="a3df8-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="a3df8-184">`[AllowedAction <String[]>]`: 이 작업에 적용할 수 있는 상태/작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="a3df8-185">`[CustomDetailInstanceType <String>]`: 작업 세부 정보의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="a3df8-186">`[EndTime <DateTime?>]`: 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="a3df8-187">`[Error <IJobErrorDetails[]>]`: 작업 오류 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="a3df8-188">`[FriendlyName <String>]`: 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="a3df8-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: 자식 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="a3df8-190">`[GroupTaskCustomDetailInstanceType <String>]`: 작업 세부 정보의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="a3df8-191">`[Name <String>]`: 고유한 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="a3df8-192">`[StartTime <DateTime?>]`: 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="a3df8-193">`[State <String>]`: 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="a3df8-194">NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended 또는 Other 값 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="a3df8-195">`[StateDescription <String>]`: 작업 상태 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="a3df8-196">예를 들어 성공 상태의 경우 설명은 Completed, PartiallySucceeded, CompletedWithInformation 또는 Skipped일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="a3df8-197">`[TaskId <String>]`: ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="a3df8-198">`[TaskType <String>]`: 작업의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="a3df8-199">CustomDetails 속성의 세부 정보는 이 형식에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="a3df8-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="a3df8-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3df8-200">RELATED LINKS</span></span>

