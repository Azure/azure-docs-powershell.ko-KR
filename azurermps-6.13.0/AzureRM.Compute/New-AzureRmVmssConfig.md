---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: ee18925960b7f2afd9e35250a3cc33a5bd16e073
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528586"
---
# <span data-ttu-id="88359-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="88359-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="88359-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88359-102">SYNOPSIS</span></span>
<span data-ttu-id="88359-103">VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88359-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88359-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88359-104">SYNTAX</span></span>

### <span data-ttu-id="88359-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="88359-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88359-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="88359-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88359-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="88359-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88359-108">설명은</span><span class="sxs-lookup"><span data-stu-id="88359-108">DESCRIPTION</span></span>
<span data-ttu-id="88359-109">**AzureRmVmssConfig** cmdlet은 구성 가능한 vmss (로컬 가상 관리자 배율 집합) 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88359-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="88359-110">VMSS 개체를 구성 하려면 다른 cmdlet이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="88359-111">이러한 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-111">These cmdlets are:</span></span>
- <span data-ttu-id="88359-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="88359-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="88359-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="88359-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="88359-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="88359-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="88359-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="88359-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="88359-116">예제의</span><span class="sxs-lookup"><span data-stu-id="88359-116">EXAMPLES</span></span>

### <span data-ttu-id="88359-117">예제 1: VMSS 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="88359-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="88359-118">이 예제에서는 VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88359-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="88359-119">첫 번째 명령은 **AzureRmVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="88359-120">두 번째 명령은 **새 AzureRmVmss** cmdlet을 사용 하 여 첫 번째 명령에서 만든 vmss 구성 개체를 사용 하는 vmss를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88359-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="88359-121">변수</span><span class="sxs-lookup"><span data-stu-id="88359-121">PARAMETERS</span></span>

### <span data-ttu-id="88359-122">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="88359-122">-AssignIdentity</span></span>
<span data-ttu-id="88359-123">시스템에서 가상 머신 크기 조정 집합에 대해 할당 된 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88359-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="88359-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="88359-125">최신 버전의 이미지를 사용할 수 있게 되 면 이동 방식으로 확장 설정 인스턴스에 OS 업그레이드를 자동으로 적용할지 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="88359-126">-부팅 진단</span><span class="sxs-lookup"><span data-stu-id="88359-126">-BootDiagnostic</span></span>
<span data-ttu-id="88359-127">가상 컴퓨터 크기 집합 부팅 진단 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="88359-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88359-128">-DefaultProfile</span></span>
<span data-ttu-id="88359-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88359-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88359-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="88359-130">-DisableAutoRollback</span></span>
<span data-ttu-id="88359-131">자동 OS 업그레이드 정책에 대 한 자동 롤백 해제</span><span class="sxs-lookup"><span data-stu-id="88359-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="88359-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="88359-132">-EnableUltraSSD</span></span>
<span data-ttu-id="88359-133">하나 이상의 관리 되는 데이터 디스크를 가상 컴퓨터 크기 집합의 UltraSSD_LRS 저장소 계정 형식으로 한 개 이상 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="88359-134">저장소 계정 유형이 UltraSSD_LRS 관리 디스크는이 속성을 사용 하도록 설정 된 경우에만 VMSS에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="88359-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="88359-135">-EvictionPolicy</span></span>
<span data-ttu-id="88359-136">확장 집합의 가상 컴퓨터에 대 한 제거 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="88359-137">-확장</span><span class="sxs-lookup"><span data-stu-id="88359-137">-Extension</span></span>
<span data-ttu-id="88359-138">VMSS에 대 한 확장 정보 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="88359-139">**Add-AzureRmVmssExtension** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-139">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88359-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="88359-140">-HealthProbeId</span></span>
<span data-ttu-id="88359-141">가상 컴퓨터 크기 집합에서 인스턴스의 상태를 확인 하는 데 사용 되는 부하 분산 장치 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="88359-142">HealthProbeId는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} ' 형식으로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="88359-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="88359-143">-IdentityId</span></span>
<span data-ttu-id="88359-144">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="88359-145">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="88359-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="88359-146">-IdentityType</span></span>
<span data-ttu-id="88359-147">가상 컴퓨터 크기 집합에 사용 되는 id 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="88359-148">' SystemAssignedUserAssigned ' 형식에는 암시적으로 만든 id와 사용자가 할당 한 id 집합이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88359-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="88359-149">' 없음 ' 형식은 가상 컴퓨터 배율 집합에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="88359-150">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88359-151">지정 된 SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="88359-151">SystemAssigned</span></span>
- <span data-ttu-id="88359-152">UserAssigned 됨</span><span class="sxs-lookup"><span data-stu-id="88359-152">UserAssigned</span></span>
- <span data-ttu-id="88359-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="88359-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="88359-154">않아야</span><span class="sxs-lookup"><span data-stu-id="88359-154">None</span></span>

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

