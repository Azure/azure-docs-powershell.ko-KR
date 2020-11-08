---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218620"
---
# <span data-ttu-id="4cf76-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="4cf76-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="4cf76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cf76-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf76-103">복제 서버에 대 한 테스트 마이그레이션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="4cf76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cf76-104">SYNTAX</span></span>

### <span data-ttu-id="4cf76-105">Byidvmwa, Bt (기본값)</span><span class="sxs-lookup"><span data-stu-id="4cf76-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4cf76-106">Byinputobjectvmwa, Bt</span><span class="sxs-lookup"><span data-stu-id="4cf76-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4cf76-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4cf76-107">DESCRIPTION</span></span>
<span data-ttu-id="4cf76-108">Start-AzMigrateTestMigration cmdlet은 복제 서버에 대 한 테스트 마이그레이션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="4cf76-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4cf76-109">EXAMPLES</span></span>

### <span data-ttu-id="4cf76-110">예제 1: 컴퓨터 id 기준.</span><span class="sxs-lookup"><span data-stu-id="4cf76-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigration -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f' -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxxresourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="4cf76-111">컴퓨터 id를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-111">By machine id.</span></span>

### <span data-ttu-id="4cf76-112">예제 2: 입력 개체 기준</span><span class="sxs-lookup"><span data-stu-id="4cf76-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigration -InputObject $obj -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="4cf76-113">입력 개체를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-113">By input object.</span></span>

## <span data-ttu-id="4cf76-114">변수</span><span class="sxs-lookup"><span data-stu-id="4cf76-114">PARAMETERS</span></span>

### <span data-ttu-id="4cf76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf76-115">-DefaultProfile</span></span>
<span data-ttu-id="4cf76-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cf76-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cf76-117">-InputObject</span></span>
<span data-ttu-id="4cf76-118">테스트 마이그레이션을 시작 해야 하는 복제 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="4cf76-119">서버 개체는 Get-AzMigrateServerReplication cmdlet을 사용 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="4cf76-120">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4cf76-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4cf76-121">-SubscriptionId</span></span>
<span data-ttu-id="4cf76-122">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="4cf76-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="4cf76-123">-TargetObjectID</span></span>
<span data-ttu-id="4cf76-124">테스트 마이그레이션을 시작 해야 하는 복제 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="4cf76-125">ID는 Get-AzMigrateServerReplication cmdlet을 사용 하 여 검색 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="4cf76-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="4cf76-126">-TestNetworkID</span></span>
<span data-ttu-id="4cf76-127">테스트 마이그레이션에 사용할 대상 Azure 구독 내의 가상 네트워크 id를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf76-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf76-128">CommonParameters</span></span>
<span data-ttu-id="4cf76-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf76-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4cf76-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf76-131">입력</span><span class="sxs-lookup"><span data-stu-id="4cf76-131">INPUTS</span></span>

## <span data-ttu-id="4cf76-132">출력</span><span class="sxs-lookup"><span data-stu-id="4cf76-132">OUTPUTS</span></span>

### <span data-ttu-id="4cf76-133">Api20180110 작업을 위한. i a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4cf76-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="4cf76-134">상속자</span><span class="sxs-lookup"><span data-stu-id="4cf76-134">NOTES</span></span>

<span data-ttu-id="4cf76-135">별칭과</span><span class="sxs-lookup"><span data-stu-id="4cf76-135">ALIASES</span></span>

<span data-ttu-id="4cf76-136">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4cf76-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4cf76-137">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4cf76-138">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="4cf76-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4cf76-139">INPUTOBJECT <IMigrationItem> : 테스트 마이그레이션을 시작 해야 하는 복제 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="4cf76-140">서버 개체는 Get-AzMigrateServerReplication cmdlet을 사용 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="4cf76-141">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="4cf76-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="4cf76-142">`[CurrentJobId <String>]`: 실행할 작업의 ARM Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="4cf76-143">`[CurrentJobName <String>]`: 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="4cf76-144">`[CurrentJobStartTime <DateTime?>]`: 작업의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="4cf76-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: 마이그레이션 공급자 사용자 지정 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf76-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="4cf76-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cf76-146">RELATED LINKS</span></span>

