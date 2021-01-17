---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490116"
---
# <span data-ttu-id="d00e4-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="d00e4-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="d00e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d00e4-102">SYNOPSIS</span></span>
<span data-ttu-id="d00e4-103">마이그레이션된 서버에 대한 복제를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="d00e4-104">구문</span><span class="sxs-lookup"><span data-stu-id="d00e4-104">SYNTAX</span></span>

### <span data-ttu-id="d00e4-105">ByIDVMwareCbt(기본값)</span><span class="sxs-lookup"><span data-stu-id="d00e4-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d00e4-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="d00e4-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d00e4-107">설명</span><span class="sxs-lookup"><span data-stu-id="d00e4-107">DESCRIPTION</span></span>
<span data-ttu-id="d00e4-108">Remove-AzMigrateServerReplication cmdlet은 마이그레이션된 서버에 대한 복제를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="d00e4-109">예제</span><span class="sxs-lookup"><span data-stu-id="d00e4-109">EXAMPLES</span></span>

### <span data-ttu-id="d00e4-110">예제 1: ID로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-110">Example 1: Remove by id.</span></span>
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

<span data-ttu-id="d00e4-111">ID로 다시동기.</span><span class="sxs-lookup"><span data-stu-id="d00e4-111">Resync by id.</span></span>

### <span data-ttu-id="d00e4-112">예제 2: 입력 개체로 제거</span><span class="sxs-lookup"><span data-stu-id="d00e4-112">Example 2: Remove by Input Object</span></span>
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

<span data-ttu-id="d00e4-113">이름에 의해.</span><span class="sxs-lookup"><span data-stu-id="d00e4-113">By name.</span></span>

## <span data-ttu-id="d00e4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d00e4-114">PARAMETERS</span></span>

### <span data-ttu-id="d00e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d00e4-115">-DefaultProfile</span></span>
<span data-ttu-id="d00e4-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d00e4-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="d00e4-117">-ForceRemove</span></span>
<span data-ttu-id="d00e4-118">복제를 강제로 제거해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="d00e4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d00e4-119">-InputObject</span></span>
<span data-ttu-id="d00e4-120">복제 서버의 컴퓨터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="d00e4-121">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d00e4-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d00e4-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d00e4-122">-SubscriptionId</span></span>
<span data-ttu-id="d00e4-123">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d00e4-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="d00e4-124">-TargetObjectID</span></span>
<span data-ttu-id="d00e4-125">복제본을 사용하지 않도록 설정해야 하는 응답 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="d00e4-126">ID는 Get-AzMigrateServerReplication cmdlet을 사용하여 검색해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="d00e4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d00e4-127">CommonParameters</span></span>
<span data-ttu-id="d00e4-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d00e4-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d00e4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d00e4-130">입력</span><span class="sxs-lookup"><span data-stu-id="d00e4-130">INPUTS</span></span>

## <span data-ttu-id="d00e4-131">출력</span><span class="sxs-lookup"><span data-stu-id="d00e4-131">OUTPUTS</span></span>

### <span data-ttu-id="d00e4-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="d00e4-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="d00e4-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d00e4-133">NOTES</span></span>

<span data-ttu-id="d00e4-134">별칭</span><span class="sxs-lookup"><span data-stu-id="d00e4-134">ALIASES</span></span>

<span data-ttu-id="d00e4-135">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d00e4-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d00e4-136">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d00e4-137">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d00e4-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d00e4-138">INPUTOBJECT: <IMigrationItem> 복제 서버의 컴퓨터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="d00e4-139">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="d00e4-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="d00e4-140">`[CurrentJobId <String>]`: ARM 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="d00e4-141">`[CurrentJobName <String>]`: 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="d00e4-142">`[CurrentJobStartTime <DateTime?>]`: 작업의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="d00e4-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: 마이그레이션 공급자 사용자 지정 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="d00e4-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="d00e4-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d00e4-144">RELATED LINKS</span></span>