### <span data-ttu-id="88359-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="88359-155">-LicenseType</span></span>
<span data-ttu-id="88359-156">라이선스 종류를 지정 합니다 (사용자 고유의 라이선스 시나리오를 가져오는 데 사용).</span><span class="sxs-lookup"><span data-stu-id="88359-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="88359-157">-위치</span><span class="sxs-lookup"><span data-stu-id="88359-157">-Location</span></span>
<span data-ttu-id="88359-158">VMSS가 만들어지는 Azure 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="88359-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="88359-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="88359-160">VMSS 구성에 대 한 네트워킹 속성을 포함 하는 네트워크 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="88359-161">**Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-161">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="88359-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="88359-162">-OsProfile</span></span>
<span data-ttu-id="88359-163">VMSS 구성에 대 한 운영 체제 속성을 포함 하는 운영 체제 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="88359-164">**Set-AzureRmVmssOsProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-164">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="88359-165">-과잉 프로비저닝</span><span class="sxs-lookup"><span data-stu-id="88359-165">-Overprovision</span></span>
<span data-ttu-id="88359-166">Cmdlet이 VMSS를 프로 비전 하 고 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="88359-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="88359-167">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="88359-167">-PlanName</span></span>
<span data-ttu-id="88359-168">계획 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="88359-169">계획 제품</span><span class="sxs-lookup"><span data-stu-id="88359-169">-PlanProduct</span></span>
<span data-ttu-id="88359-170">계획 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="88359-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="88359-171">-PlanPromotionCode</span></span>
<span data-ttu-id="88359-172">계획 프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="88359-173">-계획 Publisher</span><span class="sxs-lookup"><span data-stu-id="88359-173">-PlanPublisher</span></span>
<span data-ttu-id="88359-174">계획 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="88359-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="88359-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="88359-176">각 배치 그룹의 오류 도메인 수입니다.</span><span class="sxs-lookup"><span data-stu-id="88359-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="88359-177">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="88359-177">-Priority</span></span>
<span data-ttu-id="88359-178">확장 집합의 가상 컴퓨터에 대 한 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="88359-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="88359-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="88359-180">롤링 업그레이드 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="88359-181">-Single배치 그룹</span><span class="sxs-lookup"><span data-stu-id="88359-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="88359-182">단일 배치 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="88359-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="88359-183">-SkuCapacity</span></span>
<span data-ttu-id="88359-184">VMSS의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="88359-185">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="88359-185">-SkuName</span></span>
<span data-ttu-id="88359-186">VMSS의 모든 인스턴스 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="88359-187">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="88359-187">-SkuTier</span></span>
<span data-ttu-id="88359-188">VMSS의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="88359-189">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88359-190">표준이</span><span class="sxs-lookup"><span data-stu-id="88359-190">Standard</span></span>
- <span data-ttu-id="88359-191">기본적</span><span class="sxs-lookup"><span data-stu-id="88359-191">Basic</span></span>

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

