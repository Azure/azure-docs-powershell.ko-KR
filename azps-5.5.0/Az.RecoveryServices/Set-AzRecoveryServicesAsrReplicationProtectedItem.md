---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 21c924d02a18ae60f07abd616809358208256039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191316"
---
# <span data-ttu-id="07304-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07304-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="07304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07304-102">SYNOPSIS</span></span>
<span data-ttu-id="07304-103">지정된 복제 보호 항목에 대한 대상 네트워크 및 가상 머신 크기와 같은 복구 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="07304-104">구문</span><span class="sxs-lookup"><span data-stu-id="07304-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-EnableAcceleratedNetworkingOnRecovery]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07304-105">설명</span><span class="sxs-lookup"><span data-stu-id="07304-105">DESCRIPTION</span></span>
<span data-ttu-id="07304-106">**Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet은 복제 보호된 항목에 대한 복구 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="07304-107">예제</span><span class="sxs-lookup"><span data-stu-id="07304-107">EXAMPLES</span></span>

### <span data-ttu-id="07304-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="07304-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="07304-109">지정된 매개 변수를 사용하여 복제 보호된 항목 설정을 업데이트하는 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="07304-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="07304-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="07304-111">지정된 매개 변수를 사용하여 복제 보호 항목 네트워크 인터페이스 카드(NIC 감소) 설정을 업데이트하는 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="07304-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="07304-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="07304-113">지정된 매개 변수를 사용하여 복제 보호된 항목 기본 NIC(복구된 vm )설정 업데이트 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="07304-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="07304-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="07304-115">지정된 매개 변수를 사용하여 복제 보호된 항목 NIC(복구된 vm 설정에 사용)를 업데이트하는 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="07304-116">예제 5</span><span class="sxs-lookup"><span data-stu-id="07304-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="07304-117">선택한 noc tp를 사용하여 복구 VM(Azure에서 Azure로 재해 복구)에서 가속화된 네트워킹을 사용하도록 선택한 복제 보호 항목을 업데이트하는 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="07304-118">가속 네트워킹을 사용하지 않도록 설정하려면 -EnableAcceleratedNetworkingOnRecovery를 전달하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07304-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="07304-119">예제 6</span><span class="sxs-lookup"><span data-stu-id="07304-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="07304-120">지정된 암호화된 복제 보호 항목에 대한 업데이트 작업을 시작하여 장애 조치(failover) VM에 제공된 암호화 세부 정보를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="07304-121">예제 7</span><span class="sxs-lookup"><span data-stu-id="07304-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="07304-122">지정된 복제 보호 항목에 대한 업데이트 작업을 시작하여 장애 조치(failover) VM에 제공된 근접 배치 그룹을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>

## <span data-ttu-id="07304-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07304-123">PARAMETERS</span></span>

### <span data-ttu-id="07304-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="07304-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="07304-125">테스트 장애 조치(failover) 및 장애 조치(failover) NIC 구성 세부 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-125">Specifies the test failover and failover NIC configuration details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07304-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="07304-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="07304-127">관리 디스크 VM에 대해 udpated할 디스크 구성을 지정합니다(Azure에서 Azure DR scenrio로).</span><span class="sxs-lookup"><span data-stu-id="07304-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07304-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07304-128">-DefaultProfile</span></span>
<span data-ttu-id="07304-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07304-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="07304-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="07304-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="07304-131">장애 조치(failover) 후 복구 VM으로 사용할 버전(Azure 디스크 암호화)을 사용하여 디스크 암호화 비밀 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="07304-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="07304-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="07304-133">장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 비밀 키 자격 증명 모음 ID(Azure Disk Encryption)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="07304-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="07304-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="07304-135">디스크 리소스 ID에서 디스크 암호화 집합으로의 사전 ARM ID입니다.</span><span class="sxs-lookup"><span data-stu-id="07304-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07304-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="07304-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="07304-137">장애 조치(failover)가 가속화된 네트워킹을 사용하여 복구 VM에 지정된 NIC를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="07304-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07304-138">-InputObject</span></span>
<span data-ttu-id="07304-139">cmdlet에 대한 입력 개체: 업데이트할 복제 보호 항목에 해당하는 ASR 복제 보호된 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="07304-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07304-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="07304-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="07304-141">장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 키 URL 버전(Azure 디스크 암호화)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="07304-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="07304-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="07304-143">장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 keyVault ID(Azure Disk Encryption)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="07304-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="07304-144">-LicenseType</span></span>
<span data-ttu-id="07304-145">Windows Server 가상 머신에 사용할 라이선스 유형 선택을 정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="07304-146">마이그레이션에 Azure HUB(Hybrid Use Benefit)를 사용할 자격이 있으며 이 보호된 항목을 장애 조치하는 동안 허브 설정을 사용할 수 있도록 지정하려는 경우 라이선스 유형을 WindowsServer로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="07304-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07304-147">-Name</span><span class="sxs-lookup"><span data-stu-id="07304-147">-Name</span></span>
<span data-ttu-id="07304-148">장애 조치 시 만들 복구 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="07304-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="07304-149">-NicSelectionType</span></span>
<span data-ttu-id="07304-150">사용자가 설정하거나 기본적으로 설정한 NIC(네트워크 인터페이스 카드) 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="07304-151">NotSelected를 지정하여 기본값으로 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07304-151">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07304-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="07304-152">-PrimaryNic</span></span>
<span data-ttu-id="07304-153">장애 조치(failover) 후 재구성 VM에 대한 기본 NIC로 사용할 NIC를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="07304-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="07304-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="07304-155">장애 조치(failover) 후 복제 보호 항목에 대한 가용성 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="07304-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="07304-156">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="07304-156">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="07304-157">장애 조치(failover) 후 복제 보호 항목에 대한 가용성 영역 지정</span><span class="sxs-lookup"><span data-stu-id="07304-157">Specifies availability zone for replication protected item after failover.</span></span>

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

