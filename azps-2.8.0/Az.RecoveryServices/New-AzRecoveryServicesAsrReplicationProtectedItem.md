---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: c3c420e29d0aba3f8e64e8b5528b62dddf974984
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873531"
---
# <span data-ttu-id="7003b-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7003b-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="7003b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7003b-102">SYNOPSIS</span></span>
<span data-ttu-id="7003b-103">복제 보호 항목을 만들어 ASR 보호 가능한 항목에 대 한 복제를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="7003b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7003b-104">SYNTAX</span></span>

### <span data-ttu-id="7003b-105">EnterpriseToEnterprise (기본값)</span><span class="sxs-lookup"><span data-stu-id="7003b-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7003b-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="7003b-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7003b-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7003b-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7003b-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="7003b-108">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7003b-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="7003b-109">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7003b-110">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="7003b-110">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> -RecoveryResourceGroupId <String>
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7003b-111">설명은</span><span class="sxs-lookup"><span data-stu-id="7003b-111">DESCRIPTION</span></span>
<span data-ttu-id="7003b-112">**AzRecoveryServicesAsrReplicationProtectedItem** cmdlet은 새 복제 보호 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-112">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="7003b-113">이 cmdlet을 사용 하 여 ASR 보호 가능한 항목에 대 한 복제를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-113">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="7003b-114">예제의</span><span class="sxs-lookup"><span data-stu-id="7003b-114">EXAMPLES</span></span>

