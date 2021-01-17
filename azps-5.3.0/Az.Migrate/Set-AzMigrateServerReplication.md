---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490119"
---
# <span data-ttu-id="91009-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="91009-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="91009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91009-102">SYNOPSIS</span></span>
<span data-ttu-id="91009-103">복제 서버에 대한 대상 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="91009-104">구문</span><span class="sxs-lookup"><span data-stu-id="91009-104">SYNTAX</span></span>

### <span data-ttu-id="91009-105">ByIDVMwareCbt(기본값)</span><span class="sxs-lookup"><span data-stu-id="91009-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91009-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="91009-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="91009-107">설명</span><span class="sxs-lookup"><span data-stu-id="91009-107">DESCRIPTION</span></span>
<span data-ttu-id="91009-108">Set-AzMigrateServerReplication cmdlet은 복제 서버에 대한 대상 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="91009-109">예제</span><span class="sxs-lookup"><span data-stu-id="91009-109">EXAMPLES</span></span>

### <span data-ttu-id="91009-110">예제 1: ID로 업데이트</span><span class="sxs-lookup"><span data-stu-id="91009-110">Example 1: Update by id</span></span>
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="91009-111">ID로</span><span class="sxs-lookup"><span data-stu-id="91009-111">By id.</span></span>

## <span data-ttu-id="91009-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91009-112">PARAMETERS</span></span>

### <span data-ttu-id="91009-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91009-113">-DefaultProfile</span></span>
<span data-ttu-id="91009-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91009-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91009-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91009-115">-InputObject</span></span>
<span data-ttu-id="91009-116">속성을 업데이트해야 하는 복제 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="91009-117">Get-AzMigrateServerReplication cmdlet을 사용하여 서버 개체를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91009-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="91009-118">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="91009-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="91009-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="91009-119">-NicToUpdate</span></span>
<span data-ttu-id="91009-120">만들 Azure VM에 대한 NIC를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="91009-121">생성을 위해 NICTOUPDATE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="91009-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91009-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91009-122">-SubscriptionId</span></span>
<span data-ttu-id="91009-123">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="91009-123">The subscription Id.</span></span>

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

### <span data-ttu-id="91009-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="91009-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="91009-125">VM 생성에 사용할 가용성 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="91009-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="91009-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="91009-127">VM 생성에 사용할 가용성 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="91009-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="91009-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="91009-128">-TargetNetworkId</span></span>
<span data-ttu-id="91009-129">서버를 마이그레이션해야 하는 대상 Azure 구독 내의 Virtual Network ID를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="91009-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="91009-130">-TargetObjectID</span></span>
<span data-ttu-id="91009-131">속성을 업데이트해야 하는 응답 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="91009-132">ID는 Get-AzMigrateServerReplication cmdlet을 사용하여 검색해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="91009-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="91009-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="91009-134">서버를 마이그레이션해야 하는 대상 Azure 구독 내의 리소스 그룹 ID를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="91009-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="91009-135">-TargetVMName</span></span>
<span data-ttu-id="91009-136">속성을 업데이트해야 하는 응답 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="91009-137">ID는 Get-AzMigrateServerReplication cmdlet을 사용하여 검색해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="91009-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="91009-138">-TargetVMSize</span></span>
<span data-ttu-id="91009-139">만들 Azure VM의 SKU를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="91009-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91009-140">CommonParameters</span></span>
<span data-ttu-id="91009-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91009-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91009-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91009-143">입력</span><span class="sxs-lookup"><span data-stu-id="91009-143">INPUTS</span></span>

## <span data-ttu-id="91009-144">출력</span><span class="sxs-lookup"><span data-stu-id="91009-144">OUTPUTS</span></span>

### <span data-ttu-id="91009-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="91009-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="91009-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91009-146">NOTES</span></span>

<span data-ttu-id="91009-147">별칭</span><span class="sxs-lookup"><span data-stu-id="91009-147">ALIASES</span></span>

<span data-ttu-id="91009-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="91009-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91009-149">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91009-150">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="91009-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91009-151">INPUTOBJECT: 속성을 업데이트해야 하는 복제 <IMigrationItem> 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="91009-152">Get-AzMigrateServerReplication cmdlet을 사용하여 서버 개체를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91009-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="91009-153">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="91009-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="91009-154">`[CurrentJobId <String>]`: ARM 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="91009-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="91009-155">`[CurrentJobName <String>]`: 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91009-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="91009-156">`[CurrentJobStartTime <DateTime?>]`: 작업의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="91009-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="91009-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: 마이그레이션 공급자 사용자 지정 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="91009-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="91009-158">NICTOUPDATE <IVMwareCbtNicInput[]>: 만들 Azure VM에 대한 NIC를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91009-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="91009-159">`IsPrimaryNic <String>`: 기본 NIC인지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="91009-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="91009-160">`NicId <String>`: NIC ID입니다.</span><span class="sxs-lookup"><span data-stu-id="91009-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="91009-161">`[IsSelectedForMigration <String>]`: 이 NIC가 마이그레이션에 선택되어 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="91009-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="91009-162">`[TargetStaticIPAddress <String>]`: 고정 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="91009-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="91009-163">`[TargetSubnetName <String>]`: 대상 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91009-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="91009-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91009-164">RELATED LINKS</span></span>