### <span data-ttu-id="07304-158">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="07304-158">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="07304-159">복구 Azure VM에 대한 부팅 진단을 위한 저장소 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-159">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="07304-160">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="07304-160">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="07304-161">이 가상 머신을 장애 조치(failover)할 복구 클라우드 서비스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="07304-161">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="07304-162">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="07304-162">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="07304-163">복구 NIC와 연결될 대상 백안 주소 풀을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-163">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07304-164">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="07304-164">-RecoveryNetworkId</span></span>
<span data-ttu-id="07304-165">보호된 항목을 실패해야 하는 Azure 가상 네트워크의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-165">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="07304-166">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="07304-166">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="07304-167">복구 NIC와 연결될 네트워크 보안 그룹의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-167">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="07304-168">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="07304-168">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="07304-169">복구 시 기본 NIC에 할당해야 하는 고정 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-169">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="07304-170">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="07304-170">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="07304-171">장애 조치 시 보호된 항목의 이 NIC를 연결해야 하는 복구 Azure 가상 네트워크의 서브넷 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-171">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="07304-172">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="07304-172">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="07304-173">가상 머신을 장애 조치할 복구 근접 배치 그룹의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-173">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="07304-174">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="07304-174">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="07304-175">복구 NIC와 연결될 공용 IP 주소 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-175">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="07304-176">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="07304-176">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="07304-177">장애 조치 시 보호된 항목을 복구할 복구 지역의 Azure 리소스 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="07304-177">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="07304-178">-Size</span><span class="sxs-lookup"><span data-stu-id="07304-178">-Size</span></span>
<span data-ttu-id="07304-179">복구 가상 머신 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-179">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="07304-180">값은 Azure 가상 머신에서 지원하는 크기 집합에서 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-180">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="07304-181">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="07304-181">-TfoAzureVMName</span></span>
<span data-ttu-id="07304-182">테스트 장애 조치(failover) VM의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-182">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="07304-183">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="07304-183">-UpdateNic</span></span>
<span data-ttu-id="07304-184">이 cmdlet이 복구 네트워크 속성을 udpated해야 하는 가상 머신의 NIC를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-184">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="07304-185">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="07304-185">-UseManagedDisk</span></span>
<span data-ttu-id="07304-186">장애 조치(failover)에 생성된 Azure 가상 머신이 관리 디스크를 사용할지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-186">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07304-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07304-187">-Confirm</span></span>
<span data-ttu-id="07304-188">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07304-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07304-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07304-189">-WhatIf</span></span>
<span data-ttu-id="07304-190">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="07304-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07304-191">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07304-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07304-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07304-192">CommonParameters</span></span>
<span data-ttu-id="07304-193">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07304-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07304-194">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="07304-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07304-195">입력</span><span class="sxs-lookup"><span data-stu-id="07304-195">INPUTS</span></span>

### <span data-ttu-id="07304-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07304-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="07304-197">출력</span><span class="sxs-lookup"><span data-stu-id="07304-197">OUTPUTS</span></span>

### <span data-ttu-id="07304-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="07304-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="07304-199">참고 사항</span><span class="sxs-lookup"><span data-stu-id="07304-199">NOTES</span></span>

## <span data-ttu-id="07304-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07304-200">RELATED LINKS</span></span>

[<span data-ttu-id="07304-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07304-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="07304-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07304-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="07304-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07304-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
