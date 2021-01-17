---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372625"
---
# <span data-ttu-id="b08ff-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b08ff-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="b08ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b08ff-102">SYNOPSIS</span></span>
<span data-ttu-id="b08ff-103">VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="b08ff-104">구문</span><span class="sxs-lookup"><span data-stu-id="b08ff-104">SYNTAX</span></span>

### <span data-ttu-id="b08ff-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b08ff-105">DefaultParameterSet (Default)</span></span>
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

### <span data-ttu-id="b08ff-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b08ff-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="b08ff-107">설명</span><span class="sxs-lookup"><span data-stu-id="b08ff-107">DESCRIPTION</span></span>
<span data-ttu-id="b08ff-108">**New-AzVmssConfig** cmdlet은 구성 가능한 로컬 VMSS(Virtual Manager Scale Set) 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="b08ff-109">다른 cmdlet은 VMSS 개체를 구성하는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="b08ff-110">이러한 cmdlet은</span><span class="sxs-lookup"><span data-stu-id="b08ff-110">These cmdlets are:</span></span>
- <span data-ttu-id="b08ff-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="b08ff-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="b08ff-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b08ff-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="b08ff-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b08ff-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="b08ff-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b08ff-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="b08ff-115">예제</span><span class="sxs-lookup"><span data-stu-id="b08ff-115">EXAMPLES</span></span>

### <span data-ttu-id="b08ff-116">예제 1: VMSS 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="b08ff-116">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="b08ff-117">이 예제에서는 VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="b08ff-118">첫 번째 명령은 **New-AzVmssConfig** cmdlet을 사용하여 VMSS 구성 개체를 만들고 결과를 VMSS라는 이름의 변수에 $VMSS.</span><span class="sxs-lookup"><span data-stu-id="b08ff-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="b08ff-119">두 번째 명령은 **New-AzVmss** cmdlet을 사용하여 첫 번째 명령에서 만든 VMSS 구성 개체를 사용하는 VMSS를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="b08ff-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="b08ff-120">Example 2</span></span>

<span data-ttu-id="b08ff-121">VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="b08ff-122">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="b08ff-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="b08ff-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b08ff-123">PARAMETERS</span></span>

