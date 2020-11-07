---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fab7fa9f02f70b5afa1c4c5ffcbd07a8e1706998
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703561"
---
# <span data-ttu-id="7e097-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7e097-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="7e097-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e097-102">SYNOPSIS</span></span>
<span data-ttu-id="7e097-103">복제 보호 항목을 만들어 ASR 보호 가능한 항목에 대 한 복제를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e097-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e097-104">SYNTAX</span></span>

### <span data-ttu-id="7e097-105">EnterpriseToEnterprise (기본값)</span><span class="sxs-lookup"><span data-stu-id="7e097-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e097-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="7e097-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e097-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7e097-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e097-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="7e097-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e097-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="7e097-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e097-110">설명은</span><span class="sxs-lookup"><span data-stu-id="7e097-110">DESCRIPTION</span></span>
<span data-ttu-id="7e097-111">**AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet은 새 복제 보호 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-111">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="7e097-112">이 cmdlet을 사용 하 여 ASR 보호 가능한 항목에 대 한 복제를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-112">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="7e097-113">예제의</span><span class="sxs-lookup"><span data-stu-id="7e097-113">EXAMPLES</span></span>

### <span data-ttu-id="7e097-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e097-114">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="7e097-115">지정 된 ASR 보호 가능한 항목에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-115">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="7e097-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="7e097-116">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="7e097-117">지정 된 ASR 보호 가능한 항목에 대 한 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다 (vmWare에서 Azure 시나리오).</span><span class="sxs-lookup"><span data-stu-id="7e097-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="7e097-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="7e097-118">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="7e097-119">지정 된 ASR 보호 가능한 항목에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업 (Azure to Azure 시나리오)을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="7e097-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="7e097-120">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="7e097-121">지정 된 VmId에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다 (Azure to Azure 시나리오).</span><span class="sxs-lookup"><span data-stu-id="7e097-121">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="7e097-122">변수</span><span class="sxs-lookup"><span data-stu-id="7e097-122">PARAMETERS</span></span>

### <span data-ttu-id="7e097-123">-계정</span><span class="sxs-lookup"><span data-stu-id="7e097-123">-Account</span></span>
<span data-ttu-id="7e097-124">필요한 경우 모바일 서비스를 강제 설치 하는 데 사용할 실행 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-124">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="7e097-125">ASR 패브릭의 실행 계정 목록에서 1 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-125">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-126">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="7e097-126">-AzureToAzure</span></span>
<span data-ttu-id="7e097-127">복제 된 항목이 복구 Azure 지역에 복제 되는 Azure virtual machine 인 것으로 지정 하려면 Switch 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-127">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-128">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e097-128">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="7e097-129">복제 될 가상 컴퓨터 디스크 목록과 디스크를 복제 하는 데 사용할 캐시 저장소 계정 및 복구 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-129">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-130">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="7e097-130">-AzureVmId</span></span>
<span data-ttu-id="7e097-131">복제할 azure vm id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-131">Specifies the azure vm id to be replicated.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-132">-확인</span><span class="sxs-lookup"><span data-stu-id="7e097-132">-Confirm</span></span>
<span data-ttu-id="7e097-133">작업을 시작 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-133">Prompts  for confirmation before starting the operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e097-134">-DefaultProfile</span></span>
<span data-ttu-id="7e097-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-136">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="7e097-136">-HyperVToAzure</span></span>
<span data-ttu-id="7e097-137">복제 된 항목을 Azure에 복제 되는 Hyper-v 가상 컴퓨터를 지정 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-137">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-138">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="7e097-138">-IncludeDiskId</span></span>
<span data-ttu-id="7e097-139">복제에 대해 포함할 디스크 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-139">The list of disks to include for replication.</span></span> <span data-ttu-id="7e097-140">기본적으로 모든 디스크가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-140">By default all disks are included.</span></span>

