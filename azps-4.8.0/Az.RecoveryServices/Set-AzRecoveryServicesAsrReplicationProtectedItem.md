---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1b5f447e95e137ba9199ba596029f2088a977c91
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204924"
---
# <span data-ttu-id="8becc-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8becc-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="8becc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8becc-102">SYNOPSIS</span></span>
<span data-ttu-id="8becc-103">지정 된 복제 보호 항목에 대 한 대상 네트워크 및 가상 컴퓨터 크기와 같은 복구 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="8becc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8becc-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8becc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8becc-105">DESCRIPTION</span></span>
<span data-ttu-id="8becc-106">**AzRecoveryServicesAsrReplicationProtectedItem** Cmdlet은 복제 보호 항목에 대 한 복구 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="8becc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8becc-107">EXAMPLES</span></span>

### <span data-ttu-id="8becc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8becc-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="8becc-109">지정 된 매개 변수를 사용 하 여 복제 보호 항목 설정을 업데이트 하는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8becc-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="8becc-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="8becc-111">지정 된 매개 변수를 사용 하 여 보호 된 복제 항목 네트워크 인터페이스 카드 (NIC 감소) 설정을 업데이트 하는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8becc-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="8becc-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="8becc-113">지정 된 매개 변수를 사용 하 여 복제 보호 된 항목 기본 NIC를 업데이트 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8becc-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="8becc-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="8becc-115">지정 된 매개 변수를 사용 하 여 복제 보호 된 항목 NIC를 업데이트 하 고, 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8becc-116">예제 5</span><span class="sxs-lookup"><span data-stu-id="8becc-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="8becc-117">복제 보호 항목을 업데이트 하는 작업을 시작 합니다. @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ Azure에서 복구 VM에 가속 네트워킹</span><span class="sxs-lookup"><span data-stu-id="8becc-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="8becc-118">EnableAcceleratedNetworkingOnRecovery가 가속 네트워킹을 사용 하지 않도록 설정 하기 위해 통과 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="8becc-119">예제 6</span><span class="sxs-lookup"><span data-stu-id="8becc-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="8becc-120">지정 된 암호화 된 복제 보호 항목에 대 한 업데이트 작업을 시작 하 여 장애 조치 VM에 대해 제공 된 암호화 세부 정보를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="8becc-121">예제 7</span><span class="sxs-lookup"><span data-stu-id="8becc-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="8becc-122">장애 조치 (failover) VM에 대해 제공 된 근접 배치 그룹을 사용 하도록 지정 된 복제 보호 항목에 대 한 업데이트 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>


## <span data-ttu-id="8becc-123">변수</span><span class="sxs-lookup"><span data-stu-id="8becc-123">PARAMETERS</span></span>