### <span data-ttu-id="b08ff-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="b08ff-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="b08ff-125">VM의 상태 변경으로 인해 자동 복구가 일시 중단되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="b08ff-126">유예 시간은 상태 변경이 완료된 후에 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="b08ff-127">이렇게 하면 조기 또는 실수로 수리를 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="b08ff-128">기간은 ISO 8601 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="b08ff-129">허용되는 최소 유예 기간은 기본값인 30분(PT30M)입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="b08ff-130">허용되는 최대 유예 기간은 90분(PT90M)입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="b08ff-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="b08ff-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="b08ff-132">최신 버전의 이미지를 사용할 수 있을 때 OS 업그레이드를 롤링식으로 확장 집합 인스턴스에 자동으로 적용해야 하는지 여부를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="b08ff-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b08ff-133">-BootDiagnostic</span></span>
<span data-ttu-id="b08ff-134">가상 머신 확장 집합 부팅 진단 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="b08ff-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08ff-135">-DefaultProfile</span></span>
<span data-ttu-id="b08ff-136">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b08ff-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="b08ff-137">-DisableAutoRollback</span></span>
<span data-ttu-id="b08ff-138">자동 OS 업그레이드 정책에 대한 자동 롤백 사용 안</span><span class="sxs-lookup"><span data-stu-id="b08ff-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="b08ff-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="b08ff-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="b08ff-140">가상 머신 확장 집합에서 자동 복구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="b08ff-141">-EnableUltrassd</span><span class="sxs-lookup"><span data-stu-id="b08ff-141">-EnableUltraSSD</span></span>
<span data-ttu-id="b08ff-142">가상 머신 확장 집합에 저장소 계정 유형이 UltraSSD_LRS 하나 이상의 관리되는 데이터 디스크를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="b08ff-143">저장소 계정 유형이 UltraSSD_LRS 관리 디스크는 이 속성을 사용하는 UltraSSD_LRS VMSS에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="b08ff-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="b08ff-144">-EncryptionAtHost</span></span>
<span data-ttu-id="b08ff-145">이 매개 변수는 호스트 자체의 리소스/임시 디스크를 포함한 모든 디스크에 대해 암호화를 사용하도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="b08ff-146">기본값: 이 속성이 리소스에 대해 true로 설정되지 않으면 호스트의 암호화가 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="b08ff-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="b08ff-147">-EvictionPolicy</span></span>
<span data-ttu-id="b08ff-148">확장 집합의 가상 머신에 대한 지우기 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="b08ff-149">-Extension</span><span class="sxs-lookup"><span data-stu-id="b08ff-149">-Extension</span></span>
<span data-ttu-id="b08ff-150">VMSS에 대한 확장 정보 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="b08ff-151">**Add-AzVmssExtension** cmdlet을 사용하여 이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="b08ff-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="b08ff-152">-HealthProbeId</span></span>
<span data-ttu-id="b08ff-153">가상 머신 확장 집합에서 인스턴스의 상태 확인에 사용되는 부하 균형 조정기 프로브의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="b08ff-154">HealthProbeId는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="b08ff-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="b08ff-155">-IdentityId</span></span>
<span data-ttu-id="b08ff-156">가상 머신 확장 집합과 연결된 사용자 ID 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="b08ff-157">사용자 ARM ID 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' 형식의 리소스 ID로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="b08ff-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b08ff-158">-IdentityType</span></span>
<span data-ttu-id="b08ff-159">가상 머신 확장 집합에 사용되는 ID 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="b08ff-160">'SystemAssignedUserAssigned' 형식에는 암시적으로 만든 ID와 사용자 할당 ID 집합이 모두 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="b08ff-161">'없음' 형식은 가상 머신 확장 집합에서 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="b08ff-162">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="b08ff-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b08ff-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="b08ff-163">SystemAssigned</span></span>
- <span data-ttu-id="b08ff-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="b08ff-164">UserAssigned</span></span>
- <span data-ttu-id="b08ff-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="b08ff-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="b08ff-166">없음</span><span class="sxs-lookup"><span data-stu-id="b08ff-166">None</span></span>

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

