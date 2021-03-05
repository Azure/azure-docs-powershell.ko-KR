---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: 65f9527005b849b9ffbcc8c343b57515b2d437c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006560"
---
# <span data-ttu-id="41b1e-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="41b1e-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="41b1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="41b1e-103">마이그레이션된 서버에 대한 복제를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="41b1e-104">구문</span><span class="sxs-lookup"><span data-stu-id="41b1e-104">SYNTAX</span></span>

### <span data-ttu-id="41b1e-105">ByIDVMwareCbt(기본값)</span><span class="sxs-lookup"><span data-stu-id="41b1e-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41b1e-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="41b1e-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="41b1e-107">설명</span><span class="sxs-lookup"><span data-stu-id="41b1e-107">DESCRIPTION</span></span>
<span data-ttu-id="41b1e-108">Remove-AzMigrateServerReplication cmdlet은 마이그레이션된 서버에 대한 복제를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="41b1e-109">예제</span><span class="sxs-lookup"><span data-stu-id="41b1e-109">EXAMPLES</span></span>

### <span data-ttu-id="41b1e-110">예제 1: ID로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-110">Example 1: Remove by id.</span></span>
```powershell
PS C:\> Remove-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="41b1e-111">ID로 다시싱크합니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-111">Resync by id.</span></span>

### <span data-ttu-id="41b1e-112">예제 2: 입력 개체로 제거</span><span class="sxs-lookup"><span data-stu-id="41b1e-112">Example 2: Remove by Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> Remove-AzMigrateServerReplication -InputObject $obj


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="41b1e-113">이름에 의해.</span><span class="sxs-lookup"><span data-stu-id="41b1e-113">By name.</span></span>

## <span data-ttu-id="41b1e-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="41b1e-114">PARAMETERS</span></span>

### <span data-ttu-id="41b1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b1e-115">-DefaultProfile</span></span>
<span data-ttu-id="41b1e-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41b1e-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="41b1e-117">-ForceRemove</span></span>
<span data-ttu-id="41b1e-118">복제를 강제로 제거해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="41b1e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41b1e-119">-InputObject</span></span>
<span data-ttu-id="41b1e-120">복제 서버의 컴퓨터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="41b1e-121">생성을 위해 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="41b1e-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b1e-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41b1e-122">-SubscriptionId</span></span>
<span data-ttu-id="41b1e-123">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="41b1e-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="41b1e-124">-TargetObjectID</span></span>
<span data-ttu-id="41b1e-125">복제본을 사용하지 않도록 설정해야 하는 답장 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="41b1e-126">ID는 Get-AzMigrateServerReplication cmdlet을 사용하여 검색해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b1e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b1e-127">CommonParameters</span></span>
<span data-ttu-id="41b1e-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b1e-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41b1e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b1e-130">입력</span><span class="sxs-lookup"><span data-stu-id="41b1e-130">INPUTS</span></span>

## <span data-ttu-id="41b1e-131">출력</span><span class="sxs-lookup"><span data-stu-id="41b1e-131">OUTPUTS</span></span>

### <span data-ttu-id="41b1e-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="41b1e-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="41b1e-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="41b1e-133">NOTES</span></span>

<span data-ttu-id="41b1e-134">별칭</span><span class="sxs-lookup"><span data-stu-id="41b1e-134">ALIASES</span></span>

<span data-ttu-id="41b1e-135">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="41b1e-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41b1e-136">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41b1e-137">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41b1e-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41b1e-138">INPUTOBJECT : 복제 서버의 <IMigrationItem> 컴퓨터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="41b1e-139">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="41b1e-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="41b1e-140">`[CurrentJobId <String>]`: ARM 실행되는 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="41b1e-141">`[CurrentJobName <String>]`: 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="41b1e-142">`[CurrentJobStartTime <DateTime?>]`: 작업의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="41b1e-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="41b1e-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: 마이그레이션 공급자 사용자 지정 설정.</span><span class="sxs-lookup"><span data-stu-id="41b1e-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="41b1e-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41b1e-144">RELATED LINKS</span></span>

