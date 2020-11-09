---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308531"
---
# <span data-ttu-id="dccb3-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="dccb3-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="dccb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dccb3-102">SYNOPSIS</span></span>
<span data-ttu-id="dccb3-103">VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="dccb3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dccb3-104">SYNTAX</span></span>

### <span data-ttu-id="dccb3-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dccb3-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dccb3-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="dccb3-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dccb3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dccb3-107">DESCRIPTION</span></span>
<span data-ttu-id="dccb3-108">**AzVmssConfig** cmdlet은 구성 가능한 vmss (로컬 가상 관리자 배율 집합) 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="dccb3-109">VMSS 개체를 구성 하려면 다른 cmdlet이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="dccb3-110">이러한 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-110">These cmdlets are:</span></span>
- <span data-ttu-id="dccb3-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="dccb3-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="dccb3-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="dccb3-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="dccb3-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="dccb3-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="dccb3-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="dccb3-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="dccb3-115">예제의</span><span class="sxs-lookup"><span data-stu-id="dccb3-115">EXAMPLES</span></span>

### <span data-ttu-id="dccb3-116">예제 1: VMSS 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="dccb3-116">Example 1: Create a VMSS configuration object</span></span>
```powershell
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="dccb3-117">이 예제에서는 VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="dccb3-118">첫 번째 명령은 **AzVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="dccb3-119">두 번째 명령은 **새 AzVmss** cmdlet을 사용 하 여 첫 번째 명령에서 만든 vmss 구성 개체를 사용 하는 vmss를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="dccb3-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="dccb3-120">Example 2</span></span>

<span data-ttu-id="dccb3-121">VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="dccb3-122">생성</span><span class="sxs-lookup"><span data-stu-id="dccb3-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="dccb3-123">변수</span><span class="sxs-lookup"><span data-stu-id="dccb3-123">PARAMETERS</span></span>

### <span data-ttu-id="dccb3-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="dccb3-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="dccb3-125">VM의 상태 변경으로 인해 자동 복구가 일시 중단 되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="dccb3-126">상태 변경이 완료 된 후에 유예 시간이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="dccb3-127">이는 예기치 않은 복구 또는 우발적으로 수리 하는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="dccb3-128">기간을 ISO 8601 형식으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="dccb3-129">허용 되는 최소 유예 기간은 30 분 (PT30M) 이며,이 값도 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="dccb3-130">허용 되는 최대 유예 기간은 90 분 (PT90M)입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="dccb3-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="dccb3-132">최신 버전의 이미지를 사용할 수 있게 되 면 이동 방식으로 확장 설정 인스턴스에 OS 업그레이드를 자동으로 적용할지 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="dccb3-133">-부팅 진단</span><span class="sxs-lookup"><span data-stu-id="dccb3-133">-BootDiagnostic</span></span>
<span data-ttu-id="dccb3-134">가상 컴퓨터 크기 집합 부팅 진단 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dccb3-135">-DefaultProfile</span></span>
<span data-ttu-id="dccb3-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dccb3-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="dccb3-137">-DisableAutoRollback</span></span>
<span data-ttu-id="dccb3-138">자동 OS 업그레이드 정책에 대 한 자동 롤백 해제</span><span class="sxs-lookup"><span data-stu-id="dccb3-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-139">-Enable자동 복구</span><span class="sxs-lookup"><span data-stu-id="dccb3-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="dccb3-140">가상 머신 크기 집합에 대 한 자동 복구를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-140">Enables automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="dccb3-141">-EnableUltraSSD</span></span>
<span data-ttu-id="dccb3-142">하나 이상의 관리 되는 데이터 디스크를 가상 컴퓨터 크기 집합의 UltraSSD_LRS 저장소 계정 형식으로 한 개 이상 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="dccb3-143">저장소 계정 유형이 UltraSSD_LRS 관리 디스크는이 속성을 사용 하도록 설정 된 경우에만 VMSS에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="dccb3-144">-EncryptionAtHost</span></span>
<span data-ttu-id="dccb3-145">이 매개 변수는 호스트 자체의 리소스/임시 디스크를 포함 하 여 모든 디스크에 대 한 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="dccb3-146">기본값: 리소스에 대해이 속성을 true로 설정 하지 않는 한 호스트의 암호화를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="dccb3-147">-EvictionPolicy</span></span>
<span data-ttu-id="dccb3-148">확장 집합의 가상 컴퓨터에 대 한 제거 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-149">-확장</span><span class="sxs-lookup"><span data-stu-id="dccb3-149">-Extension</span></span>
<span data-ttu-id="dccb3-150">VMSS에 대 한 확장 정보 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="dccb3-151">**Add-AzVmssExtension** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="dccb3-152">-HealthProbeId</span></span>
<span data-ttu-id="dccb3-153">가상 컴퓨터 크기 집합에서 인스턴스의 상태를 확인 하는 데 사용 되는 부하 분산 장치 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="dccb3-154">HealthProbeId는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} ' 형식으로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="dccb3-155">-IdentityId</span></span>
<span data-ttu-id="dccb3-156">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="dccb3-157">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="dccb3-158">-IdentityType</span></span>
<span data-ttu-id="dccb3-159">가상 컴퓨터 크기 집합에 사용 되는 id 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="dccb3-160">' SystemAssignedUserAssigned ' 형식에는 암시적으로 만든 id와 사용자가 할당 한 id 집합이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="dccb3-161">' 없음 ' 형식은 가상 컴퓨터 배율 집합에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="dccb3-162">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dccb3-163">지정 된 SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="dccb3-163">SystemAssigned</span></span>
- <span data-ttu-id="dccb3-164">UserAssigned 됨</span><span class="sxs-lookup"><span data-stu-id="dccb3-164">UserAssigned</span></span>
- <span data-ttu-id="dccb3-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="dccb3-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="dccb3-166">않아야</span><span class="sxs-lookup"><span data-stu-id="dccb3-166">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="dccb3-167">-LicenseType</span></span>
<span data-ttu-id="dccb3-168">라이선스 종류를 지정 합니다 (사용자 고유의 라이선스 시나리오를 가져오는 데 사용).</span><span class="sxs-lookup"><span data-stu-id="dccb3-168">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-169">-위치</span><span class="sxs-lookup"><span data-stu-id="dccb3-169">-Location</span></span>
<span data-ttu-id="dccb3-170">VMSS가 만들어지는 Azure 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-170">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="dccb3-171">-MaxPrice</span></span>
<span data-ttu-id="dccb3-172">스폿 VM/VMSS에 대해 지불할 최대 가격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="dccb3-173">이 가격은 미국 달러입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-173">This price is in US Dollars.</span></span> <span data-ttu-id="dccb3-174">이 가격은 VM 크기에 대 한 현재 스폿 가격과 비교 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="dccb3-175">또한 스폿 VM/VMSS를 만들거나 업데이트 하는 시점에 가격을 비교 하 고 maxPrice가 현재 스폿 가격 보다 더 큰 경우에만 작동을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="dccb3-176">현재 스폿 가격이 VM/VMSS를 만든 후 maxPrice를 초과 하는 경우에도 maxPrice는 스폿 VM/VMSS를 제거 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="dccb3-177">가능한 값은 다음과 같습니다. 0 보다 큰 10 진수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="dccb3-178">예: 0.01538.</span><span class="sxs-lookup"><span data-stu-id="dccb3-178">Example: 0.01538.</span></span>  <span data-ttu-id="dccb3-179">-1은 스폿 VM/VMSS가 가격 이유로 제거 되어서는 안 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="dccb3-180">또한 기본 최대 가격은 사용자가 제공 하지 않는 경우-1입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-180">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="dccb3-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="dccb3-182">VMSS 구성에 대 한 네트워킹 속성을 포함 하는 네트워크 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="dccb3-183">**Add-AzVmssNetworkInterfaceConfiguration** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="dccb3-184">-OsProfile</span></span>
<span data-ttu-id="dccb3-185">VMSS 구성에 대 한 운영 체제 속성을 포함 하는 운영 체제 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="dccb3-186">**Set-AzVmssOsProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-187">-과잉 프로비저닝</span><span class="sxs-lookup"><span data-stu-id="dccb3-187">-Overprovision</span></span>
<span data-ttu-id="dccb3-188">Cmdlet이 VMSS를 프로 비전 하 고 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-189">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="dccb3-189">-PlanName</span></span>
<span data-ttu-id="dccb3-190">계획 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-190">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-191">계획 제품</span><span class="sxs-lookup"><span data-stu-id="dccb3-191">-PlanProduct</span></span>
<span data-ttu-id="dccb3-192">계획 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-192">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="dccb3-193">-PlanPromotionCode</span></span>
<span data-ttu-id="dccb3-194">계획 프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-194">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-195">-계획 Publisher</span><span class="sxs-lookup"><span data-stu-id="dccb3-195">-PlanPublisher</span></span>
<span data-ttu-id="dccb3-196">계획 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-196">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="dccb3-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="dccb3-198">각 배치 그룹의 오류 도메인 수입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-198">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-199">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="dccb3-199">-Priority</span></span>
<span data-ttu-id="dccb3-200">크기 조정 집합의 가상 machien에 대 한 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="dccb3-201">' 일반 ', ' 스폿 ' 및 ' Low ' 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="dccb3-202">' 일반 '은 일반 가상 컴퓨터에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="dccb3-203">' 스폿 '은 가상 컴퓨터를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="dccb3-204">' Low '는 스폿 가상 컴퓨터에도 사용할 수 있지만 ' 스폿 '으로 대체 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="dccb3-205">' 낮음 ' 대신 ' 스폿 '을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="dccb3-205">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="dccb3-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="dccb3-207">이 배율 집합에 사용할 근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="dccb3-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="dccb3-209">롤링 업그레이드 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-209">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="dccb3-210">-ScaleInPolicy</span></span>
<span data-ttu-id="dccb3-211">가상 컴퓨터 배율 집합의 크기 조정을 할 때 따라야 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="dccb3-212">사용할 수 있는 값은 ' Default ', ' OldestVM ' 및 ' NewestVM '입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="dccb3-213">' Default ' 가상 컴퓨터 배율 집합이에서 크기를 조정 하면 영역에 대해 먼저 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="dccb3-214">그런 다음, 최대한 다양 한 장애 도메인에 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="dccb3-215">각 장애 도메인 내에서 제거 하도록 선택 된 가상 머신은 확장 기능에서 보호 되지 않는 최신 것입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="dccb3-216">' OldestVM ' 가상 컴퓨터 크기 조정 집합을 확장 하는 동안에는 스케일에서 보호 되지 않는 가장 오래 된 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="dccb3-217">영역 가상 컴퓨터 배율 집합의 경우에는 맨 먼저 범위에서 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="dccb3-218">각 영역 내에서 보호 되지 않는 가장 오래 된 가상 컴퓨터는 제거 하도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="dccb3-219">' NewestVM ' 가상 컴퓨터 배율 집합이 확장 되는 경우에는 스케일에서 보호 되지 않는 최신 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="dccb3-220">영역 가상 컴퓨터 배율 집합의 경우에는 맨 먼저 범위에서 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="dccb3-221">각 영역 내에서 보호 되지 않는 최신 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-222">-Single배치 그룹</span><span class="sxs-lookup"><span data-stu-id="dccb3-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="dccb3-223">단일 배치 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-223">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="dccb3-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="dccb3-225">추가 과잉 프로 비전 된 Vm에서 확장이 실행 되지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="dccb3-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="dccb3-226">-SkuCapacity</span></span>
<span data-ttu-id="dccb3-227">VMSS의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-227">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-228">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="dccb3-228">-SkuName</span></span>
<span data-ttu-id="dccb3-229">VMSS의 모든 인스턴스 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-229">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-230">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="dccb3-230">-SkuTier</span></span>
<span data-ttu-id="dccb3-231">VMSS의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="dccb3-232">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dccb3-233">표준이</span><span class="sxs-lookup"><span data-stu-id="dccb3-233">Standard</span></span>
- <span data-ttu-id="dccb3-234">기본적</span><span class="sxs-lookup"><span data-stu-id="dccb3-234">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="dccb3-235">-StorageProfile</span></span>
<span data-ttu-id="dccb3-236">VMSS 구성의 디스크 속성이 포함 된 저장소 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="dccb3-237">**Set-AzVmssStorageProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-238">태그</span><span class="sxs-lookup"><span data-stu-id="dccb3-238">-Tag</span></span>
<span data-ttu-id="dccb3-239">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dccb3-240">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="dccb3-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="dccb3-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="dccb3-242">구성 가능한 기간 (분) 삭제 되는 가상 컴퓨터는 이벤트가 자동으로 승인 되기 전에 종료 예약 된 이벤트를 승인 해야 합니다 (시간 초과).</span><span class="sxs-lookup"><span data-stu-id="dccb3-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="dccb3-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="dccb3-244">예약 된 이벤트 종료 사용</span><span class="sxs-lookup"><span data-stu-id="dccb3-244">Enable the Terminate Scheduled events</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="dccb3-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="dccb3-246">확장 집합의 가상 컴퓨터로 업그레이드 모드를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="dccb3-247">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dccb3-248">자동 번역</span><span class="sxs-lookup"><span data-stu-id="dccb3-248">Automatic</span></span>
- <span data-ttu-id="dccb3-249">수동</span><span class="sxs-lookup"><span data-stu-id="dccb3-249">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="dccb3-250">-Zone</span></span>
<span data-ttu-id="dccb3-251">가상 컴퓨터 크기 집합에 대 한 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-251">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccb3-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="dccb3-252">-ZoneBalance</span></span>
<span data-ttu-id="dccb3-253">영역 작동이 중단 되는 경우를 대비 하 여 가상 컴퓨터 배포 교차 x 영역을 강제 적용할지 여부</span><span class="sxs-lookup"><span data-stu-id="dccb3-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="dccb3-254">-확인</span><span class="sxs-lookup"><span data-stu-id="dccb3-254">-Confirm</span></span>
<span data-ttu-id="dccb3-255">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dccb3-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dccb3-256">-WhatIf</span></span>
<span data-ttu-id="dccb3-257">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dccb3-258">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dccb3-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dccb3-259">CommonParameters</span></span>
<span data-ttu-id="dccb3-260">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dccb3-261">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dccb3-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dccb3-262">입력</span><span class="sxs-lookup"><span data-stu-id="dccb3-262">INPUTS</span></span>

### <span data-ttu-id="dccb3-263">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dccb3-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dccb3-264">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dccb3-264">System.String</span></span>

### <span data-ttu-id="dccb3-265">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="dccb3-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dccb3-266">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="dccb3-266">System.Int32</span></span>

### <span data-ttu-id="dccb3-267">시스템 Null 허용 ' 1 [[23.0.0.0]. UpgradeMode, Microsoft Azure. 관리., Version = 31bf3856ad364e35, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="dccb3-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="dccb3-268">VirtualMachineScaleSetOSProfile를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="dccb3-269">VirtualMachineScaleSetStorageProfile를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="dccb3-270">Microsoft VirtualMachineScaleSetNetworkConfiguration []을 (를)</span><span class="sxs-lookup"><span data-stu-id="dccb3-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="dccb3-271">Microsoft VirtualMachineScaleSetExtension []을 (를)</span><span class="sxs-lookup"><span data-stu-id="dccb3-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="dccb3-272">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="dccb3-272">System.String[]</span></span>

### <span data-ttu-id="dccb3-273">RollingUpgradePolicy를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="dccb3-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="dccb3-274">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dccb3-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dccb3-275">Microsoft. Azure. 관리자. 부팅 진단</span><span class="sxs-lookup"><span data-stu-id="dccb3-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="dccb3-276">시스템 Null 허용 ' 1 [[ResourceIdentityType, Microsoft azure. 23.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dccb3-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="dccb3-277">출력</span><span class="sxs-lookup"><span data-stu-id="dccb3-277">OUTPUTS</span></span>

### <span data-ttu-id="dccb3-278">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="dccb3-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="dccb3-279">상속자</span><span class="sxs-lookup"><span data-stu-id="dccb3-279">NOTES</span></span>

## <span data-ttu-id="dccb3-280">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dccb3-280">RELATED LINKS</span></span>

[<span data-ttu-id="dccb3-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="dccb3-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="dccb3-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="dccb3-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="dccb3-283">추가-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="dccb3-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="dccb3-284">추가-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="dccb3-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="dccb3-285">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="dccb3-285">New-AzVmss</span></span>](./New-AzVmss.md)