```yaml
Type: String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-141">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7e097-141">-LogStorageAccountId</span></span>
<span data-ttu-id="7e097-142">복제 로그를 저장 하는 데 사용할 로그 또는 캐시 저장소 계정 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-142">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-143">-이름</span><span class="sxs-lookup"><span data-stu-id="7e097-143">-Name</span></span>
<span data-ttu-id="7e097-144">ASR 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-144">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="7e097-145">이름은 자격 증명 모음 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-145">The name must be unique within the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-146">-OS</span><span class="sxs-lookup"><span data-stu-id="7e097-146">-OS</span></span>
<span data-ttu-id="7e097-147">운영 체제 패밀리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-147">Specifies the operating system family.</span></span>
<span data-ttu-id="7e097-148">이 매개 변수에 허용 되는 값은 Windows 또는 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-148">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-149">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="7e097-149">-OSDiskName</span></span>
<span data-ttu-id="7e097-150">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-150">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="7e097-151">-ProcessServer</span></span>
<span data-ttu-id="7e097-152">이 컴퓨터를 복제 하는 데 사용할 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-152">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="7e097-153">구성 서버에 해당 하는 ASR 패브릭에 있는 프로세스 서버 목록을 사용 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-153">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-154">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7e097-154">-ProtectableItem</span></span>
<span data-ttu-id="7e097-155">복제를 사용할 수 있는 ASR 보호 가능한 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-155">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-156">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7e097-156">-ProtectionContainerMapping</span></span>
<span data-ttu-id="7e097-157">복제에 사용할 복제 정책에 해당 하는 ASR 보호 컨테이너 매핑 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-157">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-158">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="7e097-158">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="7e097-159">장애 조치 시 컴퓨터를 복구할 AvailabilitySet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-159">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-160">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="7e097-160">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="7e097-161">장애 조치 시 컴퓨터를 복구할 Azure 가상 네트워크의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-161">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-162">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7e097-162">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="7e097-163">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-163">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-164">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="7e097-164">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="7e097-165">장애 조치 시 가상 머신이 실패 한 경우 복구 Azure 가상 네트워크 내의 서브넷이 연결 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-165">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-166">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="7e097-166">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="7e097-167">이 가상 컴퓨터를 장애 조치 (failover) 할 복구 클라우드 서비스의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-167">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-168">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="7e097-168">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="7e097-169">장애 조치 시 가상 컴퓨터가 생성 될 리소스 그룹의 ARM 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-169">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-170">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="7e097-170">-RecoveryVmName</span></span>
<span data-ttu-id="7e097-171">장애 조치 이후 만든 복구 Vm의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-171">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-172">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="7e097-172">-ReplicationGroupName</span></span>
<span data-ttu-id="7e097-173">여러 VM에서 일관 된 복구 지점을 만드는 데 사용할 복제 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-173">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="7e097-174">기본적으로 각 복제 보호 항목은 자체 그룹에서 만들어지고, 다중 VM 일관성 복구 지점은 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-174">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="7e097-175">모든 컴퓨터를 동일한 복제 그룹으로 보호 하 여 여러 컴퓨터에 걸친 VM의 일관 된 복구 지점을 만들어야 하는 경우에만이 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-175">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-176">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="7e097-176">-VMwareToAzure</span></span>
<span data-ttu-id="7e097-177">복제 된 항목을 지정 하는 스위치 매개 변수는 Azure에 복제 되는 VMware 가상 머신 또는 물리적 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-177">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-178">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="7e097-178">-VmmToVmm</span></span>
<span data-ttu-id="7e097-179">복제 된 항목을 지정 하는 스위치 매개 변수는 VMM 관리 Hyper-v 사이트 간에 복제 되는 Hyper-v 가상 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-179">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-180">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7e097-180">-WaitForCompletion</span></span>
<span data-ttu-id="7e097-181">반환 하기 전에 cmdlet에서 작업이 완료 될 때까지 기다리도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-181">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e097-182">-WhatIf</span></span>
<span data-ttu-id="7e097-183">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e097-184">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-184">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e097-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e097-185">CommonParameters</span></span>
<span data-ttu-id="7e097-186">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e097-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e097-187">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e097-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e097-188">입력</span><span class="sxs-lookup"><span data-stu-id="7e097-188">INPUTS</span></span>

### <span data-ttu-id="7e097-189">SiteRecovery. ASRProtectableItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="7e097-189">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="7e097-190">출력</span><span class="sxs-lookup"><span data-stu-id="7e097-190">OUTPUTS</span></span>

### <span data-ttu-id="7e097-191">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="7e097-191">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7e097-192">상속자</span><span class="sxs-lookup"><span data-stu-id="7e097-192">NOTES</span></span>

## <span data-ttu-id="7e097-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e097-193">RELATED LINKS</span></span>

[<span data-ttu-id="7e097-194">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7e097-194">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7e097-195">제거-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7e097-195">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7e097-196">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7e097-196">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