### <span data-ttu-id="b08ff-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b08ff-167">-LicenseType</span></span>
<span data-ttu-id="b08ff-168">사용자 라이선스 시나리오를 가져오기 위한 라이선스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="b08ff-169">-Location</span><span class="sxs-lookup"><span data-stu-id="b08ff-169">-Location</span></span>
<span data-ttu-id="b08ff-170">VMSS가 생성되는 Azure 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="b08ff-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="b08ff-171">-MaxPrice</span></span>
<span data-ttu-id="b08ff-172">스폿 VM/VMSS에 대해 지불할 최대 가격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="b08ff-173">이 가격은 미국 달러입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-173">This price is in US Dollars.</span></span> <span data-ttu-id="b08ff-174">이 가격은 VM 크기에 대한 현재 스폿 가격과 비교됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="b08ff-175">또한 가격은 스폿 VM/VMSS를 만들/업데이트할 때와 비교하며 maxPrice가 현재 스폿 가격보다 큰 경우 작업이 성공합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="b08ff-176">현재 스폿 가격이 VM/VMSS를 생성한 후 maxPrice를 초과하는 경우 maxPrice는 스폿 VM/VMSS를 꺼는 데도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="b08ff-177">가능한 값은 0보다 큰 모든 10진수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="b08ff-178">예: 0.01538.</span><span class="sxs-lookup"><span data-stu-id="b08ff-178">Example: 0.01538.</span></span>  <span data-ttu-id="b08ff-179">-1은 가격상의 이유로 스폿 VM/VMSS를 피하지 말아야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="b08ff-180">또한 사용자가 제공하지 않는 경우 기본 최대 가격은 -1입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="b08ff-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b08ff-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="b08ff-182">VMSS 구성에 대한 네트워킹 속성을 포함하는 네트워크 프로필 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="b08ff-183">**Add-AzVmssNetworkInterfaceConfiguration** cmdlet을 사용하여 이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="b08ff-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="b08ff-184">-OsProfile</span></span>
<span data-ttu-id="b08ff-185">VMSS 구성에 대한 운영 체제 속성을 포함하는 운영 체제 프로필 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="b08ff-186">**Set-AzVmssOsProfile** cmdlet을 사용하여 이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="b08ff-187">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="b08ff-187">-Overprovision</span></span>
<span data-ttu-id="b08ff-188">cmdlet이 VMSS를 오버프로비전하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="b08ff-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="b08ff-189">-PlanName</span></span>
<span data-ttu-id="b08ff-190">계획 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="b08ff-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="b08ff-191">-PlanProduct</span></span>
<span data-ttu-id="b08ff-192">계획 제품을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="b08ff-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="b08ff-193">-PlanPromotionCode</span></span>
<span data-ttu-id="b08ff-194">계획 프로모션 코드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="b08ff-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="b08ff-195">-PlanPublisher</span></span>
<span data-ttu-id="b08ff-196">계획 게시자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="b08ff-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="b08ff-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="b08ff-198">각 배치 그룹에 대한 장애 도메인 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="b08ff-199">-Priority</span><span class="sxs-lookup"><span data-stu-id="b08ff-199">-Priority</span></span>
<span data-ttu-id="b08ff-200">확장 집합의 가상 머신에 대한 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="b08ff-201">지원되는 값만 'Regular', 'Spot' 및 'Low'입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="b08ff-202">'일반'은 일반 가상 머신에 대한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="b08ff-203">'Spot'은 스폿 가상 머신에 대한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="b08ff-204">'낮음'은 스폿 가상 머신에도 사용되지만 'Spot'로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="b08ff-205">'낮음' 대신 'Spot'을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b08ff-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="b08ff-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="b08ff-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="b08ff-207">이 확장 집합에 사용할 근접 배치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="b08ff-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="b08ff-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="b08ff-209">롤링 업그레이드 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="b08ff-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="b08ff-210">-ScaleInPolicy</span></span>
<span data-ttu-id="b08ff-211">가상 머신 확장 집합의 크기를 조정하는 경우 따를 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="b08ff-212">가능한 값은 'Default', 'OldestVM' 및 'NewestVM'입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="b08ff-213">가상 머신 확장 집합이 확장될 때 '기본값'은 영역 확장 집합인 경우 먼저 영역 전체에서 확장 집합이 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="b08ff-214">그런 다음, 가능한 한 장애 도메인에서 균형을 맞출 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="b08ff-215">각 장애 도메인 내에서 제거를 위해 선택한 가상 머신은 규모 확장으로부터 보호되지 않는 가장 최근의 가상 머신이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="b08ff-216">가상 머신 확장 집합이 확장되는 경우 'OldestVM'은 규모 확장으로부터 보호되지 않는 가장 오래된 가상 머신을 제거하기 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="b08ff-217">영역 가상 머신 확장 집합의 경우 확장 집합이 먼저 영역 전체에서 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="b08ff-218">각 영역 내에서 보호되지 않는 가장 오래된 가상 머신은 제거를 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="b08ff-219">가상 머신 확장 집합이 확장되는 경우 'NewestVM'은 규모 확장으로부터 보호되지 않는 가장 최근 가상 머신을 제거하기 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="b08ff-220">영역 가상 머신 확장 집합의 경우 확장 집합이 먼저 영역 전체에서 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="b08ff-221">각 영역 내에서 보호되지 않는 가장 새로운 가상 머신은 제거를 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="b08ff-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b08ff-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="b08ff-223">단일 배치 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="b08ff-224">-SkipExtensionsOnOverprovisionedVM</span><span class="sxs-lookup"><span data-stu-id="b08ff-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="b08ff-225">확장이 추가 오버프로비전된 VM에서 실행되지 않는지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="b08ff-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b08ff-226">-SkuCapacity</span></span>
<span data-ttu-id="b08ff-227">VMSS의 인스턴스 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="b08ff-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b08ff-228">-SkuName</span></span>
<span data-ttu-id="b08ff-229">VMSS의 모든 인스턴스의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="b08ff-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b08ff-230">-SkuTier</span></span>
<span data-ttu-id="b08ff-231">VMSS의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="b08ff-232">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="b08ff-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b08ff-233">표준</span><span class="sxs-lookup"><span data-stu-id="b08ff-233">Standard</span></span>
- <span data-ttu-id="b08ff-234">기본</span><span class="sxs-lookup"><span data-stu-id="b08ff-234">Basic</span></span>

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

