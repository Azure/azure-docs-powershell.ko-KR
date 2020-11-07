---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 3229f1e09cca1b32b62e5b7233806b20ed8ed78e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711290"
---
# <span data-ttu-id="d6236-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d6236-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="d6236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6236-102">SYNOPSIS</span></span>
<span data-ttu-id="d6236-103">VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6236-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6236-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-AssignIdentity]
 [-IdentityType <ResourceIdentityType>] [-RecoveryPolicyMode <RecoveryMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6236-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d6236-105">DESCRIPTION</span></span>
<span data-ttu-id="d6236-106">**AzureRmVmssConfig** cmdlet은 구성 가능한 vmss (로컬 가상 관리자 배율 집합) 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="d6236-107">VMSS 개체를 구성 하려면 다른 cmdlet이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="d6236-108">이러한 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-108">These cmdlets are:</span></span>

- <span data-ttu-id="d6236-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="d6236-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="d6236-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d6236-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="d6236-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6236-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="d6236-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d6236-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="d6236-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d6236-113">EXAMPLES</span></span>

### <span data-ttu-id="d6236-114">예제 1: VMSS 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="d6236-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="d6236-115">이 예제에서는 VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="d6236-116">첫 번째 명령은 **AzureRmVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="d6236-117">두 번째 명령은 **새 AzureRmVmss** cmdlet을 사용 하 여 첫 번째 명령에서 만든 vmss 구성 개체를 사용 하는 vmss를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="d6236-118">변수</span><span class="sxs-lookup"><span data-stu-id="d6236-118">PARAMETERS</span></span>

### <span data-ttu-id="d6236-119">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="d6236-119">-AssignIdentity</span></span>
<span data-ttu-id="d6236-120">시스템에서 가상 머신 크기 조정 집합에 대해 할당 된 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-120">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6236-121">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="d6236-121">-AutoOSUpgrade</span></span>
<span data-ttu-id="d6236-122">최신 버전의 이미지를 사용할 수 있게 되 면 이동 방식으로 확장 설정 인스턴스에 OS 업그레이드를 자동으로 적용할지 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-122">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6236-123">-부팅 진단</span><span class="sxs-lookup"><span data-stu-id="d6236-123">-BootDiagnostic</span></span>
<span data-ttu-id="d6236-124">가상 컴퓨터 크기 집합 부팅 진단 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-124">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="d6236-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6236-125">-DefaultProfile</span></span>
<span data-ttu-id="d6236-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6236-127">-확장</span><span class="sxs-lookup"><span data-stu-id="d6236-127">-Extension</span></span>
<span data-ttu-id="d6236-128">VMSS에 대 한 확장 정보 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-128">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="d6236-129">**Add-AzureRmVmssExtension** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-129">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="d6236-130">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="d6236-130">-HealthProbeId</span></span>
<span data-ttu-id="d6236-131">가상 컴퓨터 크기 집합에서 인스턴스의 상태를 확인 하는 데 사용 되는 부하 분산 장치 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-131">Specify the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span> <span data-ttu-id="d6236-132">HealthProbeId는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} ' 형식으로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-132">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="d6236-133">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d6236-133">-IdentityType</span></span>
<span data-ttu-id="d6236-134">구성 된 경우 가상 컴퓨터 크기 집합의 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-134">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6236-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d6236-135">-LicenseType</span></span>
<span data-ttu-id="d6236-136">라이선스 종류를 지정 합니다 (사용자 고유의 라이선스 시나리오를 가져오는 데 사용).</span><span class="sxs-lookup"><span data-stu-id="d6236-136">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="d6236-137">-위치</span><span class="sxs-lookup"><span data-stu-id="d6236-137">-Location</span></span>
<span data-ttu-id="d6236-138">VMSS가 만들어지는 Azure 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-138">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="d6236-139">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6236-139">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="d6236-140">VMSS 구성에 대 한 네트워킹 속성을 포함 하는 네트워크 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-140">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="d6236-141">**Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-141">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="d6236-142">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="d6236-142">-OsProfile</span></span>
<span data-ttu-id="d6236-143">VMSS 구성에 대 한 운영 체제 속성을 포함 하는 운영 체제 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-143">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="d6236-144">**Set-AzureRmVmssOsProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-144">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="d6236-145">-과잉 프로비저닝</span><span class="sxs-lookup"><span data-stu-id="d6236-145">-Overprovision</span></span>
<span data-ttu-id="d6236-146">Cmdlet이 VMSS를 프로 비전 하 고 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-146">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="d6236-147">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="d6236-147">-PlanName</span></span>
<span data-ttu-id="d6236-148">계획 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-148">Specifies the plan name.</span></span>

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

### <span data-ttu-id="d6236-149">계획 제품</span><span class="sxs-lookup"><span data-stu-id="d6236-149">-PlanProduct</span></span>
<span data-ttu-id="d6236-150">계획 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-150">Specifies the plan product.</span></span>

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

### <span data-ttu-id="d6236-151">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="d6236-151">-PlanPromotionCode</span></span>
<span data-ttu-id="d6236-152">계획 프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-152">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="d6236-153">-계획 Publisher</span><span class="sxs-lookup"><span data-stu-id="d6236-153">-PlanPublisher</span></span>
<span data-ttu-id="d6236-154">계획 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-154">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="d6236-155">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="d6236-155">-RecoveryPolicyMode</span></span>
<span data-ttu-id="d6236-156">복구 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-156">Specify the recovery policy.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Compute.Automation.RecoveryMode]
Parameter Sets: (All)
Aliases: 
Accepted values: None, OverProvision, Reprovision

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6236-157">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="d6236-157">-RollingUpgradePolicy</span></span>
<span data-ttu-id="d6236-158">롤링 업그레이드 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-158">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="d6236-159">-Single배치 그룹</span><span class="sxs-lookup"><span data-stu-id="d6236-159">-SinglePlacementGroup</span></span>
<span data-ttu-id="d6236-160">단일 배치 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-160">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="d6236-161">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d6236-161">-SkuCapacity</span></span>
<span data-ttu-id="d6236-162">VMSS의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-162">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6236-163">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="d6236-163">-SkuName</span></span>
<span data-ttu-id="d6236-164">VMSS의 모든 인스턴스 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-164">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="d6236-165">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="d6236-165">-SkuTier</span></span>
<span data-ttu-id="d6236-166">VMSS의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-166">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="d6236-167">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d6236-168">표준이</span><span class="sxs-lookup"><span data-stu-id="d6236-168">Standard</span></span>
- <span data-ttu-id="d6236-169">기본적</span><span class="sxs-lookup"><span data-stu-id="d6236-169">Basic</span></span>

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

### <span data-ttu-id="d6236-170">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="d6236-170">-StorageProfile</span></span>
<span data-ttu-id="d6236-171">VMSS 구성의 디스크 속성이 포함 된 저장소 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-171">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="d6236-172">**Set-AzureRmVmssStorageProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-172">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="d6236-173">태그</span><span class="sxs-lookup"><span data-stu-id="d6236-173">-Tag</span></span>
<span data-ttu-id="d6236-174">VMSS에 할당 될 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-174">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="d6236-175">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="d6236-175">-UpgradePolicyMode</span></span>
<span data-ttu-id="d6236-176">확장 집합의 가상 컴퓨터로 업그레이드 모드를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-176">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="d6236-177">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-177">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d6236-178">자동 번역</span><span class="sxs-lookup"><span data-stu-id="d6236-178">Automatic</span></span>
- <span data-ttu-id="d6236-179">수동</span><span class="sxs-lookup"><span data-stu-id="d6236-179">Manual</span></span>

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

### <span data-ttu-id="d6236-180">-Zone</span><span class="sxs-lookup"><span data-stu-id="d6236-180">-Zone</span></span>
<span data-ttu-id="d6236-181">가상 컴퓨터 크기 집합에 대 한 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-181">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d6236-182">-확인</span><span class="sxs-lookup"><span data-stu-id="d6236-182">-Confirm</span></span>
<span data-ttu-id="d6236-183">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6236-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6236-184">-WhatIf</span></span>
<span data-ttu-id="d6236-185">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-185">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6236-186">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6236-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6236-187">CommonParameters</span></span>
<span data-ttu-id="d6236-188">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6236-189">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6236-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6236-190">입력</span><span class="sxs-lookup"><span data-stu-id="d6236-190">INPUTS</span></span>

## <span data-ttu-id="d6236-191">출력</span><span class="sxs-lookup"><span data-stu-id="d6236-191">OUTPUTS</span></span>

### <span data-ttu-id="d6236-192">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6236-192">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d6236-193">상속자</span><span class="sxs-lookup"><span data-stu-id="d6236-193">NOTES</span></span>

## <span data-ttu-id="d6236-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6236-194">RELATED LINKS</span></span>

[<span data-ttu-id="d6236-195">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="d6236-195">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="d6236-196">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d6236-196">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="d6236-197">추가-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6236-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="d6236-198">추가-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d6236-198">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="d6236-199">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d6236-199">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


