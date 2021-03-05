---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: fbdefd7e80e0054bbef8e12614316f7b23ff134a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015392"
---
# <span data-ttu-id="9f090-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f090-101">Update-AzVmss</span></span>

## <span data-ttu-id="9f090-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f090-102">SYNOPSIS</span></span>
<span data-ttu-id="9f090-103">VMSS의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="9f090-104">구문</span><span class="sxs-lookup"><span data-stu-id="9f090-104">SYNTAX</span></span>

### <span data-ttu-id="9f090-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="9f090-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f090-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f090-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f090-107">설명</span><span class="sxs-lookup"><span data-stu-id="9f090-107">DESCRIPTION</span></span>
<span data-ttu-id="9f090-108">**Update-AzVmss** cmdlet은 VMSS(Virtual Machine Scale Set) 상태를 로컬 VMSS 개체의 상태로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="9f090-109">예제</span><span class="sxs-lookup"><span data-stu-id="9f090-109">EXAMPLES</span></span>

### <span data-ttu-id="9f090-110">예제 1: VMSS의 상태를 로컬 VMSS 개체의 상태로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="9f090-111">이 명령은 그룹001이라는 리소스 그룹에 속하는 VMSS001이라는 VMSS의 상태를 로컬 VMSS 개체의 상태로 $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="9f090-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="9f090-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9f090-112">PARAMETERS</span></span>

