---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226791"
---
# <span data-ttu-id="1b88f-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="1b88f-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="1b88f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b88f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b88f-103">Azure 마이그레이션 작업의 상태를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="1b88f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1b88f-104">SYNTAX</span></span>

### <span data-ttu-id="1b88f-105">ListByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1b88f-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1b88f-106">GetById</span><span class="sxs-lookup"><span data-stu-id="1b88f-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1b88f-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="1b88f-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b88f-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="1b88f-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1b88f-109">ListById</span><span class="sxs-lookup"><span data-stu-id="1b88f-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1b88f-110">설명은</span><span class="sxs-lookup"><span data-stu-id="1b88f-110">DESCRIPTION</span></span>
<span data-ttu-id="1b88f-111">Get-AzMigrateJob cmdlet retrives Azure 마이그레이션 작업의 상태를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="1b88f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="1b88f-112">EXAMPLES</span></span>

### <span data-ttu-id="1b88f-113">예제 1: 작업 Id로 가져오기</span><span class="sxs-lookup"><span data-stu-id="1b88f-113">Example 1: Get By Job Id</span></span>
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

<span data-ttu-id="1b88f-114">Id를 기준으로 작업을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="1b88f-115">예제 2: 리소스 그룹 및 프로젝트별 목록</span><span class="sxs-lookup"><span data-stu-id="1b88f-115">Example 2: List by resource group and project</span></span>
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

<span data-ttu-id="1b88f-116">프로젝트의 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="1b88f-117">예제 3: 리소스 그룹, 프로젝트 및 작업 이름으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="1b88f-117">Example 3: Get by resource group, project and job name</span></span>
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

<span data-ttu-id="1b88f-118">이는 특정 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-118">This gets a specific job.</span></span>

## <span data-ttu-id="1b88f-119">변수</span><span class="sxs-lookup"><span data-stu-id="1b88f-119">PARAMETERS</span></span>

### <span data-ttu-id="1b88f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b88f-120">-DefaultProfile</span></span>
<span data-ttu-id="1b88f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b88f-122">-필터</span><span class="sxs-lookup"><span data-stu-id="1b88f-122">-Filter</span></span>
<span data-ttu-id="1b88f-123">OData 필터 옵션</span><span class="sxs-lookup"><span data-stu-id="1b88f-123">OData filter options.</span></span>

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

### <span data-ttu-id="1b88f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b88f-124">-InputObject</span></span>
<span data-ttu-id="1b88f-125">복제 서버의 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="1b88f-126">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1b88f-127">-JobID</span><span class="sxs-lookup"><span data-stu-id="1b88f-127">-JobID</span></span>
<span data-ttu-id="1b88f-128">세부 정보를 검색 해야 하는 작업 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-128">Specifies the job id for which the details needs to be retrieved.</span></span>

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

### <span data-ttu-id="1b88f-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="1b88f-129">-JobName</span></span>
<span data-ttu-id="1b88f-130">작업 식별자</span><span class="sxs-lookup"><span data-stu-id="1b88f-130">Job identifier</span></span>

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

### <span data-ttu-id="1b88f-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="1b88f-131">-ProjectID</span></span>
<span data-ttu-id="1b88f-132">서버가 복제 되는 Azure 마이그레이션 프로젝트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

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

### <span data-ttu-id="1b88f-133">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="1b88f-133">-ProjectName</span></span>
<span data-ttu-id="1b88f-134">마이그레이션 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-134">The name of the migrate project.</span></span>

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

### <span data-ttu-id="1b88f-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="1b88f-135">-ResourceGroupID</span></span>
<span data-ttu-id="1b88f-136">현재 구독에서 Azure 마이그레이션 프로젝트의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="1b88f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b88f-137">-ResourceGroupName</span></span>
<span data-ttu-id="1b88f-138">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-138">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="1b88f-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b88f-139">-SubscriptionId</span></span>
<span data-ttu-id="1b88f-140">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1b88f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b88f-141">CommonParameters</span></span>
<span data-ttu-id="1b88f-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b88f-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1b88f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b88f-144">입력</span><span class="sxs-lookup"><span data-stu-id="1b88f-144">INPUTS</span></span>

## <span data-ttu-id="1b88f-145">출력</span><span class="sxs-lookup"><span data-stu-id="1b88f-145">OUTPUTS</span></span>

### <span data-ttu-id="1b88f-146">Api20180110 작업을 위한. i a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1b88f-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="1b88f-147">상속자</span><span class="sxs-lookup"><span data-stu-id="1b88f-147">NOTES</span></span>

<span data-ttu-id="1b88f-148">별칭과</span><span class="sxs-lookup"><span data-stu-id="1b88f-148">ALIASES</span></span>