### <span data-ttu-id="b08ff-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="b08ff-235">-StorageProfile</span></span>
<span data-ttu-id="b08ff-236">VMSS 구성에 대한 디스크 속성을 포함하는 저장소 프로필 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="b08ff-237">**Set-AzVmssStorageProfile** cmdlet을 사용하여 이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="b08ff-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="b08ff-238">-Tag</span></span>
<span data-ttu-id="b08ff-239">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b08ff-240">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="b08ff-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b08ff-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b08ff-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="b08ff-242">이벤트가 자동으로 승인(시간 제한)되기 전에 삭제되는 Virtual Machine을 구성 가능한 기간(분)으로 예약된 이벤트 종료를 승인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="b08ff-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="b08ff-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="b08ff-244">종료 예약된 이벤트 사용</span><span class="sxs-lookup"><span data-stu-id="b08ff-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="b08ff-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="b08ff-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="b08ff-246">확장 집합의 가상 머신에 대한 업그레이드 모드를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="b08ff-247">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="b08ff-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b08ff-248">자동 번역</span><span class="sxs-lookup"><span data-stu-id="b08ff-248">Automatic</span></span>
- <span data-ttu-id="b08ff-249">수동</span><span class="sxs-lookup"><span data-stu-id="b08ff-249">Manual</span></span>

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

### <span data-ttu-id="b08ff-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="b08ff-250">-Zone</span></span>
<span data-ttu-id="b08ff-251">가상 머신 확장 집합에 대한 영역 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="b08ff-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="b08ff-252">-ZoneBalance</span></span>
<span data-ttu-id="b08ff-253">영역이 정전된 경우 X 영역 간 Virtual Machine 배포를 강제로 강제로 적용하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="b08ff-254">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b08ff-254">-Confirm</span></span>
<span data-ttu-id="b08ff-255">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b08ff-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b08ff-256">-WhatIf</span></span>
<span data-ttu-id="b08ff-257">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b08ff-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b08ff-258">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b08ff-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08ff-259">CommonParameters</span></span>
<span data-ttu-id="b08ff-260">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b08ff-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08ff-261">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b08ff-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08ff-262">입력</span><span class="sxs-lookup"><span data-stu-id="b08ff-262">INPUTS</span></span>

### <span data-ttu-id="b08ff-263">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b08ff-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b08ff-264">System.String</span><span class="sxs-lookup"><span data-stu-id="b08ff-264">System.String</span></span>

### <span data-ttu-id="b08ff-265">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b08ff-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b08ff-266">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b08ff-266">System.Int32</span></span>

### <span data-ttu-id="b08ff-267">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b08ff-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b08ff-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="b08ff-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="b08ff-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b08ff-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="b08ff-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="b08ff-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="b08ff-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span><span class="sxs-lookup"><span data-stu-id="b08ff-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="b08ff-272">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b08ff-272">System.String[]</span></span>

### <span data-ttu-id="b08ff-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="b08ff-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="b08ff-274">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b08ff-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b08ff-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b08ff-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="b08ff-276">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b08ff-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b08ff-277">출력</span><span class="sxs-lookup"><span data-stu-id="b08ff-277">OUTPUTS</span></span>

### <span data-ttu-id="b08ff-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b08ff-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b08ff-279">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b08ff-279">NOTES</span></span>

## <span data-ttu-id="b08ff-280">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b08ff-280">RELATED LINKS</span></span>

[<span data-ttu-id="b08ff-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="b08ff-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="b08ff-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b08ff-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="b08ff-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b08ff-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="b08ff-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b08ff-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="b08ff-285">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b08ff-285">New-AzVmss</span></span>](./New-AzVmss.md)