### <span data-ttu-id="9f090-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f090-113">-AsJob</span></span>
<span data-ttu-id="9f090-114">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9f090-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="9f090-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="9f090-116">최신 버전의 이미지를 사용할 수 있을 때 롤링 스타일로 집합 인스턴스의 크기 조정에 OS 업그레이드를 자동으로 적용해야 하는지 여부를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="9f090-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="9f090-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="9f090-118">VM의 상태 변경으로 인해 자동 복구가 일시 중단되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="9f090-119">상태 변경이 완료된 후에 유예 시간이 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="9f090-120">이렇게 하면 조기 또는 우발적 복구를 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="9f090-121">시간 기간은 ISO 8601 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="9f090-122">허용되는 최소 유예 기간은 PT30M(30분)입니다. 이는 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="9f090-123">허용되는 최대 유예 기간은 90분(PT90M)입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="9f090-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="9f090-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="9f090-125">가상 머신 확장 집합에서 부팅 진단을 사용하도록 설정해야 하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="9f090-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="9f090-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="9f090-127">콘솔 출력 및 스크린샷을 배치하는 데 사용할 저장소 계정의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="9f090-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="9f090-128">-CustomData</span></span>
<span data-ttu-id="9f090-129">사용자 지정 데이터의 base-64 인코딩된 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="9f090-130">가상 머신의 파일로 저장되는 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="9f090-131">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="9f090-132">VM에 클라우드-init를 사용하는 경우 만들기 중에 [Cloud-init를 사용하여 Linux VM을 사용자 지정하는 방법을 참조합니다.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="9f090-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="9f090-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f090-133">-DefaultProfile</span></span>
<span data-ttu-id="9f090-134">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f090-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="9f090-135">-DisableAutoRollback</span></span>
<span data-ttu-id="9f090-136">자동 OS 업그레이드 정책에 대한 자동 롤백 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="9f090-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="9f090-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="9f090-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="9f090-138">이 cmdlet은 Linux OS에 대한 암호 인증을 사용하지 않도록 설정하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="9f090-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="9f090-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="9f090-140">가상 머신 확장 집합에서 자동 복구를 사용하도록 설정하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="9f090-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="9f090-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="9f090-142">VMSS의 Windows 가상 머신이 자동 업데이트를 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="9f090-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="9f090-143">-EncryptionAtHost</span></span>
<span data-ttu-id="9f090-144">이 매개 변수는 요청에서 사용자가 가상 머신 확장 집합에 대한 호스트 암호화를 사용하도록 설정하거나 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="9f090-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="9f090-145">-IdentityId</span></span>
<span data-ttu-id="9f090-146">가상 머신 확장 집합과 연결된 사용자 ID 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="9f090-147">사용자 ARM ID 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' 형식의 리소스 ID로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9f090-148">-IdentityType</span></span>
<span data-ttu-id="9f090-149">가상 머신 확장 집합에 사용되는 ID 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="9f090-150">'SystemAssignedUserAssigned' 형식에는 암시적으로 만든 ID와 사용자 할당 ID 집합이 모두 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="9f090-151">'None' 형식은 가상 머신 확장 집합에서 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="9f090-152">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f090-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="9f090-153">SystemAssigned</span></span>
- <span data-ttu-id="9f090-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="9f090-154">UserAssigned</span></span>
- <span data-ttu-id="9f090-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="9f090-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="9f090-156">없음</span><span class="sxs-lookup"><span data-stu-id="9f090-156">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="9f090-157">-ImageReferenceId</span></span>
<span data-ttu-id="9f090-158">이미지 참조 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="9f090-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="9f090-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="9f090-160">VMImage(가상 머신 이미지) 제품 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="9f090-161">이미지 제안을 얻은 경우 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="9f090-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="9f090-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="9f090-163">VMImage의 게시자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="9f090-164">퍼블리셔를 얻지 위해 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9f090-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="9f090-165">-ImageReferenceSku</span></span>
<span data-ttu-id="9f090-166">VMImage SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="9f090-167">SKUS를 얻지 위해 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="9f090-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="9f090-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="9f090-169">VMImage 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="9f090-170">최신 버전을 사용하기 위해 특정 버전 대신 최신 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="9f090-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="9f090-171">-ImageUri</span></span>
<span data-ttu-id="9f090-172">사용자 이미지에 대한 Blob URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="9f090-173">VMSS는 사용자 이미지의 동일한 컨테이너에 운영 체제 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="9f090-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9f090-174">-LicenseType</span></span>
<span data-ttu-id="9f090-175">라이선스 시나리오를 가져오기 위한 라이선스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="9f090-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9f090-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="9f090-177">관리 디스크에 대한 저장소 계정 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="9f090-178">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f090-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="9f090-179">StandardLRS</span></span>
- <span data-ttu-id="9f090-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="9f090-180">PremiumLRS</span></span>

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

### <span data-ttu-id="9f090-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="9f090-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="9f090-182">한 번의 일괄 처리로 롤링 업그레이드를 통해 동시에 업그레이드되는 총 가상 머신 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="9f090-183">이전 또는 향후 일괄 처리에서 최대의 이상한 인스턴스이기 때문에 일괄 처리의 인스턴스 백분율이 감소하여 더 높은 안정성을 보장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="9f090-184">값을 지정하지 않으면 20으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-184">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="9f090-185">-MaxPrice</span></span>
<span data-ttu-id="9f090-186">우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="9f090-187">이 가격은 미국 달러입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-187">This price is in US Dollars.</span></span> <span data-ttu-id="9f090-188">이 가격은 VM 크기에 대한 현재 낮은 우선 순위 가격과 비교됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="9f090-189">또한 가격은 우선 순위가 낮은 VM/VMSS를 만들/업데이트할 때 비교하며, maxPrice가 현재 낮은 우선 순위 가격보다 큰 경우 작업이 성공합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="9f090-190">현재 낮은 우선 순위 가격이 VM/VMSS를 생성한 후 maxPrice를 초과하는 경우, maxPrice는 우선 순위가 낮은 VM/VMSS를 지우는 데도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="9f090-191">가능한 값은 0보다 큰 소수점 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="9f090-192">예: 0.01538입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-192">Example: 0.01538.</span></span>  <span data-ttu-id="9f090-193">-1은 가격상의 이유로 우선 순위가 낮은 VM/VMSS를 아 내지 말아야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="9f090-194">또한 기본 최대 가격은 사용자가 제공하지 않는 경우 -1입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-194">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="9f090-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="9f090-196">업그레이드가 중단되기 전에 가상 머신 상태 확인에 의해 위태로울 수 있는 확장 집합의 총 가상 머신 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="9f090-197">이 제약 조건은 일괄 처리를 시작하기 전에 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="9f090-198">값을 지정하지 않으면 20으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-198">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="9f090-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="9f090-200">업그레이드된 가상 머신 인스턴스의 최대 백분율은 상태가 상태가 나타남을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="9f090-201">이 검사는 각 일괄 처리가 업그레이드된 후에 진행됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="9f090-202">이 백분율을 초과하면 롤링 업데이트가 중단됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="9f090-203">값을 지정하지 않으면 20으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-203">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="9f090-204">-OsDiskCaching</span></span>
<span data-ttu-id="9f090-205">운영 체제 디스크의 캐싱 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="9f090-206">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f090-207">없음</span><span class="sxs-lookup"><span data-stu-id="9f090-207">None</span></span>
- <span data-ttu-id="9f090-208">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9f090-208">ReadOnly</span></span>
- <span data-ttu-id="9f090-209">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="9f090-210">캐싱 값을 변경하면 cmdlet이 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="9f090-211">이 설정은 디스크의 일관성 및 성능에 영향을 미치게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-211">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9f090-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="9f090-213">OS 디스크에서 WriteAccelerator를 사용하도록 설정하거나 사용하지 않도록 설정해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="9f090-214">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="9f090-214">-Overprovision</span></span>
<span data-ttu-id="9f090-215">cmdlet이 VMSS를 오버프로비전하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="9f090-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="9f090-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="9f090-217">모든 가상 머신에 대한 업데이트를 한 일괄 처리로 완료하고 다음 일괄 처리를 시작하는 사이의 대기 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="9f090-218">시간 기간은 ISO 8601 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="9f090-219">기본값은 0초(PT0S)입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="9f090-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="9f090-220">-PlanName</span></span>
<span data-ttu-id="9f090-221">계획 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="9f090-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="9f090-222">-PlanProduct</span></span>
<span data-ttu-id="9f090-223">계획 제품을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="9f090-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="9f090-224">-PlanPromotionCode</span></span>
<span data-ttu-id="9f090-225">계획 프로모션 코드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="9f090-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="9f090-226">-PlanPublisher</span></span>
<span data-ttu-id="9f090-227">계획 게시자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="9f090-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="9f090-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="9f090-229">VMSS의 Windows 가상 머신에서 가상 머신 에이전트를 프로비전해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="9f090-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="9f090-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="9f090-231">이 확장 집합에 사용할 근접 배치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="9f090-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f090-232">-ResourceGroupName</span></span>
<span data-ttu-id="9f090-233">VMSS가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="9f090-234">-ScaleInPolicy</span></span>
<span data-ttu-id="9f090-235">가상 머신 확장 집합의 크기 조정 시 따라야 할 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="9f090-236">가능한 값은 'Default', 'OldestVM' 및 'NewestVM'입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="9f090-237">가상 머신 확장 집합이 확장될 때 '기본값'은 크기 조정 집합이 영역 전체에 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="9f090-238">그런 다음 오류 도메인에서 가능한 한 균형이 조정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="9f090-239">각 장애 도메인 내에서 제거를 위해 선택한 가상 머신은 확장으로부터 보호되지 않는 가장 최근의 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="9f090-240">가상 머신 확장 집합이 확장되는 경우 'OldestVM'은 확장으로부터 보호되지 않는 가장 오래된 가상 머신을 제거하기 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="9f090-241">zonal 가상 머신 확장 집합의 경우 먼저 확장 집합이 영역 전체에서 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="9f090-242">각 영역 내에서 보호되지 않는 가장 오래된 가상 머신은 제거를 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="9f090-243">가상 머신 확장 집합이 확장되는 경우 'NewestVM'은 확장으로부터 보호되지 않는 가장 최근 가상 머신을 제거하기 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="9f090-244">zonal 가상 머신 확장 집합의 경우 먼저 확장 집합이 영역 전체에서 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="9f090-245">각 영역 내에서 보호되지 않는 가장 새로운 가상 머신은 제거를 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="9f090-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="9f090-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="9f090-247">단일 배치 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="9f090-248">-SkipExtensionsOnOverprovisionedVM</span><span class="sxs-lookup"><span data-stu-id="9f090-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="9f090-249">확장이 추가 오버프로비전된 VM에서 실행되지 않는지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="9f090-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9f090-250">-SkuCapacity</span></span>
<span data-ttu-id="9f090-251">VMSS의 인스턴스 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-251">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9f090-252">-SkuName</span></span>
<span data-ttu-id="9f090-253">VMSS의 모든 인스턴스의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="9f090-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="9f090-254">-SkuTier</span></span>
<span data-ttu-id="9f090-255">VMSS의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="9f090-256">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f090-257">표준</span><span class="sxs-lookup"><span data-stu-id="9f090-257">Standard</span></span>
- <span data-ttu-id="9f090-258">기본</span><span class="sxs-lookup"><span data-stu-id="9f090-258">Basic</span></span>

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

### <span data-ttu-id="9f090-259">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f090-259">-Tag</span></span>
<span data-ttu-id="9f090-260">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9f090-261">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9f090-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9f090-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="9f090-263">구성 가능한 시간(분) 삭제되는 Virtual Machine은 이벤트가 자동 승인(시간 제한)되기 전에 예약된 종료 이벤트를 승인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="9f090-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="9f090-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="9f090-265">예약된 종료 이벤트를 사용하도록 설정하거나 사용하지 않도록 설정할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-266">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="9f090-266">-TimeZone</span></span>
<span data-ttu-id="9f090-267">Windows OS의 표준 시간대를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="9f090-268">예: \" 태평양 표준시 \" 입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="9f090-269">가능한 값은 [](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) [TimeZoneInfo.GetSystemTimeZones에서](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)TimeZoneInfo.Id 표준 시간대에서 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="9f090-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="9f090-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="9f090-271">가상 머신 확장 집합에 저장소 계정 유형이 있는 하나 이상의 관리되는 데이터 디스크를 UltraSSD_LRS 수 있는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="9f090-272">저장소 계정 유형이 있는 UltraSSD_LRS 이 속성을 사용하도록 설정한 경우 VMSS에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="9f090-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="9f090-274">확장 집합에서 가상 머신으로 업그레이드 모드를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="9f090-275">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f090-276">자동 번역</span><span class="sxs-lookup"><span data-stu-id="9f090-276">Automatic</span></span>
- <span data-ttu-id="9f090-277">수동</span><span class="sxs-lookup"><span data-stu-id="9f090-277">Manual</span></span>
- <span data-ttu-id="9f090-278">롤링</span><span class="sxs-lookup"><span data-stu-id="9f090-278">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="9f090-279">-VhdContainer</span></span>
<span data-ttu-id="9f090-280">VMSS에 대한 운영 체제 디스크를 저장하는 데 사용되는 컨테이너 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="9f090-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9f090-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9f090-282">로컬 VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="9f090-283">VMSS 개체를 얻으면 Get-AzVmss cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="9f090-284">이 가상 머신 개체에는 VMSS에 대한 업데이트된 상태가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-284">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9f090-285">-VMScaleSetName</span></span>
<span data-ttu-id="9f090-286">이 cmdlet이 만드는 VMSS의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-287">-확인</span><span class="sxs-lookup"><span data-stu-id="9f090-287">-Confirm</span></span>
<span data-ttu-id="9f090-288">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-288">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f090-289">-WhatIf</span></span>
<span data-ttu-id="9f090-290">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f090-291">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-291">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f090-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f090-292">CommonParameters</span></span>
<span data-ttu-id="9f090-293">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9f090-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f090-294">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f090-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f090-295">입력</span><span class="sxs-lookup"><span data-stu-id="9f090-295">INPUTS</span></span>

### <span data-ttu-id="9f090-296">System.String</span><span class="sxs-lookup"><span data-stu-id="9f090-296">System.String</span></span>

### <span data-ttu-id="9f090-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9f090-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="9f090-298">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f090-298">System.Boolean</span></span>

## <span data-ttu-id="9f090-299">출력</span><span class="sxs-lookup"><span data-stu-id="9f090-299">OUTPUTS</span></span>

### <span data-ttu-id="9f090-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9f090-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9f090-301">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f090-301">NOTES</span></span>

## <span data-ttu-id="9f090-302">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f090-302">RELATED LINKS</span></span>

[<span data-ttu-id="9f090-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f090-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="9f090-304">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f090-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="9f090-305">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f090-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="9f090-306">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f090-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="9f090-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f090-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="9f090-308">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f090-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="9f090-309">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f090-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


