---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 494edd4f399855512cd7b0a847f261e711bb01cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043531"
---
# <span data-ttu-id="8ed80-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ed80-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="8ed80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ed80-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed80-103">지정 된 복제 보호 항목에 대 한 대상 네트워크 및 가상 컴퓨터 크기와 같은 복구 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="8ed80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ed80-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-EnableAcceleratedNetworkingOnRecovery]
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

## <span data-ttu-id="8ed80-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ed80-105">DESCRIPTION</span></span>
<span data-ttu-id="8ed80-106">**AzRecoveryServicesAsrReplicationProtectedItem** Cmdlet은 복제 보호 항목에 대 한 복구 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="8ed80-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8ed80-107">EXAMPLES</span></span>

### <span data-ttu-id="8ed80-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ed80-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="8ed80-109">지정 된 매개 변수를 사용 하 여 복제 보호 항목 설정을 업데이트 하는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8ed80-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="8ed80-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="8ed80-111">지정 된 매개 변수를 사용 하 여 보호 된 복제 항목 네트워크 인터페이스 카드 (NIC 감소) 설정을 업데이트 하는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8ed80-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="8ed80-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="8ed80-113">지정 된 매개 변수를 사용 하 여 복제 보호 된 항목 기본 NIC를 업데이트 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8ed80-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="8ed80-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="8ed80-115">지정 된 매개 변수를 사용 하 여 복제 보호 된 항목 NIC를 업데이트 하 고, 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8ed80-116">예제 5</span><span class="sxs-lookup"><span data-stu-id="8ed80-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="8ed80-117">복제 보호 항목을 업데이트 하는 작업을 시작 합니다. @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ @ Azure에서 복구 VM에 가속 네트워킹</span><span class="sxs-lookup"><span data-stu-id="8ed80-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="8ed80-118">EnableAcceleratedNetworkingOnRecovery가 가속 네트워킹을 사용 하지 않도록 설정 하기 위해 통과 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="8ed80-119">예제 6</span><span class="sxs-lookup"><span data-stu-id="8ed80-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="8ed80-120">지정 된 암호화 된 복제 보호 항목에 대 한 업데이트 작업을 시작 하 여 장애 조치 VM에 대해 제공 된 암호화 세부 정보를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

## <span data-ttu-id="8ed80-121">변수</span><span class="sxs-lookup"><span data-stu-id="8ed80-121">PARAMETERS</span></span>

