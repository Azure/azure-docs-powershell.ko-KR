---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 4b87c121368232769672c24bc5005f3a50bfd39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529015"
---
# <span data-ttu-id="31c4b-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="31c4b-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="31c4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="31c4b-103">VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31c4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31c4b-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-PlanName <String>]
 [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RecoveryPolicyMode <RecoveryMode>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-IdentityType <ResourceIdentityType>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31c4b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31c4b-105">DESCRIPTION</span></span>
<span data-ttu-id="31c4b-106">**AzureRmVmssConfig** cmdlet은 구성 가능한 vmss (로컬 가상 관리자 배율 집합) 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="31c4b-107">VMSS 개체를 구성 하려면 다른 cmdlet이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="31c4b-108">이러한 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-108">These cmdlets are:</span></span>

- <span data-ttu-id="31c4b-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="31c4b-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="31c4b-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="31c4b-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="31c4b-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="31c4b-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="31c4b-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="31c4b-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="31c4b-113">예제의</span><span class="sxs-lookup"><span data-stu-id="31c4b-113">EXAMPLES</span></span>

### <span data-ttu-id="31c4b-114">예제 1: VMSS 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="31c4b-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="31c4b-115">이 예제에서는 VMSS 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="31c4b-116">첫 번째 명령은 **AzureRmVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="31c4b-117">두 번째 명령은 **새 AzureRmVmss** cmdlet을 사용 하 여 첫 번째 명령에서 만든 vmss 구성 개체를 사용 하는 vmss를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="31c4b-118">변수</span><span class="sxs-lookup"><span data-stu-id="31c4b-118">PARAMETERS</span></span>

### <span data-ttu-id="31c4b-119">-부팅 진단</span><span class="sxs-lookup"><span data-stu-id="31c4b-119">-BootDiagnostic</span></span>
<span data-ttu-id="31c4b-120">가상 컴퓨터 크기 집합 부팅 진단 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-120">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="31c4b-121">-확장</span><span class="sxs-lookup"><span data-stu-id="31c4b-121">-Extension</span></span>
<span data-ttu-id="31c4b-122">VMSS에 대 한 확장 정보 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-122">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="31c4b-123">**Add-AzureRmVmssExtension** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-123">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="31c4b-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="31c4b-124">-IdentityType</span></span>
<span data-ttu-id="31c4b-125">구성 된 경우 가상 컴퓨터 크기 집합의 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-125">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c4b-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="31c4b-126">-LicenseType</span></span>
<span data-ttu-id="31c4b-127">라이선스 종류를 지정 합니다 (사용자 고유의 라이선스 시나리오를 가져오는 데 사용).</span><span class="sxs-lookup"><span data-stu-id="31c4b-127">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="31c4b-128">-위치</span><span class="sxs-lookup"><span data-stu-id="31c4b-128">-Location</span></span>
<span data-ttu-id="31c4b-129">VMSS가 만들어지는 Azure 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-129">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="31c4b-130">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="31c4b-130">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="31c4b-131">VMSS 구성에 대 한 네트워킹 속성을 포함 하는 네트워크 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-131">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="31c4b-132">**Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-132">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="31c4b-133">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="31c4b-133">-OsProfile</span></span>
<span data-ttu-id="31c4b-134">VMSS 구성에 대 한 운영 체제 속성을 포함 하는 운영 체제 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-134">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="31c4b-135">**Set-AzureRmVmssOsProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-135">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="31c4b-136">-과잉 프로비저닝</span><span class="sxs-lookup"><span data-stu-id="31c4b-136">-Overprovision</span></span>
<span data-ttu-id="31c4b-137">Cmdlet이 VMSS를 프로 비전 하 고 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-137">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="31c4b-138">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="31c4b-138">-PlanName</span></span>
<span data-ttu-id="31c4b-139">계획 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-139">Specifies the plan name.</span></span>

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

### <span data-ttu-id="31c4b-140">계획 제품</span><span class="sxs-lookup"><span data-stu-id="31c4b-140">-PlanProduct</span></span>
<span data-ttu-id="31c4b-141">계획 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-141">Specifies the plan product.</span></span>

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

### <span data-ttu-id="31c4b-142">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="31c4b-142">-PlanPromotionCode</span></span>
<span data-ttu-id="31c4b-143">계획 프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-143">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="31c4b-144">-계획 Publisher</span><span class="sxs-lookup"><span data-stu-id="31c4b-144">-PlanPublisher</span></span>
<span data-ttu-id="31c4b-145">계획 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-145">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="31c4b-146">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="31c4b-146">-RecoveryPolicyMode</span></span>
<span data-ttu-id="31c4b-147">복구 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-147">Specify the recovery policy.</span></span>

```yaml
Type: RecoveryMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c4b-148">-Single배치 그룹</span><span class="sxs-lookup"><span data-stu-id="31c4b-148">-SinglePlacementGroup</span></span>
<span data-ttu-id="31c4b-149">단일 배치 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-149">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="31c4b-150">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="31c4b-150">-SkuCapacity</span></span>
<span data-ttu-id="31c4b-151">VMSS의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-151">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c4b-152">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="31c4b-152">-SkuName</span></span>
<span data-ttu-id="31c4b-153">VMSS의 모든 인스턴스 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-153">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="31c4b-154">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="31c4b-154">-SkuTier</span></span>
<span data-ttu-id="31c4b-155">VMSS의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-155">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="31c4b-156">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31c4b-157">표준이</span><span class="sxs-lookup"><span data-stu-id="31c4b-157">Standard</span></span>
- <span data-ttu-id="31c4b-158">기본적</span><span class="sxs-lookup"><span data-stu-id="31c4b-158">Basic</span></span>

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

### <span data-ttu-id="31c4b-159">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="31c4b-159">-StorageProfile</span></span>
<span data-ttu-id="31c4b-160">VMSS 구성의 디스크 속성이 포함 된 저장소 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-160">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="31c4b-161">**Set-AzureRmVmssStorageProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-161">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="31c4b-162">태그</span><span class="sxs-lookup"><span data-stu-id="31c4b-162">-Tag</span></span>
<span data-ttu-id="31c4b-163">VMSS에 할당 될 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-163">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="31c4b-164">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="31c4b-164">-UpgradePolicyMode</span></span>
<span data-ttu-id="31c4b-165">확장 집합의 가상 컴퓨터로 업그레이드 모드를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-165">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="31c4b-166">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31c4b-167">자동 번역</span><span class="sxs-lookup"><span data-stu-id="31c4b-167">Automatic</span></span>
- <span data-ttu-id="31c4b-168">수동</span><span class="sxs-lookup"><span data-stu-id="31c4b-168">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c4b-169">-확인</span><span class="sxs-lookup"><span data-stu-id="31c4b-169">-Confirm</span></span>
<span data-ttu-id="31c4b-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31c4b-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31c4b-171">-WhatIf</span></span>
<span data-ttu-id="31c4b-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31c4b-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31c4b-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c4b-174">CommonParameters</span></span>
<span data-ttu-id="31c4b-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c4b-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31c4b-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c4b-177">입력</span><span class="sxs-lookup"><span data-stu-id="31c4b-177">INPUTS</span></span>

### <span data-ttu-id="31c4b-178">않아야</span><span class="sxs-lookup"><span data-stu-id="31c4b-178">None</span></span>
<span data-ttu-id="31c4b-179">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31c4b-180">출력</span><span class="sxs-lookup"><span data-stu-id="31c4b-180">OUTPUTS</span></span>

### <span data-ttu-id="31c4b-181">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31c4b-181">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="31c4b-182">상속자</span><span class="sxs-lookup"><span data-stu-id="31c4b-182">NOTES</span></span>

## <span data-ttu-id="31c4b-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31c4b-183">RELATED LINKS</span></span>

[<span data-ttu-id="31c4b-184">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="31c4b-184">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="31c4b-185">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="31c4b-185">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="31c4b-186">추가-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="31c4b-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="31c4b-187">추가-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="31c4b-187">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="31c4b-188">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="31c4b-188">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


