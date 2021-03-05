---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: b87e541266c3ce555c0fc11910c9541914b14738
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009584"
---
# <span data-ttu-id="a41b6-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="a41b6-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="a41b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a41b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a41b6-103">복제 서버에 대한 대상 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="a41b6-104">구문</span><span class="sxs-lookup"><span data-stu-id="a41b6-104">SYNTAX</span></span>

### <span data-ttu-id="a41b6-105">ByIDVMwareCbt(기본값)</span><span class="sxs-lookup"><span data-stu-id="a41b6-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a41b6-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="a41b6-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a41b6-107">설명</span><span class="sxs-lookup"><span data-stu-id="a41b6-107">DESCRIPTION</span></span>
<span data-ttu-id="a41b6-108">Set-AzMigrateServerReplication cmdlet은 복제 서버에 대한 대상 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="a41b6-109">예제</span><span class="sxs-lookup"><span data-stu-id="a41b6-109">EXAMPLES</span></span>

### <span data-ttu-id="a41b6-110">예제 1: ID로 업데이트</span><span class="sxs-lookup"><span data-stu-id="a41b6-110">Example 1: Update by id</span></span>
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

<span data-ttu-id="a41b6-111">ID로.</span><span class="sxs-lookup"><span data-stu-id="a41b6-111">By id.</span></span>

## <span data-ttu-id="a41b6-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a41b6-112">PARAMETERS</span></span>

### <span data-ttu-id="a41b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a41b6-113">-DefaultProfile</span></span>
<span data-ttu-id="a41b6-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a41b6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a41b6-115">-InputObject</span></span>
<span data-ttu-id="a41b6-116">속성을 업데이트해야 하는 복제 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="a41b6-117">서버 개체는 cmdlet을 사용하여 Get-AzMigrateServerReplication 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="a41b6-118">생성을 위해 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a41b6-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a41b6-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="a41b6-119">-NicToUpdate</span></span>
<span data-ttu-id="a41b6-120">만들 Azure VM에 대한 NIC를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="a41b6-121">생성을 위해 NICTOUPDATE 속성에 대한 메모 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a41b6-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a41b6-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a41b6-122">-SubscriptionId</span></span>
<span data-ttu-id="a41b6-123">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-123">The subscription Id.</span></span>

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

### <span data-ttu-id="a41b6-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a41b6-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="a41b6-125">VM 만들기에 사용할 가용성 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="a41b6-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="a41b6-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="a41b6-127">VM 만들기에 사용할 가용성 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="a41b6-128">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a41b6-128">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="a41b6-129">부팅 진단에 사용할 저장소 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-129">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="a41b6-130">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="a41b6-130">-TargetNetworkId</span></span>
<span data-ttu-id="a41b6-131">서버를 마이그레이션해야 하는 대상 Azure 구독 내에서 Virtual Network ID를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-131">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="a41b6-132">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="a41b6-132">-TargetObjectID</span></span>
<span data-ttu-id="a41b6-133">속성을 업데이트해야 하는 답장 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-133">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="a41b6-134">ID는 Get-AzMigrateServerReplication cmdlet을 사용하여 검색해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-134">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="a41b6-135">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="a41b6-135">-TargetResourceGroupID</span></span>
<span data-ttu-id="a41b6-136">서버를 마이그레이션해야 하는 대상 Azure 구독 내에서 리소스 그룹 ID를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-136">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="a41b6-137">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="a41b6-137">-TargetVMName</span></span>
<span data-ttu-id="a41b6-138">속성을 업데이트해야 하는 답장 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-138">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="a41b6-139">ID는 Get-AzMigrateServerReplication cmdlet을 사용하여 검색해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-139">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="a41b6-140">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="a41b6-140">-TargetVMSize</span></span>
<span data-ttu-id="a41b6-141">만들 Azure VM의 SKU를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-141">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="a41b6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a41b6-142">CommonParameters</span></span>
<span data-ttu-id="a41b6-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a41b6-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a41b6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a41b6-145">입력</span><span class="sxs-lookup"><span data-stu-id="a41b6-145">INPUTS</span></span>

## <span data-ttu-id="a41b6-146">출력</span><span class="sxs-lookup"><span data-stu-id="a41b6-146">OUTPUTS</span></span>

### <span data-ttu-id="a41b6-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="a41b6-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="a41b6-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a41b6-148">NOTES</span></span>

<span data-ttu-id="a41b6-149">별칭</span><span class="sxs-lookup"><span data-stu-id="a41b6-149">ALIASES</span></span>

<span data-ttu-id="a41b6-150">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a41b6-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a41b6-151">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a41b6-152">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a41b6-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a41b6-153">INPUTOBJECT : 속성을 업데이트해야 하는 복제 <IMigrationItem> 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-153">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="a41b6-154">서버 개체는 cmdlet을 사용하여 Get-AzMigrateServerReplication 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-154">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="a41b6-155">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="a41b6-155">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="a41b6-156">`[CurrentJobId <String>]`: ARM 실행되는 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-156">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="a41b6-157">`[CurrentJobName <String>]`: 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-157">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="a41b6-158">`[CurrentJobStartTime <DateTime?>]`: 작업의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-158">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="a41b6-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: 마이그레이션 공급자 사용자 지정 설정.</span><span class="sxs-lookup"><span data-stu-id="a41b6-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="a41b6-160">NICTOUPDATE <CbtNicInput[]>: 만들 Azure VM에 대한 NIC를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-160">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="a41b6-161">`IsPrimaryNic <String>`: 기본 NIC인지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-161">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="a41b6-162">`NicId <String>`: NIC ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-162">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="a41b6-163">`[IsSelectedForMigration <String>]`: 이 NIC가 마이그레이션에 선택되어 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-163">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="a41b6-164">`[TargetStaticIPAddress <String>]`: 정적 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-164">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="a41b6-165">`[TargetSubnetName <String>]`: 대상 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a41b6-165">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="a41b6-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a41b6-166">RELATED LINKS</span></span>

