---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185052"
---
# <span data-ttu-id="7eb5f-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="7eb5f-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="7eb5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eb5f-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb5f-103">복제 서버에 대한 마이그레이션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="7eb5f-104">구문</span><span class="sxs-lookup"><span data-stu-id="7eb5f-104">SYNTAX</span></span>

### <span data-ttu-id="7eb5f-105">ByIDVMwareCbt(기본값)</span><span class="sxs-lookup"><span data-stu-id="7eb5f-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7eb5f-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="7eb5f-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7eb5f-107">설명</span><span class="sxs-lookup"><span data-stu-id="7eb5f-107">DESCRIPTION</span></span>
<span data-ttu-id="7eb5f-108">복제 서버에 대한 마이그레이션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="7eb5f-109">예제</span><span class="sxs-lookup"><span data-stu-id="7eb5f-109">EXAMPLES</span></span>

### <span data-ttu-id="7eb5f-110">예제 1: ID로</span><span class="sxs-lookup"><span data-stu-id="7eb5f-110">Example 1: By id</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Start-AzMigrateServerMigration -TargetObjectID "/Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_52f42ee7-8eb3-1aa4-e2d5-1ae83f86b085"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Migrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="7eb5f-111">ID로</span><span class="sxs-lookup"><span data-stu-id="7eb5f-111">By id</span></span>

## <span data-ttu-id="7eb5f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7eb5f-112">PARAMETERS</span></span>

### <span data-ttu-id="7eb5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb5f-113">-DefaultProfile</span></span>
<span data-ttu-id="7eb5f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eb5f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eb5f-115">-InputObject</span></span>
<span data-ttu-id="7eb5f-116">마이그레이션을 시작해야 하는 복제 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="7eb5f-117">Get-AzMigrateServerReplication cmdlet을 사용하여 서버 개체를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="7eb5f-118">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7eb5f-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7eb5f-119">-SubscriptionId</span></span>
<span data-ttu-id="7eb5f-120">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7eb5f-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="7eb5f-121">-TargetObjectID</span></span>
<span data-ttu-id="7eb5f-122">마이그레이션을 시작해야 하는 응답 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="7eb5f-123">ID는 Get-AzMigrateServerReplication cmdlet을 사용하여 검색해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="7eb5f-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="7eb5f-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="7eb5f-125">마이그레이션 후 원본 서버를 해제해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-125">Specifies whether the source server should be turned off post migration.</span></span>

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

### <span data-ttu-id="7eb5f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb5f-126">CommonParameters</span></span>
<span data-ttu-id="7eb5f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb5f-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb5f-129">입력</span><span class="sxs-lookup"><span data-stu-id="7eb5f-129">INPUTS</span></span>

## <span data-ttu-id="7eb5f-130">출력</span><span class="sxs-lookup"><span data-stu-id="7eb5f-130">OUTPUTS</span></span>

### <span data-ttu-id="7eb5f-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="7eb5f-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="7eb5f-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7eb5f-132">NOTES</span></span>

<span data-ttu-id="7eb5f-133">별칭</span><span class="sxs-lookup"><span data-stu-id="7eb5f-133">ALIASES</span></span>

<span data-ttu-id="7eb5f-134">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7eb5f-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7eb5f-135">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7eb5f-136">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7eb5f-137">INPUTOBJECT: 마이그레이션을 시작해야 하는 복제 <IMigrationItem> 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="7eb5f-138">Get-AzMigrateServerReplication cmdlet을 사용하여 서버 개체를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="7eb5f-139">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="7eb5f-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="7eb5f-140">`[CurrentJobId <String>]`: ARM 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="7eb5f-141">`[CurrentJobName <String>]`: 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="7eb5f-142">`[CurrentJobStartTime <DateTime?>]`: 작업의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="7eb5f-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: 마이그레이션 공급자 사용자 지정 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="7eb5f-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="7eb5f-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7eb5f-144">RELATED LINKS</span></span>