### <span data-ttu-id="88359-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="88359-192">-StorageProfile</span></span>
<span data-ttu-id="88359-193">VMSS 구성의 디스크 속성이 포함 된 저장소 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="88359-194">**Set-AzureRmVmssStorageProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-194">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="88359-195">태그</span><span class="sxs-lookup"><span data-stu-id="88359-195">-Tag</span></span>
<span data-ttu-id="88359-196">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="88359-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="88359-197">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="88359-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="88359-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="88359-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="88359-199">확장 집합의 가상 컴퓨터로 업그레이드 모드를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="88359-200">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88359-201">자동 번역</span><span class="sxs-lookup"><span data-stu-id="88359-201">Automatic</span></span>
- <span data-ttu-id="88359-202">수동</span><span class="sxs-lookup"><span data-stu-id="88359-202">Manual</span></span>

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

### <span data-ttu-id="88359-203">-Zone</span><span class="sxs-lookup"><span data-stu-id="88359-203">-Zone</span></span>
<span data-ttu-id="88359-204">가상 컴퓨터 크기 집합에 대 한 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="88359-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="88359-205">-ZoneBalance</span></span>
<span data-ttu-id="88359-206">영역 작동이 중단 되는 경우를 대비 하 여 가상 컴퓨터 배포 교차 x 영역을 강제 적용할지 여부</span><span class="sxs-lookup"><span data-stu-id="88359-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="88359-207">-확인</span><span class="sxs-lookup"><span data-stu-id="88359-207">-Confirm</span></span>
<span data-ttu-id="88359-208">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88359-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88359-209">-WhatIf</span></span>
<span data-ttu-id="88359-210">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="88359-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88359-211">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88359-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88359-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88359-212">CommonParameters</span></span>
<span data-ttu-id="88359-213">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88359-214">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88359-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88359-215">입력</span><span class="sxs-lookup"><span data-stu-id="88359-215">INPUTS</span></span>

### <span data-ttu-id="88359-216">시스템 Null 허용 ' 1 [[b77a5c561934e089] [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="88359-216">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="88359-217">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88359-217">System.String</span></span>

### <span data-ttu-id="88359-218">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="88359-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="88359-219">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="88359-219">System.Int32</span></span>

### <span data-ttu-id="88359-220">시스템 Null 허용 ' 1 [[21.0.0.0]. UpgradeMode, Microsoft Azure. 관리., Version = 31bf3856ad364e35, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="88359-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="88359-221">VirtualMachineScaleSetOSProfile를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="88359-222">VirtualMachineScaleSetStorageProfile를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="88359-223">Microsoft VirtualMachineScaleSetNetworkConfiguration []을 (를)</span><span class="sxs-lookup"><span data-stu-id="88359-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="88359-224">Microsoft VirtualMachineScaleSetExtension []을 (를)</span><span class="sxs-lookup"><span data-stu-id="88359-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="88359-225">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="88359-225">System.String[]</span></span>

### <span data-ttu-id="88359-226">RollingUpgradePolicy를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="88359-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="88359-227">Microsoft. Azure. 관리자. 부팅 진단</span><span class="sxs-lookup"><span data-stu-id="88359-227">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="88359-228">시스템 Null 허용 ' 1 [[ResourceIdentityType, Microsoft azure. 21.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="88359-228">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="88359-229">출력</span><span class="sxs-lookup"><span data-stu-id="88359-229">OUTPUTS</span></span>

### <span data-ttu-id="88359-230">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="88359-230">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="88359-231">상속자</span><span class="sxs-lookup"><span data-stu-id="88359-231">NOTES</span></span>

## <span data-ttu-id="88359-232">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88359-232">RELATED LINKS</span></span>

[<span data-ttu-id="88359-233">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="88359-233">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="88359-234">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="88359-234">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="88359-235">추가-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="88359-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="88359-236">추가-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="88359-236">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="88359-237">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="88359-237">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)
