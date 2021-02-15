---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateServerReplication.md
ms.openlocfilehash: 2ba6f3252dc3ac1a16609c3d4a82f0bf76ce8a48
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203611"
---
# <span data-ttu-id="913fe-101">Get-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="913fe-101">Get-AzMigrateServerReplication</span></span>

## <span data-ttu-id="913fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="913fe-102">SYNOPSIS</span></span>
<span data-ttu-id="913fe-103">복제 서버의 세부 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-103">Retrieves the details of the replicating server.</span></span>

## <span data-ttu-id="913fe-104">구문</span><span class="sxs-lookup"><span data-stu-id="913fe-104">SYNTAX</span></span>

### <span data-ttu-id="913fe-105">ListByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="913fe-105">ListByName (Default)</span></span>
```
Get-AzMigrateServerReplication -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-SkipToken <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="913fe-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="913fe-106">GetByInputObject</span></span>
```
Get-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="913fe-107">GetByMachineName</span><span class="sxs-lookup"><span data-stu-id="913fe-107">GetByMachineName</span></span>
```
Get-AzMigrateServerReplication -MachineName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="913fe-108">GetBySDSID</span><span class="sxs-lookup"><span data-stu-id="913fe-108">GetBySDSID</span></span>
```
Get-AzMigrateServerReplication -DiscoveredMachineId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="913fe-109">GetBySRSID</span><span class="sxs-lookup"><span data-stu-id="913fe-109">GetBySRSID</span></span>
```
Get-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="913fe-110">ListById</span><span class="sxs-lookup"><span data-stu-id="913fe-110">ListById</span></span>
```
Get-AzMigrateServerReplication -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>]
 [-Filter <String>] [-SkipToken <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="913fe-111">설명</span><span class="sxs-lookup"><span data-stu-id="913fe-111">DESCRIPTION</span></span>
<span data-ttu-id="913fe-112">Get-AzMigrateServerReplication cmdlet은 복제 서버에 대한 개체를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-112">The Get-AzMigrateServerReplication cmdlet retrieves the object for the replicating server.</span></span>

## <span data-ttu-id="913fe-113">예제</span><span class="sxs-lookup"><span data-stu-id="913fe-113">EXAMPLES</span></span>

### <span data-ttu-id="913fe-114">예제 1: ID로 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="913fe-114">Example 1: Get details by id</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="913fe-115">ID로 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-115">Get by id.</span></span>

### <span data-ttu-id="913fe-116">예제 2: ID를 통해 프로젝트의 모든 항목 나열</span><span class="sxs-lookup"><span data-stu-id="913fe-116">Example 2: List all in project by id.</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -ResourceGroupID /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020 -ProjectID "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Migrate/MigrateProjects/AzMigrateTestProjectPWSH"

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : 57b59212-6a2f-4333-8882-461647bb05f9
Health                      : Normal
HealthError                 : {593b735d-2a34-53b2-b8ed-e33da5650703}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : rb-w2k12r2-1
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="913fe-117">모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-117">List all.</span></span>

### <span data-ttu-id="913fe-118">예제 2: 프로젝트의 이름을 모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-118">Example 2: List all in project by name.</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -ResourceGroupName azmigratepwshtestasr13072020 -ProjectName AzMigrateTestProjectPWSH

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : 57b59212-6a2f-4333-8882-461647bb05f9
Health                      : Normal
HealthError                 : {593b735d-2a34-53b2-b8ed-e33da5650703}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : rb-w2k12r2-1
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="913fe-119">모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-119">List all.</span></span>

## <span data-ttu-id="913fe-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="913fe-120">PARAMETERS</span></span>

### <span data-ttu-id="913fe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913fe-121">-DefaultProfile</span></span>
<span data-ttu-id="913fe-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="913fe-123">-DiscoveredMachineId</span><span class="sxs-lookup"><span data-stu-id="913fe-123">-DiscoveredMachineId</span></span>
<span data-ttu-id="913fe-124">검색된 서버의 컴퓨터 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-124">Specifies the machine ID of the discovered server.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySDSID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913fe-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="913fe-125">-Filter</span></span>
<span data-ttu-id="913fe-126">OData 필터 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-126">OData filter options.</span></span>

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

### <span data-ttu-id="913fe-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="913fe-127">-InputObject</span></span>
<span data-ttu-id="913fe-128">복제 서버의 컴퓨터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-128">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="913fe-129">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="913fe-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913fe-130">-MachineName</span><span class="sxs-lookup"><span data-stu-id="913fe-130">-MachineName</span></span>
<span data-ttu-id="913fe-131">복제 컴퓨터의 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-131">Specifies the display name of the replicating machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByMachineName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913fe-132">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="913fe-132">-ProjectID</span></span>
<span data-ttu-id="913fe-133">서버가 복제되는 Azure Migrate 프로젝트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-133">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

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

### <span data-ttu-id="913fe-134">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="913fe-134">-ProjectName</span></span>
<span data-ttu-id="913fe-135">현재 구독에서 Azure Migrate 프로젝트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-135">Specifies the Azure Migrate project  in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByMachineName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913fe-136">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="913fe-136">-ResourceGroupID</span></span>
<span data-ttu-id="913fe-137">현재 구독에서 Azure Migrate 프로젝트의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-137">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="913fe-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913fe-138">-ResourceGroupName</span></span>
<span data-ttu-id="913fe-139">현재 구독에서 Azure Migrate 프로젝트의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-139">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByMachineName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913fe-140">-SkipToken</span><span class="sxs-lookup"><span data-stu-id="913fe-140">-SkipToken</span></span>
<span data-ttu-id="913fe-141">Pagination 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-141">The pagination token.</span></span>

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

### <span data-ttu-id="913fe-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="913fe-142">-SubscriptionId</span></span>
<span data-ttu-id="913fe-143">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-143">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="913fe-144">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="913fe-144">-TargetObjectID</span></span>
<span data-ttu-id="913fe-145">복제 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-145">Specifies the replicating server.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySRSID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913fe-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913fe-146">CommonParameters</span></span>
<span data-ttu-id="913fe-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913fe-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="913fe-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913fe-149">입력</span><span class="sxs-lookup"><span data-stu-id="913fe-149">INPUTS</span></span>

## <span data-ttu-id="913fe-150">출력</span><span class="sxs-lookup"><span data-stu-id="913fe-150">OUTPUTS</span></span>

### <span data-ttu-id="913fe-151">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem</span><span class="sxs-lookup"><span data-stu-id="913fe-151">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem</span></span>

## <span data-ttu-id="913fe-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="913fe-152">NOTES</span></span>

<span data-ttu-id="913fe-153">별칭</span><span class="sxs-lookup"><span data-stu-id="913fe-153">ALIASES</span></span>

<span data-ttu-id="913fe-154">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="913fe-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="913fe-155">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="913fe-156">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="913fe-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="913fe-157">INPUTOBJECT: <IMigrationItem> 복제 서버의 컴퓨터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-157">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="913fe-158">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="913fe-158">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="913fe-159">`[CurrentJobId <String>]`: ARM 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-159">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="913fe-160">`[CurrentJobName <String>]`: 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-160">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="913fe-161">`[CurrentJobStartTime <DateTime?>]`: 작업의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-161">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="913fe-162">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: 마이그레이션 공급자 사용자 지정 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="913fe-162">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="913fe-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="913fe-163">RELATED LINKS</span></span>

