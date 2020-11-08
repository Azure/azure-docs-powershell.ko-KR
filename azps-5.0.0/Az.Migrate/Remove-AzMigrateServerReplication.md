---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218627"
---
# <span data-ttu-id="d8263-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="d8263-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="d8263-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8263-102">SYNOPSIS</span></span>
<span data-ttu-id="d8263-103">마이그레이션된 서버에 대 한 복제를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="d8263-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8263-104">SYNTAX</span></span>

### <span data-ttu-id="d8263-105">Byidvmwa, Bt (기본값)</span><span class="sxs-lookup"><span data-stu-id="d8263-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8263-106">Byinputobjectvmwa, Bt</span><span class="sxs-lookup"><span data-stu-id="d8263-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d8263-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d8263-107">DESCRIPTION</span></span>
<span data-ttu-id="d8263-108">Remove-AzMigrateServerReplication cmdlet은 마이그레이션된 서버에 대 한 복제를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="d8263-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d8263-109">EXAMPLES</span></span>

### <span data-ttu-id="d8263-110">예제 1: id를 기준으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-110">Example 1: Remove by id.</span></span>
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

<span data-ttu-id="d8263-111">Id를 기준으로 다시 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-111">Resync by id.</span></span>

### <span data-ttu-id="d8263-112">예제 2: 입력 개체에서 제거</span><span class="sxs-lookup"><span data-stu-id="d8263-112">Example 2: Remove by Input Object</span></span>
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

<span data-ttu-id="d8263-113">이름을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-113">By name.</span></span>

## <span data-ttu-id="d8263-114">변수</span><span class="sxs-lookup"><span data-stu-id="d8263-114">PARAMETERS</span></span>

### <span data-ttu-id="d8263-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8263-115">-DefaultProfile</span></span>
<span data-ttu-id="d8263-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8263-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="d8263-117">-ForceRemove</span></span>
<span data-ttu-id="d8263-118">복제를 강제 제거 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="d8263-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8263-119">-InputObject</span></span>
<span data-ttu-id="d8263-120">복제 서버의 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="d8263-121">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8263-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8263-122">-SubscriptionId</span></span>
<span data-ttu-id="d8263-123">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d8263-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="d8263-124">-TargetObjectID</span></span>
<span data-ttu-id="d8263-125">Replicatio을 사용 하지 않도록 설정 해야 하는 replcating 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="d8263-126">ID는 Get-AzMigrateServerReplication cmdlet을 사용 하 여 검색 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="d8263-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8263-127">CommonParameters</span></span>
<span data-ttu-id="d8263-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8263-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8263-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8263-130">입력</span><span class="sxs-lookup"><span data-stu-id="d8263-130">INPUTS</span></span>

## <span data-ttu-id="d8263-131">출력</span><span class="sxs-lookup"><span data-stu-id="d8263-131">OUTPUTS</span></span>

### <span data-ttu-id="d8263-132">Api20180110 작업을 위한. i a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d8263-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="d8263-133">상속자</span><span class="sxs-lookup"><span data-stu-id="d8263-133">NOTES</span></span>

<span data-ttu-id="d8263-134">별칭과</span><span class="sxs-lookup"><span data-stu-id="d8263-134">ALIASES</span></span>

<span data-ttu-id="d8263-135">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d8263-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8263-136">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8263-137">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8263-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8263-138">INPUTOBJECT <IMigrationItem> : 복제 서버의 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="d8263-139">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="d8263-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="d8263-140">`[CurrentJobId <String>]`: 실행할 작업의 ARM Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="d8263-141">`[CurrentJobName <String>]`: 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="d8263-142">`[CurrentJobStartTime <DateTime?>]`: 작업의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="d8263-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: 마이그레이션 공급자 사용자 지정 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="d8263-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="d8263-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8263-144">RELATED LINKS</span></span>

