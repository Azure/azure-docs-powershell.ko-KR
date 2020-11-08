---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218621"
---
# <span data-ttu-id="54f04-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="54f04-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="54f04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54f04-102">SYNOPSIS</span></span>
<span data-ttu-id="54f04-103">복제 서버의 대상 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="54f04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54f04-104">SYNTAX</span></span>

### <span data-ttu-id="54f04-105">Byidvmwa, Bt (기본값)</span><span class="sxs-lookup"><span data-stu-id="54f04-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="54f04-106">Byinputobjectvmwa, Bt</span><span class="sxs-lookup"><span data-stu-id="54f04-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="54f04-107">설명은</span><span class="sxs-lookup"><span data-stu-id="54f04-107">DESCRIPTION</span></span>
<span data-ttu-id="54f04-108">Set-AzMigrateServerReplication cmdlet은 복제 서버의 대상 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="54f04-109">예제의</span><span class="sxs-lookup"><span data-stu-id="54f04-109">EXAMPLES</span></span>

### <span data-ttu-id="54f04-110">예제 1: id 별 업데이트</span><span class="sxs-lookup"><span data-stu-id="54f04-110">Example 1: Update by id</span></span>
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

<span data-ttu-id="54f04-111">Id를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-111">By id.</span></span>

## <span data-ttu-id="54f04-112">변수</span><span class="sxs-lookup"><span data-stu-id="54f04-112">PARAMETERS</span></span>

### <span data-ttu-id="54f04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f04-113">-DefaultProfile</span></span>
<span data-ttu-id="54f04-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54f04-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54f04-115">-InputObject</span></span>
<span data-ttu-id="54f04-116">속성을 업데이트 해야 하는 복제 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="54f04-117">서버 개체는 Get-AzMigrateServerReplication cmdlet을 사용 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="54f04-118">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="54f04-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="54f04-119">-NicToUpdate</span></span>
<span data-ttu-id="54f04-120">만들 Azure VM에 대 한 NIC를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="54f04-121">생성 하려면 NICTOUPDATE 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="54f04-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54f04-122">-SubscriptionId</span></span>
<span data-ttu-id="54f04-123">구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-123">The subscription Id.</span></span>

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

### <span data-ttu-id="54f04-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="54f04-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="54f04-125">VM 만들기에 사용할 가용성 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="54f04-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="54f04-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="54f04-127">VM 만들기에 사용할 가용성 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="54f04-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="54f04-128">-TargetNetworkId</span></span>
<span data-ttu-id="54f04-129">서버를 마이그레이션해야 하는 대상 Azure 구독 내의 가상 네트워크 id를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="54f04-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="54f04-130">-TargetObjectID</span></span>
<span data-ttu-id="54f04-131">속성을 업데이트 해야 하는 replcating 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="54f04-132">ID는 Get-AzMigrateServerReplication cmdlet을 사용 하 여 검색 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="54f04-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="54f04-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="54f04-134">서버를 마이그레이션해야 하는 대상 Azure 구독 내의 리소스 그룹 id를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="54f04-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="54f04-135">-TargetVMName</span></span>
<span data-ttu-id="54f04-136">속성을 업데이트 해야 하는 replcating 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="54f04-137">ID는 Get-AzMigrateServerReplication cmdlet을 사용 하 여 검색 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="54f04-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="54f04-138">-TargetVMSize</span></span>
<span data-ttu-id="54f04-139">만들 Azure VM의 SKU를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="54f04-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f04-140">CommonParameters</span></span>
<span data-ttu-id="54f04-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f04-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="54f04-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f04-143">입력</span><span class="sxs-lookup"><span data-stu-id="54f04-143">INPUTS</span></span>

## <span data-ttu-id="54f04-144">출력</span><span class="sxs-lookup"><span data-stu-id="54f04-144">OUTPUTS</span></span>

### <span data-ttu-id="54f04-145">Api20180110 작업을 위한. i a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="54f04-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="54f04-146">상속자</span><span class="sxs-lookup"><span data-stu-id="54f04-146">NOTES</span></span>

<span data-ttu-id="54f04-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="54f04-147">ALIASES</span></span>

<span data-ttu-id="54f04-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="54f04-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="54f04-149">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54f04-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="54f04-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="54f04-151">INPUTOBJECT <IMigrationItem> : 속성을 업데이트 해야 하는 복제 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="54f04-152">서버 개체는 Get-AzMigrateServerReplication cmdlet을 사용 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="54f04-153">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="54f04-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="54f04-154">`[CurrentJobId <String>]`: 실행할 작업의 ARM Id입니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="54f04-155">`[CurrentJobName <String>]`: 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="54f04-156">`[CurrentJobStartTime <DateTime?>]`: 작업의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="54f04-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: 마이그레이션 공급자 사용자 지정 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="54f04-158">NICTOUPDATE <IVMwareCbtNicInput [] >: 만들려는 Azure VM에 대 한 NIC를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="54f04-159">`IsPrimaryNic <String>`: 기본 NIC 인지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="54f04-160">`NicId <String>`: NIC Id입니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="54f04-161">`[IsSelectedForMigration <String>]`:이 NIC가 마이그레이션에 선택 되었는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="54f04-162">`[TargetStaticIPAddress <String>]`: 고정 IP 주소</span><span class="sxs-lookup"><span data-stu-id="54f04-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="54f04-163">`[TargetSubnetName <String>]`: 대상 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54f04-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="54f04-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54f04-164">RELATED LINKS</span></span>