<span data-ttu-id="1b88f-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1b88f-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1b88f-150">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1b88f-151">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="1b88f-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1b88f-152">INPUTOBJECT <IJob> : 복제 서버의 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="1b88f-153">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="1b88f-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="1b88f-154">`[ActivityId <String>]`: 활동 id입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="1b88f-155">`[AllowedAction <String[]>]`: 작업에 허용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="1b88f-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: 원본 서버, 원본 클라우드, 대상 서버, 대상 클라우드 등과 같은 영향을 받는 개체 속성이 워크플로 개체 세부 정보를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="1b88f-157">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="1b88f-158">`[EndTime <DateTime?>]`: 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="1b88f-159">`[Error <IJobErrorDetails[]>]`: 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="1b88f-160">`[CreationTime <DateTime?>]`: 작업 오류를 생성 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="1b88f-161">`[ErrorLevel <String>]`: 오류 수준 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="1b88f-162">`[ProviderErrorDetailErrorCode <Int32?>]`: 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="1b88f-163">`[ProviderErrorDetailErrorId <String>]`: 공급자 오류 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="1b88f-164">`[ProviderErrorDetailErrorMessage <String>]`: 오류 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="1b88f-165">`[ProviderErrorDetailPossibleCaus <String>]`: 오류의 원인이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="1b88f-166">`[ProviderErrorDetailRecommendedAction <String>]`: 오류를 해결 하는 데 권장 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="1b88f-167">`[ServiceErrorDetailActivityId <String>]`: 활동 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="1b88f-168">`[ServiceErrorDetailCode <String>]`: 오류 코드.</span><span class="sxs-lookup"><span data-stu-id="1b88f-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="1b88f-169">`[ServiceErrorDetailMessage <String>]`: 오류 메시지</span><span class="sxs-lookup"><span data-stu-id="1b88f-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="1b88f-170">`[ServiceErrorDetailPossibleCaus <String>]`: 오류가 발생할 수 있는 원인입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="1b88f-171">`[ServiceErrorDetailRecommendedAction <String>]`: 오류를 해결 하는 데 권장 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="1b88f-172">`[TaskId <String>]`: 작업의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="1b88f-173">`[FriendlyName <String>]`: DisplayName입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="1b88f-174">`[ScenarioName <String>]`: ScenarioName.</span><span class="sxs-lookup"><span data-stu-id="1b88f-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="1b88f-175">`[StartTime <DateTime?>]`: 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="1b88f-176">`[State <String>]`: 작업의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="1b88f-177">NotStarted, InProgress, Succeeded, Failed, 취소 됨, 일시 중단 됨 또는 기타 값 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="1b88f-178">`[StateDescription <String>]`: 작업의 상태에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="1b88f-179">예를 들어-성공 상태의 경우 설명은 완료, PartiallySucceeded, CompletedWithInformation 또는 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="1b88f-180">`[TargetInstanceType <String>]`: Microsoft.Azure.SiteRecovery.V2015_11_10 {AffectedObjectType} 클래스인 영향을 받는 개체의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="1b88f-181">`[TargetObjectId <String>]`: 영향을 받는 개체 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="1b88f-182">`[TargetObjectName <String>]`: 영향을 받는 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="1b88f-183">`[Task <IAsrTask[]>]`: 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="1b88f-184">`[AllowedAction <String[]>]`:이 작업에 해당 하는 상태/작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="1b88f-185">`[CustomDetailInstanceType <String>]`: 작업 세부 정보 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="1b88f-186">`[EndTime <DateTime?>]`: 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="1b88f-187">`[Error <IJobErrorDetails[]>]`: 작업 오류 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="1b88f-188">`[FriendlyName <String>]`: 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="1b88f-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: 자식 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="1b88f-190">`[GroupTaskCustomDetailInstanceType <String>]`: 작업 세부 정보 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="1b88f-191">`[Name <String>]`: 고유한 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="1b88f-192">`[StartTime <DateTime?>]`: 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="1b88f-193">`[State <String>]`: 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="1b88f-194">NotStarted, InProgress, Succeeded, Failed, 취소 됨, 일시 중단 됨 또는 기타 값 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="1b88f-195">`[StateDescription <String>]`: 작업 상태에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="1b88f-196">예를 들어 성공 상태의 경우 설명은 완료, PartiallySucceeded, CompletedWithInformation 또는 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="1b88f-197">`[TaskId <String>]`: Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="1b88f-198">`[TaskType <String>]`: 작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="1b88f-199">CustomDetails 속성의 세부 정보는이 형식에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="1b88f-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="1b88f-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b88f-200">RELATED LINKS</span></span>