### <span data-ttu-id="8becc-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="8becc-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="8becc-125">테스트 장애 조치 및 장애 조치 NIC 구성 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-125">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="8becc-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="8becc-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="8becc-127">관리 되는 디스크 Vm (Azure to Azure DR scenrio)에 대 한 udpated 디스크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="8becc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8becc-128">-DefaultProfile</span></span>
<span data-ttu-id="8becc-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8becc-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="8becc-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="8becc-131">장애 조치 후 복구 VM으로 사용할 버전 (Azure 디스크 암호화)이 포함 된 디스크 암호화 비밀 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8becc-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8becc-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="8becc-133">장애 조치 후 복구 VM으로 사용할 디스크 암호화 비밀 키 보관소 ID (Azure 디스크 암호화)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8becc-134">-Diskidtodiska Setmap</span><span class="sxs-lookup"><span data-stu-id="8becc-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="8becc-135">디스크 리소스 Id와 디스크 암호화의 사전이 ARM Id를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="8becc-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="8becc-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="8becc-137">장애 조치 (failover)에서 빠른 네트워킹을 사용 하는 경우 복구 vm에서 지정 된 NIC 지정</span><span class="sxs-lookup"><span data-stu-id="8becc-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="8becc-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8becc-138">-InputObject</span></span>
<span data-ttu-id="8becc-139">Cmdlet에 대 한 입력 개체: 업데이트할 복제 보호 항목에 해당 하는 ASR 복제 보호 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="8becc-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="8becc-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="8becc-141">장애 조치 후 복구 VM으로 사용할 디스크 암호화 키 URL 버전 (Azure 디스크 암호화)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8becc-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8becc-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="8becc-143">장애 조치 후 복구 VM으로 사용할 디스크 암호화 키 keyVault ID (Azure 디스크 암호화)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="8becc-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8becc-144">-LicenseType</span></span>
<span data-ttu-id="8becc-145">Windows Server 가상 컴퓨터에 사용할 라이선스 유형 선택 항목을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="8becc-146">마이그레이션에 대 한 Azure 하이브리드 사용 혜택 (허브)을 사용할 자격이 있는 경우이 보호 항목을 장애 조치 하는 동안 허브 설정을 사용 하도록 지정 하는 경우 라이선스 유형을 WindowsServer로 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="8becc-147">-이름</span><span class="sxs-lookup"><span data-stu-id="8becc-147">-Name</span></span>
<span data-ttu-id="8becc-148">장애 조치에 생성 되는 복구 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="8becc-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="8becc-149">-NicSelectionType</span></span>
<span data-ttu-id="8becc-150">사용자가 설정 하거나 기본적으로 설정 되는 NIC (네트워크 인터페이스 카드) 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="8becc-151">NotSelected를 지정 하 여 기본 값으로 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-151">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="8becc-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="8becc-152">-PrimaryNic</span></span>
<span data-ttu-id="8becc-153">장애 조치 후 recvcovery VM에 대 한 기본 NIC로 사용 될 NIC를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="8becc-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8becc-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="8becc-155">장애 조치 (failover) 후 복제 보호 항목에 대 한 가용성 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="8becc-156">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8becc-156">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="8becc-157">복구 azure VM에 대 한 부팅 진단의 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-157">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="8becc-158">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="8becc-158">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="8becc-159">이 가상 컴퓨터를 장애 조치 (failover) 할 복구 클라우드 서비스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-159">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="8becc-160">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8becc-160">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="8becc-161">복구 NIC와 연결할 대상 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-161">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="8becc-162">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="8becc-162">-RecoveryNetworkId</span></span>
<span data-ttu-id="8becc-163">보호 된 항목을 장애 조치 해야 하는 Azure 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-163">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="8becc-164">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8becc-164">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="8becc-165">복구 NIC와 연결 되는 네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-165">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="8becc-166">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="8becc-166">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="8becc-167">복구 시 기본 NIC에 할당 해야 하는 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-167">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="8becc-168">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="8becc-168">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="8becc-169">보호 된 항목의이 NIC가 장애 조치 (failover)에 연결 되어야 하는 복구 Azure 가상 네트워크의 서브넷 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-169">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="8becc-170">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="8becc-170">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="8becc-171">가상 컴퓨터를 장애 조치용으로 하는 복구 근접 배치 그룹의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-171">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="8becc-172">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="8becc-172">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="8becc-173">복구 NIC와 연결할 공용 IP 주소 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-173">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="8becc-174">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8becc-174">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="8becc-175">장애 조치 시 보호 되는 항목이 복구 되는 복구 영역에 있는 Azure 리소스 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-175">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="8becc-176">-크기</span><span class="sxs-lookup"><span data-stu-id="8becc-176">-Size</span></span>
<span data-ttu-id="8becc-177">복구 가상 컴퓨터 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-177">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="8becc-178">값은 Azure 가상 머신에서 지원 되는 크기 집합에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-178">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="8becc-179">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="8becc-179">-TfoAzureVMName</span></span>
<span data-ttu-id="8becc-180">테스트 장애 조치 (failover) VM의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-180">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="8becc-181">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="8becc-181">-UpdateNic</span></span>
<span data-ttu-id="8becc-182">이 cmdlet이 복구 네트워크 속성을 udpated로 설정 하는 가상 컴퓨터의 NIC를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-182">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="8becc-183">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8becc-183">-UseManagedDisk</span></span>
<span data-ttu-id="8becc-184">장애 조치에 만든 Azure 가상 컴퓨터에서 관리 디스크를 사용 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-184">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="8becc-185">-확인</span><span class="sxs-lookup"><span data-stu-id="8becc-185">-Confirm</span></span>
<span data-ttu-id="8becc-186">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8becc-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8becc-187">-WhatIf</span></span>
<span data-ttu-id="8becc-188">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-188">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8becc-189">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8becc-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8becc-190">CommonParameters</span></span>
<span data-ttu-id="8becc-191">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8becc-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8becc-192">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8becc-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8becc-193">입력</span><span class="sxs-lookup"><span data-stu-id="8becc-193">INPUTS</span></span>

### <span data-ttu-id="8becc-194">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="8becc-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8becc-195">출력</span><span class="sxs-lookup"><span data-stu-id="8becc-195">OUTPUTS</span></span>

### <span data-ttu-id="8becc-196">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="8becc-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8becc-197">상속자</span><span class="sxs-lookup"><span data-stu-id="8becc-197">NOTES</span></span>

## <span data-ttu-id="8becc-198">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8becc-198">RELATED LINKS</span></span>

[<span data-ttu-id="8becc-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8becc-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="8becc-200">새로운 AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8becc-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="8becc-201">제거-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8becc-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
