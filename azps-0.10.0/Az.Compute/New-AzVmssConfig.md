---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: c407ce7147d3eb175fc181b76b140605e463d9a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876988"
---
# <span data-ttu-id="e7384-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e7384-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="e7384-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7384-102">SYNOPSIS</span></span>
<span data-ttu-id="e7384-103">VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="e7384-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7384-104">SYNTAX</span></span>

### <span data-ttu-id="e7384-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e7384-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7384-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7384-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7384-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7384-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7384-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e7384-108">DESCRIPTION</span></span>
<span data-ttu-id="e7384-109">**AzVmssConfig** cmdlet은 구성 가능한 vmss (로컬 가상 관리자 배율 집합) 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="e7384-110">VMSS 개체를 구성 하려면 다른 cmdlet이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="e7384-111">이러한 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-111">These cmdlets are:</span></span>

- <span data-ttu-id="e7384-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="e7384-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="e7384-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="e7384-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="e7384-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7384-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="e7384-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="e7384-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="e7384-116">예제의</span><span class="sxs-lookup"><span data-stu-id="e7384-116">EXAMPLES</span></span>

### <span data-ttu-id="e7384-117">예제 1: VMSS 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="e7384-117">Example 1: Create a VMSS configuration object</span></span>
```
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

<span data-ttu-id="e7384-118">이 예제에서는 VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="e7384-119">첫 번째 명령은 **AzVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="e7384-120">두 번째 명령은 **새 AzVmss** cmdlet을 사용 하 여 첫 번째 명령에서 만든 vmss 구성 개체를 사용 하는 vmss를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="e7384-121">변수</span><span class="sxs-lookup"><span data-stu-id="e7384-121">PARAMETERS</span></span>

### <span data-ttu-id="e7384-122">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="e7384-122">-AssignIdentity</span></span>
<span data-ttu-id="e7384-123">시스템에서 가상 머신 크기 조정 집합에 대해 할당 된 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="e7384-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="e7384-125">최신 버전의 이미지를 사용할 수 있게 되 면 이동 방식으로 확장 설정 인스턴스에 OS 업그레이드를 자동으로 적용할지 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="e7384-126">-부팅 진단</span><span class="sxs-lookup"><span data-stu-id="e7384-126">-BootDiagnostic</span></span>
<span data-ttu-id="e7384-127">가상 컴퓨터 크기 집합 부팅 진단 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7384-128">-DefaultProfile</span></span>
<span data-ttu-id="e7384-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7384-130">-확장</span><span class="sxs-lookup"><span data-stu-id="e7384-130">-Extension</span></span>
<span data-ttu-id="e7384-131">VMSS에 대 한 확장 정보 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="e7384-132">**Add-AzVmssExtension** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-132">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="e7384-133">-HealthProbeId</span></span>
<span data-ttu-id="e7384-134">가상 컴퓨터 크기 집합에서 인스턴스의 상태를 확인 하는 데 사용 되는 부하 분산 장치 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="e7384-135">HealthProbeId는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} ' 형식으로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-136">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="e7384-136">-IdentityId</span></span>
<span data-ttu-id="e7384-137">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="e7384-138">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e7384-139">-IdentityType</span></span>
<span data-ttu-id="e7384-140">가상 컴퓨터 크기 집합에 사용 되는 id 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="e7384-141">' SystemAssignedUserAssigned ' 형식에는 암시적으로 만든 id와 사용자가 할당 한 id 집합이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="e7384-142">' 없음 ' 형식은 가상 컴퓨터 배율 집합에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="e7384-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7384-144">지정 된 SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="e7384-144">SystemAssigned</span></span>
- <span data-ttu-id="e7384-145">UserAssigned 됨</span><span class="sxs-lookup"><span data-stu-id="e7384-145">UserAssigned</span></span>
- <span data-ttu-id="e7384-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="e7384-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="e7384-147">않아야</span><span class="sxs-lookup"><span data-stu-id="e7384-147">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e7384-148">-LicenseType</span></span>
<span data-ttu-id="e7384-149">라이선스 종류를 지정 합니다 (사용자 고유의 라이선스 시나리오를 가져오는 데 사용).</span><span class="sxs-lookup"><span data-stu-id="e7384-149">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-150">-위치</span><span class="sxs-lookup"><span data-stu-id="e7384-150">-Location</span></span>
<span data-ttu-id="e7384-151">VMSS가 만들어지는 Azure 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-151">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7384-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="e7384-153">VMSS 구성에 대 한 네트워킹 속성을 포함 하는 네트워크 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="e7384-154">**Add-AzVmssNetworkInterfaceConfiguration** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-154">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="e7384-155">-OsProfile</span></span>
<span data-ttu-id="e7384-156">VMSS 구성에 대 한 운영 체제 속성을 포함 하는 운영 체제 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="e7384-157">**Set-AzVmssOsProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-157">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-158">-과잉 프로비저닝</span><span class="sxs-lookup"><span data-stu-id="e7384-158">-Overprovision</span></span>
<span data-ttu-id="e7384-159">Cmdlet이 VMSS를 프로 비전 하 고 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-160">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="e7384-160">-PlanName</span></span>
<span data-ttu-id="e7384-161">계획 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-161">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-162">계획 제품</span><span class="sxs-lookup"><span data-stu-id="e7384-162">-PlanProduct</span></span>
<span data-ttu-id="e7384-163">계획 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-163">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="e7384-164">-PlanPromotionCode</span></span>
<span data-ttu-id="e7384-165">계획 프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-165">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-166">-계획 Publisher</span><span class="sxs-lookup"><span data-stu-id="e7384-166">-PlanPublisher</span></span>
<span data-ttu-id="e7384-167">계획 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-167">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-168">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="e7384-168">-Priority</span></span>
<span data-ttu-id="e7384-169">확장 집합의 가상 컴퓨터에 대 한 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-169">Specifies the priority for the virtual machines in the scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="e7384-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="e7384-171">롤링 업그레이드 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-171">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: RollingUpgradePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-172">-Single배치 그룹</span><span class="sxs-lookup"><span data-stu-id="e7384-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="e7384-173">단일 배치 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-173">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e7384-174">-SkuCapacity</span></span>
<span data-ttu-id="e7384-175">VMSS의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-175">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-176">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="e7384-176">-SkuName</span></span>
<span data-ttu-id="e7384-177">VMSS의 모든 인스턴스 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-177">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-178">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="e7384-178">-SkuTier</span></span>
<span data-ttu-id="e7384-179">VMSS의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="e7384-180">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7384-181">표준이</span><span class="sxs-lookup"><span data-stu-id="e7384-181">Standard</span></span>
- <span data-ttu-id="e7384-182">기본적</span><span class="sxs-lookup"><span data-stu-id="e7384-182">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="e7384-183">-StorageProfile</span></span>
<span data-ttu-id="e7384-184">VMSS 구성의 디스크 속성이 포함 된 저장소 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="e7384-185">**Set-AzVmssStorageProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-185">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-186">태그</span><span class="sxs-lookup"><span data-stu-id="e7384-186">-Tag</span></span>
<span data-ttu-id="e7384-187">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e7384-188">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="e7384-188">For example:</span></span>

<span data-ttu-id="e7384-189">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e7384-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="e7384-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="e7384-191">확장 집합의 가상 컴퓨터로 업그레이드 모드를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="e7384-192">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7384-193">자동 번역</span><span class="sxs-lookup"><span data-stu-id="e7384-193">Automatic</span></span>
- <span data-ttu-id="e7384-194">수동</span><span class="sxs-lookup"><span data-stu-id="e7384-194">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-195">-Zone</span><span class="sxs-lookup"><span data-stu-id="e7384-195">-Zone</span></span>
<span data-ttu-id="e7384-196">가상 컴퓨터 크기 집합에 대 한 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-196">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7384-197">-확인</span><span class="sxs-lookup"><span data-stu-id="e7384-197">-Confirm</span></span>
<span data-ttu-id="e7384-198">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-198">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7384-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7384-199">-WhatIf</span></span>
<span data-ttu-id="e7384-200">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7384-201">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-201">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7384-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7384-202">CommonParameters</span></span>
<span data-ttu-id="e7384-203">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7384-204">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7384-204">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7384-205">입력</span><span class="sxs-lookup"><span data-stu-id="e7384-205">INPUTS</span></span>

### <span data-ttu-id="e7384-206">않아야</span><span class="sxs-lookup"><span data-stu-id="e7384-206">None</span></span>
<span data-ttu-id="e7384-207">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7384-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e7384-208">출력</span><span class="sxs-lookup"><span data-stu-id="e7384-208">OUTPUTS</span></span>

### <span data-ttu-id="e7384-209">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="e7384-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e7384-210">상속자</span><span class="sxs-lookup"><span data-stu-id="e7384-210">NOTES</span></span>

## <span data-ttu-id="e7384-211">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7384-211">RELATED LINKS</span></span>

[<span data-ttu-id="e7384-212">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="e7384-212">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="e7384-213">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="e7384-213">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="e7384-214">추가-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7384-214">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="e7384-215">추가-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="e7384-215">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="e7384-216">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="e7384-216">New-AzVmss</span></span>](./New-AzVmss.md)
