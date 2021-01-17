---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490120"
---
# <span data-ttu-id="b334f-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="b334f-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="b334f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b334f-102">SYNOPSIS</span></span>
<span data-ttu-id="b334f-103">지정된 서버에 대한 복제를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="b334f-104">구문</span><span class="sxs-lookup"><span data-stu-id="b334f-104">SYNTAX</span></span>

### <span data-ttu-id="b334f-105">ByIDVMwareCbt(기본값)</span><span class="sxs-lookup"><span data-stu-id="b334f-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b334f-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="b334f-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b334f-107">설명</span><span class="sxs-lookup"><span data-stu-id="b334f-107">DESCRIPTION</span></span>
<span data-ttu-id="b334f-108">이 Restart-AzMigrateServerReplication cmdlet은 지정된 서버에 대한 복제를 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="b334f-109">예제</span><span class="sxs-lookup"><span data-stu-id="b334f-109">EXAMPLES</span></span>

### <span data-ttu-id="b334f-110">예제 1: ID로</span><span class="sxs-lookup"><span data-stu-id="b334f-110">Example 1: By id.</span></span>
```powershell
PS C:\> Restart-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="b334f-111">ID로</span><span class="sxs-lookup"><span data-stu-id="b334f-111">By id.</span></span>

### <span data-ttu-id="b334f-112">예제 2: 입력 개체로</span><span class="sxs-lookup"><span data-stu-id="b334f-112">Example 2: By Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> $output = Restart-AzMigrateServerReplication -InputObject $obj
ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="b334f-113">입력 개체로.</span><span class="sxs-lookup"><span data-stu-id="b334f-113">By Input Object.</span></span>

## <span data-ttu-id="b334f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b334f-114">PARAMETERS</span></span>

### <span data-ttu-id="b334f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b334f-115">-DefaultProfile</span></span>
<span data-ttu-id="b334f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b334f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b334f-117">-InputObject</span></span>
<span data-ttu-id="b334f-118">복제 서버의 컴퓨터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="b334f-119">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b334f-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b334f-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b334f-120">-SubscriptionId</span></span>
<span data-ttu-id="b334f-121">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b334f-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="b334f-122">-TargetObjectID</span></span>
<span data-ttu-id="b334f-123">재동기를 시작해야 하는 응답 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="b334f-124">ID는 Get-AzMigrateServerReplication cmdlet을 사용하여 검색해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="b334f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b334f-125">CommonParameters</span></span>
<span data-ttu-id="b334f-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b334f-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b334f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b334f-128">입력</span><span class="sxs-lookup"><span data-stu-id="b334f-128">INPUTS</span></span>

## <span data-ttu-id="b334f-129">출력</span><span class="sxs-lookup"><span data-stu-id="b334f-129">OUTPUTS</span></span>

### <span data-ttu-id="b334f-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="b334f-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="b334f-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b334f-131">NOTES</span></span>

<span data-ttu-id="b334f-132">별칭</span><span class="sxs-lookup"><span data-stu-id="b334f-132">ALIASES</span></span>

<span data-ttu-id="b334f-133">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b334f-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b334f-134">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b334f-135">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b334f-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b334f-136">INPUTOBJECT: <IMigrationItem> 복제 서버의 컴퓨터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="b334f-137">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="b334f-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="b334f-138">`[CurrentJobId <String>]`: ARM 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="b334f-139">`[CurrentJobName <String>]`: 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="b334f-140">`[CurrentJobStartTime <DateTime?>]`: 작업의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="b334f-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: 마이그레이션 공급자 사용자 지정 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="b334f-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="b334f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b334f-142">RELATED LINKS</span></span>