### <span data-ttu-id="8ed80-122">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ed80-122">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="8ed80-123">테스트 장애 조치 및 장애 조치 NIC 구성 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-123">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="8ed80-124">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ed80-124">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="8ed80-125">관리 되는 디스크 Vm (Azure to Azure DR scenrio)에 대 한 udpated 디스크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-125">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="8ed80-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed80-126">-DefaultProfile</span></span>
<span data-ttu-id="8ed80-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8ed80-128">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="8ed80-128">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="8ed80-129">장애 조치 후 복구 VM으로 사용할 버전 (Azure 디스크 암호화)이 포함 된 디스크 암호화 비밀 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-129">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8ed80-130">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8ed80-130">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="8ed80-131">장애 조치 후 복구 VM으로 사용할 디스크 암호화 비밀 키 보관소 ID (Azure 디스크 암호화)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-131">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8ed80-132">-Diskidtodiska Setmap</span><span class="sxs-lookup"><span data-stu-id="8ed80-132">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="8ed80-133">디스크 리소스 Id와 디스크 암호화의 사전이 ARM Id를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-133">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="8ed80-134">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="8ed80-134">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="8ed80-135">장애 조치 (failover)에서 빠른 네트워킹을 사용 하는 경우 복구 vm에서 지정 된 NIC 지정</span><span class="sxs-lookup"><span data-stu-id="8ed80-135">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="8ed80-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ed80-136">-InputObject</span></span>
<span data-ttu-id="8ed80-137">Cmdlet에 대 한 입력 개체: 업데이트할 복제 보호 항목에 해당 하는 ASR 복제 보호 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-137">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="8ed80-138">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="8ed80-138">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="8ed80-139">장애 조치 후 복구 VM으로 사용할 디스크 암호화 키 URL 버전 (Azure 디스크 암호화)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-139">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8ed80-140">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8ed80-140">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="8ed80-141">장애 조치 후 복구 VM으로 사용할 디스크 암호화 키 keyVault ID (Azure 디스크 암호화)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-141">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="8ed80-142">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8ed80-142">-LicenseType</span></span>
<span data-ttu-id="8ed80-143">Windows Server 가상 컴퓨터에 사용할 라이선스 유형 선택 항목을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-143">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="8ed80-144">마이그레이션에 대 한 Azure 하이브리드 사용 혜택 (허브)을 사용할 자격이 있는 경우이 보호 항목을 장애 조치 하는 동안 허브 설정을 사용 하도록 지정 하는 경우 라이선스 유형을 WindowsServer로 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-144">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="8ed80-145">-이름</span><span class="sxs-lookup"><span data-stu-id="8ed80-145">-Name</span></span>
<span data-ttu-id="8ed80-146">장애 조치에 생성 되는 복구 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-146">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="8ed80-147">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="8ed80-147">-NicSelectionType</span></span>
<span data-ttu-id="8ed80-148">사용자가 설정 하거나 기본적으로 설정 되는 NIC (네트워크 인터페이스 카드) 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-148">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="8ed80-149">NotSelected를 지정 하 여 기본 값으로 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-149">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="8ed80-150">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="8ed80-150">-PrimaryNic</span></span>
<span data-ttu-id="8ed80-151">장애 조치 후 recvcovery VM에 대 한 기본 NIC로 사용 될 NIC를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-151">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="8ed80-152">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8ed80-152">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="8ed80-153">장애 조치 (failover) 후 복제 보호 항목에 대 한 가용성 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-153">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="8ed80-154">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8ed80-154">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="8ed80-155">복구 azure VM에 대 한 부팅 진단의 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-155">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="8ed80-156">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="8ed80-156">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="8ed80-157">이 가상 컴퓨터를 장애 조치 (failover) 할 복구 클라우드 서비스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-157">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="8ed80-158">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8ed80-158">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="8ed80-159">복구 NIC와 연결할 대상 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-159">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="8ed80-160">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="8ed80-160">-RecoveryNetworkId</span></span>
<span data-ttu-id="8ed80-161">보호 된 항목을 장애 조치 해야 하는 Azure 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-161">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="8ed80-162">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8ed80-162">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="8ed80-163">복구 NIC와 연결 되는 네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-163">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="8ed80-164">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="8ed80-164">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="8ed80-165">복구 시 기본 NIC에 할당 해야 하는 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-165">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="8ed80-166">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="8ed80-166">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="8ed80-167">보호 된 항목의이 NIC가 장애 조치 (failover)에 연결 되어야 하는 복구 Azure 가상 네트워크의 서브넷 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-167">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="8ed80-168">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="8ed80-168">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="8ed80-169">복구 NIC와 연결할 공용 IP 주소 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-169">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="8ed80-170">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8ed80-170">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="8ed80-171">장애 조치 시 보호 되는 항목이 복구 되는 복구 영역에 있는 Azure 리소스 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-171">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="8ed80-172">-크기</span><span class="sxs-lookup"><span data-stu-id="8ed80-172">-Size</span></span>
<span data-ttu-id="8ed80-173">복구 가상 컴퓨터 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-173">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="8ed80-174">값은 Azure 가상 머신에서 지원 되는 크기 집합에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-174">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="8ed80-175">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="8ed80-175">-TfoAzureVMName</span></span>
<span data-ttu-id="8ed80-176">테스트 장애 조치 (failover) VM의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-176">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="8ed80-177">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="8ed80-177">-UpdateNic</span></span>
<span data-ttu-id="8ed80-178">이 cmdlet이 복구 네트워크 속성을 udpated로 설정 하는 가상 컴퓨터의 NIC를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-178">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="8ed80-179">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8ed80-179">-UseManagedDisk</span></span>
<span data-ttu-id="8ed80-180">장애 조치에 만든 Azure 가상 컴퓨터에서 관리 디스크를 사용 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-180">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="8ed80-181">-확인</span><span class="sxs-lookup"><span data-stu-id="8ed80-181">-Confirm</span></span>
<span data-ttu-id="8ed80-182">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ed80-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ed80-183">-WhatIf</span></span>
<span data-ttu-id="8ed80-184">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ed80-185">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ed80-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed80-186">CommonParameters</span></span>
<span data-ttu-id="8ed80-187">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed80-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed80-188">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8ed80-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed80-189">입력</span><span class="sxs-lookup"><span data-stu-id="8ed80-189">INPUTS</span></span>

### <span data-ttu-id="8ed80-190">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="8ed80-190">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8ed80-191">출력</span><span class="sxs-lookup"><span data-stu-id="8ed80-191">OUTPUTS</span></span>

### <span data-ttu-id="8ed80-192">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="8ed80-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8ed80-193">상속자</span><span class="sxs-lookup"><span data-stu-id="8ed80-193">NOTES</span></span>

## <span data-ttu-id="8ed80-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ed80-194">RELATED LINKS</span></span>

[<span data-ttu-id="8ed80-195">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ed80-195">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="8ed80-196">새로운 AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ed80-196">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="8ed80-197">제거-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ed80-197">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
