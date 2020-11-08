---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218623"
---
# <span data-ttu-id="5f754-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="5f754-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="5f754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f754-102">SYNOPSIS</span></span>
<span data-ttu-id="5f754-103">복제 서버에 대 한 마이그레이션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="5f754-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f754-104">SYNTAX</span></span>

### <span data-ttu-id="5f754-105">Byidvmwa, Bt (기본값)</span><span class="sxs-lookup"><span data-stu-id="5f754-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5f754-106">Byinputobjectvmwa, Bt</span><span class="sxs-lookup"><span data-stu-id="5f754-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5f754-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5f754-107">DESCRIPTION</span></span>
<span data-ttu-id="5f754-108">복제 서버에 대 한 마이그레이션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="5f754-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5f754-109">EXAMPLES</span></span>

### <span data-ttu-id="5f754-110">예제 1: id 기준</span><span class="sxs-lookup"><span data-stu-id="5f754-110">Example 1: By id</span></span>
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

<span data-ttu-id="5f754-111">Id 기준</span><span class="sxs-lookup"><span data-stu-id="5f754-111">By id</span></span>

## <span data-ttu-id="5f754-112">변수</span><span class="sxs-lookup"><span data-stu-id="5f754-112">PARAMETERS</span></span>

### <span data-ttu-id="5f754-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f754-113">-DefaultProfile</span></span>
<span data-ttu-id="5f754-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f754-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f754-115">-InputObject</span></span>
<span data-ttu-id="5f754-116">마이그레이션을 시작 해야 하는 복제 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="5f754-117">서버 개체는 Get-AzMigrateServerReplication cmdlet을 사용 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="5f754-118">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5f754-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f754-119">-SubscriptionId</span></span>
<span data-ttu-id="5f754-120">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5f754-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="5f754-121">-TargetObjectID</span></span>
<span data-ttu-id="5f754-122">마이그레이션을 시작 해야 하는 replcating 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="5f754-123">ID는 Get-AzMigrateServerReplication cmdlet을 사용 하 여 검색 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="5f754-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="5f754-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="5f754-125">원본 서버에서 마이그레이션 후 해제 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-125">Specifies whether the source server should be turned off post migration.</span></span>

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

### <span data-ttu-id="5f754-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f754-126">CommonParameters</span></span>
<span data-ttu-id="5f754-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f754-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5f754-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f754-129">입력</span><span class="sxs-lookup"><span data-stu-id="5f754-129">INPUTS</span></span>

## <span data-ttu-id="5f754-130">출력</span><span class="sxs-lookup"><span data-stu-id="5f754-130">OUTPUTS</span></span>

### <span data-ttu-id="5f754-131">Api20180110 작업을 위한. i a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5f754-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="5f754-132">상속자</span><span class="sxs-lookup"><span data-stu-id="5f754-132">NOTES</span></span>

<span data-ttu-id="5f754-133">별칭과</span><span class="sxs-lookup"><span data-stu-id="5f754-133">ALIASES</span></span>

<span data-ttu-id="5f754-134">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5f754-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5f754-135">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f754-136">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="5f754-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5f754-137">INPUTOBJECT <IMigrationItem> : 마이그레이션을 시작 해야 하는 복제 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="5f754-138">서버 개체는 Get-AzMigrateServerReplication cmdlet을 사용 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="5f754-139">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="5f754-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="5f754-140">`[CurrentJobId <String>]`: 실행할 작업의 ARM Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="5f754-141">`[CurrentJobName <String>]`: 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="5f754-142">`[CurrentJobStartTime <DateTime?>]`: 작업의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="5f754-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: 마이그레이션 공급자 사용자 지정 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="5f754-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="5f754-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f754-144">RELATED LINKS</span></span>

