---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: 0ef21777f5a7f22fff5d9352f667d8968ff843f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217314"
---
# <span data-ttu-id="1c8ae-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="1c8ae-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="1c8ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="1c8ae-103">지정 된 서버에 대 한 복제를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="1c8ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c8ae-104">SYNTAX</span></span>

### <span data-ttu-id="1c8ae-105">ByIdDefaultUser (기본값)</span><span class="sxs-lookup"><span data-stu-id="1c8ae-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -LicenseType <LicenseType> -MachineId <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1c8ae-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="1c8ae-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <LicenseType>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1c8ae-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="1c8ae-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-DiskEncryptionSetID <String>]
 [-PerformAutoResync <String>] [-SubscriptionId <String>] [-TargetAvailabilitySet <String>]
 [-TargetAvailabilityZone <String>] [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>]
 [-VMWarerunasaccountID <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1c8ae-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="1c8ae-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1c8ae-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1c8ae-109">DESCRIPTION</span></span>
<span data-ttu-id="1c8ae-110">New-AzMigrateServerReplication cmdlet은 Azure 마이그레이션 프로젝트에서 검색 된 특정 서버에 대 한 복제를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="1c8ae-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1c8ae-111">EXAMPLES</span></span>

### <span data-ttu-id="1c8ae-112">예제 1: OS 디스크만 있는 경우</span><span class="sxs-lookup"><span data-stu-id="1c8ae-112">Example 1: When there is only OS disk</span></span>
```powershell
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx4/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskType "Standard_LRS" -OSDiskID "6000C299-343d-7bcd-c05e-a94bd63316dd"

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="1c8ae-113">이는 보호 해야 하는 디스크가 하나만 있는 경우 시나리오에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="1c8ae-114">예제 2: 디스크가 여러 개 있는 경우</span><span class="sxs-lookup"><span data-stu-id="1c8ae-114">Example 2: When there are multiple disks</span></span>
```powershell
PS C:\> $OSDisk = New-AzMigrateDiskMapping -DiskID '6000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'true'
PS C:\> $DataDisk = New-AzMigrateDiskMapping -DiskID '7000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'false'
PS C:\> $DisksToInclude += $OSDisk
PS C:\> $DisksToInclude += $DataDisk
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskToInclude $DisksToInclude -PerformAutoResync true

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="1c8ae-115">보호 해야 하는 디스크가 여러 개 있는 경우 시나리오에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="1c8ae-116">변수</span><span class="sxs-lookup"><span data-stu-id="1c8ae-116">PARAMETERS</span></span>

### <span data-ttu-id="1c8ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c8ae-117">-DefaultProfile</span></span>
<span data-ttu-id="1c8ae-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c8ae-119">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="1c8ae-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="1c8ae-120">사용할 디스크 encyption 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-120">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8ae-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="1c8ae-121">-DiskToInclude</span></span>
<span data-ttu-id="1c8ae-122">복제를 위해 포함할 원본 서버의 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="1c8ae-123">생성 하려면 DISKTOINCLUDE 포함 및 해시 테이블 만들기에 대 한 참고 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput[]
Parameter Sets: ByIdPowerUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8ae-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="1c8ae-124">-DiskType</span></span>
<span data-ttu-id="1c8ae-125">Azure VM에 사용 되는 디스크 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8ae-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c8ae-126">-InputObject</span></span>
<span data-ttu-id="1c8ae-127">마이그레이션할 검색 된 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="1c8ae-128">서버 개체는 Get-AzMigrateServer cmdlet을 사용 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="1c8ae-129">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine
Parameter Sets: ByInputObjectDefaultUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8ae-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1c8ae-130">-LicenseType</span></span>
<span data-ttu-id="1c8ae-131">마이그레이션할 원본 서버에 Azure 하이브리드 혜택을 적용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.LicenseType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8ae-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="1c8ae-132">-MachineId</span></span>
<span data-ttu-id="1c8ae-133">마이그레이션할 검색 된 서버의 컴퓨터 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByIdPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8ae-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="1c8ae-134">-OSDiskID</span></span>
<span data-ttu-id="1c8ae-135">마이그레이션할 원본 서버에 대 한 운영 체제 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8ae-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="1c8ae-136">-PerformAutoResync</span></span>
<span data-ttu-id="1c8ae-137">복제 중인 원본 서버의 변경 내용 추적이 손실 되는 경우를 대비 하 여 복제를 자동으로 복구할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="1c8ae-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c8ae-138">-SubscriptionId</span></span>
<span data-ttu-id="1c8ae-139">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1c8ae-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1c8ae-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="1c8ae-141">Vm 생성에 사용할 가용성 집합을 VM creationSpecifies에 사용할 가용성 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="1c8ae-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="1c8ae-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="1c8ae-143">VM 만들기에 사용할 가용성 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="1c8ae-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c8ae-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="1c8ae-145">부팅 진단에 사용할 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="1c8ae-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="1c8ae-146">-TargetNetworkId</span></span>
<span data-ttu-id="1c8ae-147">서버를 마이그레이션해야 하는 대상 Azure 구독 내의 가상 네트워크 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="1c8ae-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="1c8ae-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="1c8ae-149">서버를 마이그레이션해야 하는 대상 Azure 구독 내의 리소스 그룹 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="1c8ae-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="1c8ae-150">-TargetSubnetName</span></span>
<span data-ttu-id="1c8ae-151">서버를 마이그레이션해야 하는 대상 가상 Netowk 내의 서브넷 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="1c8ae-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="1c8ae-152">-TargetVMName</span></span>
<span data-ttu-id="1c8ae-153">만들려는 Azure VM의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="1c8ae-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="1c8ae-154">-TargetVMSize</span></span>
<span data-ttu-id="1c8ae-155">만들 Azure VM의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="1c8ae-156">-Vm워 Erunasaccountid</span><span class="sxs-lookup"><span data-stu-id="1c8ae-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="1c8ae-157">계정 id.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-157">Account id.</span></span>

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

### <span data-ttu-id="1c8ae-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c8ae-158">CommonParameters</span></span>
<span data-ttu-id="1c8ae-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c8ae-160">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c8ae-161">입력</span><span class="sxs-lookup"><span data-stu-id="1c8ae-161">INPUTS</span></span>

## <span data-ttu-id="1c8ae-162">출력</span><span class="sxs-lookup"><span data-stu-id="1c8ae-162">OUTPUTS</span></span>

### <span data-ttu-id="1c8ae-163">Api20180110 작업을 위한. i a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="1c8ae-164">상속자</span><span class="sxs-lookup"><span data-stu-id="1c8ae-164">NOTES</span></span>

<span data-ttu-id="1c8ae-165">별칭과</span><span class="sxs-lookup"><span data-stu-id="1c8ae-165">ALIASES</span></span>

<span data-ttu-id="1c8ae-166">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1c8ae-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c8ae-167">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c8ae-168">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c8ae-169">DISKTOINCLUDE IVMwareCbtDiskInput [] >: 복제에 포함할 원본 서버의 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="1c8ae-170">`DiskId <String>`: 디스크 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="1c8ae-171">`IsOSDisk <String>`: 디스크가 OS 디스크 인지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="1c8ae-172">`LogStorageAccountId <String>`: 로그 저장소 계정 팔 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="1c8ae-173">`LogStorageAccountSasSecretName <String>`: 로그 저장소 계정의 키 자격 증명 정보 비밀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="1c8ae-174">`[DiskEncryptionSetId <String>]`: Diska 암 번호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="1c8ae-175">`[DiskType <DiskAccountType?>]`: 디스크 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="1c8ae-176">INPUTOBJECT <IVMwareMachine> : 마이그레이션할 검색 된 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="1c8ae-177">서버 개체는 Get-AzMigrateServer cmdlet을 사용 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="1c8ae-178">`[GuestOSDetailOstype <String>]`: 운영 체제의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="1c8ae-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c8ae-179">RELATED LINKS</span></span>

