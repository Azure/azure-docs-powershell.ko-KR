---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: cf6b87b8d03855ae79fc0cea62a3bd126f8342a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975728"
---
# <span data-ttu-id="034a9-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="034a9-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="034a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="034a9-102">SYNOPSIS</span></span>
<span data-ttu-id="034a9-103">지정된 서버에 대한 복제를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="034a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="034a9-104">SYNTAX</span></span>

### <span data-ttu-id="034a9-105">ByIdDefaultUser(기본값)</span><span class="sxs-lookup"><span data-stu-id="034a9-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -LicenseType <String> -MachineId <String> -OSDiskID <String>
 -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String> -TargetVMName <String>
 [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="034a9-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="034a9-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <String>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="034a9-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="034a9-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -InputObject <IVMwareMachine> -LicenseType <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="034a9-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="034a9-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="034a9-109">설명</span><span class="sxs-lookup"><span data-stu-id="034a9-109">DESCRIPTION</span></span>
<span data-ttu-id="034a9-110">New-AzMigrateServerReplication cmdlet은 Azure Migrate 프로젝트에서 검색된 특정 서버에 대한 복제를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="034a9-111">예제</span><span class="sxs-lookup"><span data-stu-id="034a9-111">EXAMPLES</span></span>

### <span data-ttu-id="034a9-112">예제 1: OS 디스크만 있는 경우</span><span class="sxs-lookup"><span data-stu-id="034a9-112">Example 1: When there is only OS disk</span></span>
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

<span data-ttu-id="034a9-113">보호해야 하는 단일 디스크가 하나만 있는 시나리오를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="034a9-114">예제 2: 디스크가 여러 개 있는 경우</span><span class="sxs-lookup"><span data-stu-id="034a9-114">Example 2: When there are multiple disks</span></span>
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

<span data-ttu-id="034a9-115">보호해야 하는 디스크가 여러 개 있는 시나리오를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="034a9-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="034a9-116">PARAMETERS</span></span>

### <span data-ttu-id="034a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034a9-117">-DefaultProfile</span></span>
<span data-ttu-id="034a9-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="034a9-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="034a9-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="034a9-120">사용할 디스크 encyption 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-120">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="034a9-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="034a9-121">-DiskToInclude</span></span>
<span data-ttu-id="034a9-122">복제에 포함될 원본 서버의 디스크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="034a9-123">생성을 위해 DISKTOINCLUDE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="034a9-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="034a9-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="034a9-124">-DiskType</span></span>
<span data-ttu-id="034a9-125">Azure VM에 사용할 디스크 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-125">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="034a9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="034a9-126">-InputObject</span></span>
<span data-ttu-id="034a9-127">마이그레이션할 검색된 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="034a9-128">서버 개체는 cmdlet을 사용하여 Get-AzMigrateServer 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="034a9-129">생성을 위해 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="034a9-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="034a9-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="034a9-130">-LicenseType</span></span>
<span data-ttu-id="034a9-131">원본 서버에 마이그레이션할 Azure Hybrid 혜택이 적용 가능한지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

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

### <span data-ttu-id="034a9-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="034a9-132">-MachineId</span></span>
<span data-ttu-id="034a9-133">마이그레이션할 검색된 서버의 컴퓨터 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="034a9-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="034a9-134">-OSDiskID</span></span>
<span data-ttu-id="034a9-135">마이그레이션할 원본 서버에 대한 운영 체제 디스크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

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

### <span data-ttu-id="034a9-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="034a9-136">-PerformAutoResync</span></span>
<span data-ttu-id="034a9-137">복제에서 원본 서버에 대한 변경 내용 추적이 손실될 경우 복제를 자동으로 복구할지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="034a9-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="034a9-138">-SubscriptionId</span></span>
<span data-ttu-id="034a9-139">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="034a9-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="034a9-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="034a9-141">VM 생성에 사용할 가용성 집합을 지정합니다. VM 만들기에 사용할 가용성 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="034a9-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="034a9-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="034a9-143">VM 만들기에 사용할 가용성 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="034a9-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="034a9-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="034a9-145">부팅 진단에 사용할 저장소 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="034a9-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="034a9-146">-TargetNetworkId</span></span>
<span data-ttu-id="034a9-147">서버를 마이그레이션해야 하는 대상 Azure 구독 내의 Virtual Network ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="034a9-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="034a9-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="034a9-149">서버를 마이그레이션해야 하는 대상 Azure 구독 내의 리소스 그룹 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="034a9-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="034a9-150">-TargetSubnetName</span></span>
<span data-ttu-id="034a9-151">서버를 마이그레이션해야 하는 대상 Virtual Netowk 내의 서브넷 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="034a9-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="034a9-152">-TargetVMName</span></span>
<span data-ttu-id="034a9-153">만들 Azure VM의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="034a9-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="034a9-154">-TargetVMSize</span></span>
<span data-ttu-id="034a9-155">만들 Azure VM의 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="034a9-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="034a9-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="034a9-157">계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-157">Account id.</span></span>

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

### <span data-ttu-id="034a9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034a9-158">CommonParameters</span></span>
<span data-ttu-id="034a9-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034a9-160">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="034a9-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034a9-161">입력</span><span class="sxs-lookup"><span data-stu-id="034a9-161">INPUTS</span></span>

## <span data-ttu-id="034a9-162">출력</span><span class="sxs-lookup"><span data-stu-id="034a9-162">OUTPUTS</span></span>

### <span data-ttu-id="034a9-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="034a9-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="034a9-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="034a9-164">NOTES</span></span>

<span data-ttu-id="034a9-165">별칭</span><span class="sxs-lookup"><span data-stu-id="034a9-165">ALIASES</span></span>

<span data-ttu-id="034a9-166">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="034a9-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="034a9-167">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="034a9-168">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="034a9-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="034a9-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: 복제에 포함될 원본 서버의 디스크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="034a9-170">`DiskId <String>`: 디스크 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="034a9-171">`IsOSDisk <String>`: 디스크가 OS 디스크인지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="034a9-172">`LogStorageAccountId <String>`: 로그 저장소 계정은 ARM 합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="034a9-173">`LogStorageAccountSasSecretName <String>`: 로그 저장소 계정의 키 자격 증명 모음 비밀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="034a9-174">`[DiskEncryptionSetId <String>]`: DiskEncryptionSet ARM ID입니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="034a9-175">`[DiskType <DiskAccountType?>]`: 디스크 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="034a9-176">INPUTOBJECT : 마이그레이션할 검색된 서버를 <IVMwareMachine> 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="034a9-177">서버 개체는 cmdlet을 사용하여 Get-AzMigrateServer 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="034a9-178">`[GuestOSDetailOstype <String>]`: 운영 체제의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="034a9-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="034a9-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="034a9-179">RELATED LINKS</span></span>