### <span data-ttu-id="7003b-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="7003b-115">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="7003b-116">지정 된 ASR 보호 가능한 항목에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-116">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="7003b-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="7003b-117">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="7003b-118">지정 된 ASR 보호 가능한 항목에 대 한 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다 (vmWare에서 Azure 시나리오).</span><span class="sxs-lookup"><span data-stu-id="7003b-118">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="7003b-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="7003b-119">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzToAzure -AzToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="7003b-120">지정 된 ASR 보호 가능한 항목에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업 (Azure to Azure 시나리오)을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-120">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="7003b-121">예제 4</span><span class="sxs-lookup"><span data-stu-id="7003b-121">Example 4</span></span>
```
PS C:\> $disk1 = new-AzToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="7003b-122">지정 된 VmId에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다 (Azure to Azure 시나리오).</span><span class="sxs-lookup"><span data-stu-id="7003b-122">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="7003b-123">변수</span><span class="sxs-lookup"><span data-stu-id="7003b-123">PARAMETERS</span></span>

### <span data-ttu-id="7003b-124">-계정</span><span class="sxs-lookup"><span data-stu-id="7003b-124">-Account</span></span>
<span data-ttu-id="7003b-125">필요한 경우 모바일 서비스를 강제 설치 하는 데 사용할 실행 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-125">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="7003b-126">ASR 패브릭의 실행 계정 목록에서 1 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-126">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-127">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="7003b-127">-AzureToAzure</span></span>
<span data-ttu-id="7003b-128">{{Azureto Fill Toazure 설명}}</span><span class="sxs-lookup"><span data-stu-id="7003b-128">{{Fill AzureToAzure Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-129">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="7003b-129">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="7003b-130">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span><span class="sxs-lookup"><span data-stu-id="7003b-130">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-131">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="7003b-131">-AzureVmId</span></span>
<span data-ttu-id="7003b-132">{{AzureVmId 입력</span><span class="sxs-lookup"><span data-stu-id="7003b-132">{{Fill AzureVmId Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7003b-133">-DefaultProfile</span></span>
<span data-ttu-id="7003b-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="7003b-135">-HyperVToAzure</span></span>
<span data-ttu-id="7003b-136">복제 된 항목을 Azure에 복제 되는 Hyper-v 가상 컴퓨터를 지정 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-136">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-137">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="7003b-137">-IncludeDiskId</span></span>
<span data-ttu-id="7003b-138">복제에 대해 포함할 디스크 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-138">The list of disks to include for replication.</span></span> <span data-ttu-id="7003b-139">기본적으로 모든 디스크가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-139">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-140">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7003b-140">-LogStorageAccountId</span></span>
<span data-ttu-id="7003b-141">복제 로그를 저장 하는 데 사용할 로그 또는 캐시 저장소 계정 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-141">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-142">-이름</span><span class="sxs-lookup"><span data-stu-id="7003b-142">-Name</span></span>
<span data-ttu-id="7003b-143">ASR 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-143">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="7003b-144">이름은 자격 증명 모음 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-144">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="7003b-145">-OS</span><span class="sxs-lookup"><span data-stu-id="7003b-145">-OS</span></span>
<span data-ttu-id="7003b-146">운영 체제 패밀리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-146">Specifies the operating system family.</span></span>
<span data-ttu-id="7003b-147">이 매개 변수에 허용 되는 값은 Windows 또는 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-147">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-148">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="7003b-148">-OSDiskName</span></span>
<span data-ttu-id="7003b-149">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-149">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-150">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="7003b-150">-ProcessServer</span></span>
<span data-ttu-id="7003b-151">이 컴퓨터를 복제 하는 데 사용할 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-151">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="7003b-152">구성 서버에 해당 하는 ASR 패브릭에 있는 프로세스 서버 목록을 사용 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-152">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-153">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7003b-153">-ProtectableItem</span></span>
<span data-ttu-id="7003b-154">복제를 사용할 수 있는 ASR 보호 가능한 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-154">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-155">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7003b-155">-ProtectionContainerMapping</span></span>
<span data-ttu-id="7003b-156">복제에 사용할 복제 정책에 해당 하는 ASR 보호 컨테이너 매핑 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-156">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-157">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="7003b-157">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="7003b-158">장애 조치 시 컴퓨터를 복구할 AvailabilitySet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-158">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-159">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="7003b-159">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="7003b-160">장애 조치 시 컴퓨터를 복구할 Azure 가상 네트워크의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-160">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-161">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7003b-161">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="7003b-162">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-162">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-163">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="7003b-163">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="7003b-164">장애 조치 시 가상 머신이 실패 한 경우 복구 Azure 가상 네트워크 내의 서브넷이 연결 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-164">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-165">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7003b-165">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="7003b-166">복구 azure VM에 대 한 부팅 진단의 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-166">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-167">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="7003b-167">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="7003b-168">이 가상 컴퓨터를 장애 조치 (failover) 할 복구 클라우드 서비스의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-168">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-169">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="7003b-169">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="7003b-170">장애 조치 시 가상 컴퓨터가 생성 될 리소스 그룹의 ARM 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-170">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-171">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="7003b-171">-RecoveryVmName</span></span>
<span data-ttu-id="7003b-172">장애 조치 이후 만든 복구 Vm의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-172">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-173">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="7003b-173">-ReplicationGroupName</span></span>
<span data-ttu-id="7003b-174">여러 VM에서 일관 된 복구 지점을 만드는 데 사용할 복제 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-174">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="7003b-175">기본적으로 각 복제 보호 항목은 자체 그룹에서 만들어지고, 다중 VM 일관성 복구 지점은 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-175">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="7003b-176">모든 컴퓨터를 동일한 복제 그룹으로 보호 하 여 여러 컴퓨터에 걸친 VM의 일관 된 복구 지점을 만들어야 하는 경우에만이 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-176">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="7003b-177">-VmmToVmm</span></span>
<span data-ttu-id="7003b-178">복제 된 항목을 지정 하는 스위치 매개 변수는 VMM 관리 Hyper-v 사이트 간에 복제 되는 Hyper-v 가상 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-178">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-179">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="7003b-179">-VMwareToAzure</span></span>
<span data-ttu-id="7003b-180">복제 된 항목을 지정 하는 스위치 매개 변수는 Azure에 복제 되는 VMware 가상 머신 또는 물리적 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-180">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-181">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7003b-181">-WaitForCompletion</span></span>
<span data-ttu-id="7003b-182">반환 하기 전에 cmdlet에서 작업이 완료 될 때까지 기다리도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-182">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="7003b-183">-확인</span><span class="sxs-lookup"><span data-stu-id="7003b-183">-Confirm</span></span>
<span data-ttu-id="7003b-184">작업을 시작 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-184">Prompts  for confirmation before starting the operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7003b-185">-WhatIf</span></span>
<span data-ttu-id="7003b-186">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7003b-187">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-187">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7003b-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7003b-188">CommonParameters</span></span>
<span data-ttu-id="7003b-189">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003b-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7003b-190">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7003b-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7003b-191">입력</span><span class="sxs-lookup"><span data-stu-id="7003b-191">INPUTS</span></span>

### <span data-ttu-id="7003b-192">SiteRecovery. ASRProtectableItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="7003b-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="7003b-193">출력</span><span class="sxs-lookup"><span data-stu-id="7003b-193">OUTPUTS</span></span>

### <span data-ttu-id="7003b-194">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="7003b-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7003b-195">상속자</span><span class="sxs-lookup"><span data-stu-id="7003b-195">NOTES</span></span>

## <span data-ttu-id="7003b-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7003b-196">RELATED LINKS</span></span>

[<span data-ttu-id="7003b-197">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7003b-197">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7003b-198">제거-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7003b-198">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7003b-199">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7003b-199">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
