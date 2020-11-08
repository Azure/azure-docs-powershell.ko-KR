---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213067"
---
# <span data-ttu-id="7ac94-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ac94-101">Update-AzVmss</span></span>

## <span data-ttu-id="7ac94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ac94-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac94-103">VMSS의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="7ac94-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ac94-104">SYNTAX</span></span>

### <span data-ttu-id="7ac94-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="7ac94-105">DefaultParameter (Default)</span></span>
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

### <span data-ttu-id="7ac94-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ac94-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="7ac94-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7ac94-107">DESCRIPTION</span></span>
<span data-ttu-id="7ac94-108">**AzVmss** CMDLET은 Vmss (가상 컴퓨터 크기 집합)의 상태를 로컬 vmss 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="7ac94-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7ac94-109">EXAMPLES</span></span>

### <span data-ttu-id="7ac94-110">예제 1: VMSS의 상태를 로컬 VMSS 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="7ac94-111">이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS001 라는 VMSS의 상태를 로컬 VMSS 개체의 state로 업데이트 하 고 $LocalVMSS 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="7ac94-112">변수</span><span class="sxs-lookup"><span data-stu-id="7ac94-112">PARAMETERS</span></span>

### <span data-ttu-id="7ac94-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ac94-113">-AsJob</span></span>
<span data-ttu-id="7ac94-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7ac94-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="7ac94-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="7ac94-116">최신 버전의 이미지를 사용할 수 있게 되 면 이동 방식으로 확장 설정 인스턴스에 OS 업그레이드를 자동으로 적용할지 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="7ac94-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="7ac94-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="7ac94-118">VM의 상태 변경으로 인해 자동 복구가 일시 중단 되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="7ac94-119">상태 변경이 완료 된 후에 유예 시간이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="7ac94-120">이는 예기치 않은 복구 또는 우발적으로 수리 하는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="7ac94-121">기간을 ISO 8601 형식으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="7ac94-122">허용 되는 최소 유예 기간은 30 분 (PT30M) 이며,이 값도 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="7ac94-123">허용 되는 최대 유예 기간은 90 분 (PT90M)입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="7ac94-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="7ac94-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="7ac94-125">가상 컴퓨터 크기 집합에 부팅 진단을 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="7ac94-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="7ac94-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="7ac94-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="7ac94-127">콘솔 출력과 스크린샷을 배치 하는 데 사용할 저장소 계정의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="7ac94-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="7ac94-128">-CustomData</span></span>
<span data-ttu-id="7ac94-129">사용자 지정 데이터의 base-64 인코딩된 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="7ac94-130">이는 가상 컴퓨터에 파일로 저장 된 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="7ac94-131">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="7ac94-132">VM에 대 한 클라우드 초기화를 사용 [하려면 클라우드 초기화를 사용 하 여 LINUX VM을 만드는 동안 사용자 지정](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ac94-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="7ac94-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac94-133">-DefaultProfile</span></span>
<span data-ttu-id="7ac94-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac94-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="7ac94-135">-DisableAutoRollback</span></span>
<span data-ttu-id="7ac94-136">자동 OS 업그레이드 정책에 대 한 자동 롤백 해제</span><span class="sxs-lookup"><span data-stu-id="7ac94-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="7ac94-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="7ac94-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="7ac94-138">이 cmdlet이 Linux OS에 대 한 암호 인증을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="7ac94-139">-Enable자동 복구</span><span class="sxs-lookup"><span data-stu-id="7ac94-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="7ac94-140">가상 머신 크기 집합에 대 한 자동 복구를 설정 하거나 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="7ac94-141">-Enable자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ac94-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="7ac94-142">VMSS의 Windows 가상 컴퓨터를 자동 업데이트에 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="7ac94-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="7ac94-143">-EncryptionAtHost</span></span>
<span data-ttu-id="7ac94-144">이 매개 변수는 사용자가 가상 컴퓨터 크기 집합에 대 한 호스트 암호화를 사용 하거나 사용 하지 않도록 설정 하는 요청에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="7ac94-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="7ac94-145">-IdentityId</span></span>
<span data-ttu-id="7ac94-146">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="7ac94-147">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="7ac94-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7ac94-148">-IdentityType</span></span>
<span data-ttu-id="7ac94-149">가상 컴퓨터 크기 집합에 사용 되는 id 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="7ac94-150">' SystemAssignedUserAssigned ' 형식에는 암시적으로 만든 id와 사용자가 할당 한 id 집합이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="7ac94-151">' 없음 ' 형식은 가상 컴퓨터 배율 집합에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="7ac94-152">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ac94-153">지정 된 SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="7ac94-153">SystemAssigned</span></span>
- <span data-ttu-id="7ac94-154">UserAssigned 됨</span><span class="sxs-lookup"><span data-stu-id="7ac94-154">UserAssigned</span></span>
- <span data-ttu-id="7ac94-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="7ac94-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="7ac94-156">않아야</span><span class="sxs-lookup"><span data-stu-id="7ac94-156">None</span></span>

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

### <span data-ttu-id="7ac94-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="7ac94-157">-ImageReferenceId</span></span>
<span data-ttu-id="7ac94-158">이미지 참조 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="7ac94-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="7ac94-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="7ac94-160">VMImage (가상 컴퓨터 이미지) 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="7ac94-161">이미지 제안을 얻으려면 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="7ac94-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="7ac94-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="7ac94-163">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="7ac94-164">게시자를 얻으려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="7ac94-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="7ac94-165">-ImageReferenceSku</span></span>
<span data-ttu-id="7ac94-166">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="7ac94-167">Sku를 가져오려면 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="7ac94-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="7ac94-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="7ac94-169">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="7ac94-170">최신 버전을 사용 하려면 특정 버전 대신 최신 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="7ac94-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="7ac94-171">-ImageUri</span></span>
<span data-ttu-id="7ac94-172">사용자 이미지에 대 한 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="7ac94-173">VMSS는 사용자 이미지의 동일한 컨테이너에서 운영 체제 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="7ac94-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7ac94-174">-LicenseType</span></span>
<span data-ttu-id="7ac94-175">라이선스 종류를 지정 합니다 (사용자 고유의 라이선스 시나리오를 가져오는 데 사용).</span><span class="sxs-lookup"><span data-stu-id="7ac94-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="7ac94-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7ac94-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="7ac94-177">관리 디스크에 대 한 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="7ac94-178">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ac94-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="7ac94-179">StandardLRS</span></span>
- <span data-ttu-id="7ac94-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="7ac94-180">PremiumLRS</span></span>

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

### <span data-ttu-id="7ac94-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="7ac94-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="7ac94-182">한 일괄 처리에서 롤링 업그레이드에 의해 동시에 업그레이드 되는 총 가상 머신 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="7ac94-183">이는 최대이 고 이전 또는 이후 일괄 처리에서 비정상적인 인스턴스가 있으면 일괄 처리에서 인스턴스의 백분율이 더 높은 안정성을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="7ac94-184">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-184">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="7ac94-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="7ac94-185">-MaxPrice</span></span>
<span data-ttu-id="7ac94-186">우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="7ac94-187">이 가격은 미국 달러입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-187">This price is in US Dollars.</span></span> <span data-ttu-id="7ac94-188">이 가격은 VM 크기에 대 한 현재의 낮은 우선 순위 가격과 비교 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="7ac94-189">또한 우선 순위가 낮은 VM/VMSS의 생성/업데이트가 수행 될 때 가격이 비교 되 고 maxPrice가 현재 낮은 우선 순위의 가격 보다 더 큰 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="7ac94-190">MaxPrice는 VM/VMSS를 만든 후 현재 낮은 우선 순위의 가격이 maxPrice를 초과 하는 경우 우선 순위가 낮은 VM/VMSS를 제거 하는 데도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="7ac94-191">가능한 값은 다음과 같습니다. 0 보다 큰 10 진수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="7ac94-192">예: 0.01538.</span><span class="sxs-lookup"><span data-stu-id="7ac94-192">Example: 0.01538.</span></span>  <span data-ttu-id="7ac94-193">-1은 낮은 우선 순위의 VM/VMSS가 가격 이유로 제거 되어서는 안 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="7ac94-194">또한 기본 최대 가격은 사용자가 제공 하지 않는 경우-1입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-194">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="7ac94-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="7ac94-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="7ac94-196">업그레이드 결과 또는 롤링 업그레이드 중단 전에 가상 컴퓨터 상태 검사를 통해 비정상 상태에 있는 것으로 볼 수 있는 배율 집합의 총 가상 머신 인스턴스 중 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="7ac94-197">일괄 처리를 시작 하기 전에이 제약 조건을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="7ac94-198">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-198">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="7ac94-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="7ac94-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="7ac94-200">비정상 상태에 있는 것으로 확인 될 수 있는 업그레이드 된 가상 컴퓨터 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="7ac94-201">이 검사는 각 일괄 처리가 업그레이드 된 후에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="7ac94-202">이 백분율이 초과 되 면 롤링 업데이트가 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="7ac94-203">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-203">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="7ac94-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="7ac94-204">-OsDiskCaching</span></span>
<span data-ttu-id="7ac94-205">운영 체제 디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="7ac94-206">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ac94-207">않아야</span><span class="sxs-lookup"><span data-stu-id="7ac94-207">None</span></span>
- <span data-ttu-id="7ac94-208">읽기</span><span class="sxs-lookup"><span data-stu-id="7ac94-208">ReadOnly</span></span>
- <span data-ttu-id="7ac94-209">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="7ac94-210">캐싱 값을 변경 하면 cmdlet이 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="7ac94-211">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-211">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="7ac94-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7ac94-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="7ac94-213">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="7ac94-214">-과잉 프로비저닝</span><span class="sxs-lookup"><span data-stu-id="7ac94-214">-Overprovision</span></span>
<span data-ttu-id="7ac94-215">Cmdlet이 VMSS를 프로 비전 하 고 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="7ac94-216">-Pausetimeenwe일괄 처리</span><span class="sxs-lookup"><span data-stu-id="7ac94-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="7ac94-217">한 일괄 처리의 모든 가상 컴퓨터에 대 한 업데이트를 완료 하 고 다음 일괄 처리를 시작 하는 대기 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="7ac94-218">기간을 ISO 8601 형식으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="7ac94-219">기본값은 0 초 (PT0S)입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="7ac94-220">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="7ac94-220">-PlanName</span></span>
<span data-ttu-id="7ac94-221">계획 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="7ac94-222">계획 제품</span><span class="sxs-lookup"><span data-stu-id="7ac94-222">-PlanProduct</span></span>
<span data-ttu-id="7ac94-223">계획 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="7ac94-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="7ac94-224">-PlanPromotionCode</span></span>
<span data-ttu-id="7ac94-225">계획 프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="7ac94-226">-계획 Publisher</span><span class="sxs-lookup"><span data-stu-id="7ac94-226">-PlanPublisher</span></span>
<span data-ttu-id="7ac94-227">계획 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="7ac94-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="7ac94-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="7ac94-229">VMSS의 Windows 가상 컴퓨터에서 가상 컴퓨터 에이전트를 프로 비전 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="7ac94-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="7ac94-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="7ac94-231">이 배율 집합에 사용할 근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="7ac94-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ac94-232">-ResourceGroupName</span></span>
<span data-ttu-id="7ac94-233">VMSS가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="7ac94-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="7ac94-234">-ScaleInPolicy</span></span>
<span data-ttu-id="7ac94-235">가상 컴퓨터 배율 집합의 크기 조정을 할 때 따라야 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="7ac94-236">사용할 수 있는 값은 ' Default ', ' OldestVM ' 및 ' NewestVM '입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="7ac94-237">' Default ' 가상 컴퓨터 배율 집합이에서 크기를 조정 하면 영역에 대해 먼저 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="7ac94-238">그런 다음, 최대한 다양 한 장애 도메인에 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="7ac94-239">각 장애 도메인 내에서 제거 하도록 선택 된 가상 머신은 확장 기능에서 보호 되지 않는 최신 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="7ac94-240">' OldestVM ' 가상 컴퓨터 크기 조정 집합을 확장 하는 동안에는 스케일에서 보호 되지 않는 가장 오래 된 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="7ac94-241">영역 가상 컴퓨터 배율 집합의 경우에는 맨 먼저 범위에서 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="7ac94-242">각 영역 내에서 보호 되지 않는 가장 오래 된 가상 컴퓨터는 제거 하도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="7ac94-243">' NewestVM ' 가상 컴퓨터 배율 집합이 확장 되는 경우에는 스케일에서 보호 되지 않는 최신 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="7ac94-244">영역 가상 컴퓨터 배율 집합의 경우에는 맨 먼저 범위에서 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="7ac94-245">각 영역 내에서 보호 되지 않는 최신 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="7ac94-246">-Single배치 그룹</span><span class="sxs-lookup"><span data-stu-id="7ac94-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="7ac94-247">단일 배치 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="7ac94-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="7ac94-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="7ac94-249">추가 과잉 프로 비전 된 Vm에서 확장이 실행 되지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="7ac94-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7ac94-250">-SkuCapacity</span></span>
<span data-ttu-id="7ac94-251">VMSS의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-251">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="7ac94-252">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="7ac94-252">-SkuName</span></span>
<span data-ttu-id="7ac94-253">VMSS의 모든 인스턴스 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="7ac94-254">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="7ac94-254">-SkuTier</span></span>
<span data-ttu-id="7ac94-255">VMSS의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="7ac94-256">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ac94-257">표준이</span><span class="sxs-lookup"><span data-stu-id="7ac94-257">Standard</span></span>
- <span data-ttu-id="7ac94-258">기본적</span><span class="sxs-lookup"><span data-stu-id="7ac94-258">Basic</span></span>

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

### <span data-ttu-id="7ac94-259">태그</span><span class="sxs-lookup"><span data-stu-id="7ac94-259">-Tag</span></span>
<span data-ttu-id="7ac94-260">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7ac94-261">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7ac94-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7ac94-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7ac94-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="7ac94-263">구성 가능한 기간 (분) 삭제 되는 가상 컴퓨터는 이벤트가 자동으로 승인 되기 전에 종료 예약 된 이벤트를 승인 해야 합니다 (시간 초과).</span><span class="sxs-lookup"><span data-stu-id="7ac94-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="7ac94-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="7ac94-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="7ac94-265">종료 예약 된 이벤트를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="7ac94-266">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="7ac94-266">-TimeZone</span></span>
<span data-ttu-id="7ac94-267">Windows OS의 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="7ac94-268">예: \" 태평양 표준시 시간 \" .</span><span class="sxs-lookup"><span data-stu-id="7ac94-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="7ac94-269">가능한 값은 [TimeZoneInfo Systemtimezones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)에서 반환 된 표준 시간대의 [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) 값이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="7ac94-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="7ac94-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="7ac94-271">하나 이상의 관리 되는 데이터 디스크를 가상 컴퓨터 크기 집합에서 UltraSSD_LRS 저장소 계정 유형과 함께 사용 하는 기능을 사용 하거나 사용 하지 않도록 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="7ac94-272">저장소 계정 유형이 UltraSSD_LRS 관리 디스크는이 속성을 사용 하도록 설정 된 경우에만 VMSS에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="7ac94-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="7ac94-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="7ac94-274">확장 집합의 가상 컴퓨터로 업그레이드 모드를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="7ac94-275">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ac94-276">자동 번역</span><span class="sxs-lookup"><span data-stu-id="7ac94-276">Automatic</span></span>
- <span data-ttu-id="7ac94-277">수동</span><span class="sxs-lookup"><span data-stu-id="7ac94-277">Manual</span></span>
- <span data-ttu-id="7ac94-278">롤백할</span><span class="sxs-lookup"><span data-stu-id="7ac94-278">Rolling</span></span>

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

### <span data-ttu-id="7ac94-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="7ac94-279">-VhdContainer</span></span>
<span data-ttu-id="7ac94-280">VMSS의 운영 체제 디스크를 저장 하는 데 사용 되는 컨테이너 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="7ac94-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7ac94-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7ac94-282">로컬 VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="7ac94-283">VMSS 개체를 가져오려면 Get-AzVmss cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="7ac94-284">이 가상 컴퓨터 개체에는 VMSS의 업데이트 상태가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-284">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="7ac94-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7ac94-285">-VMScaleSetName</span></span>
<span data-ttu-id="7ac94-286">이 cmdlet이 만드는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7ac94-287">-확인</span><span class="sxs-lookup"><span data-stu-id="7ac94-287">-Confirm</span></span>
<span data-ttu-id="7ac94-288">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-288">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ac94-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ac94-289">-WhatIf</span></span>
<span data-ttu-id="7ac94-290">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ac94-291">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-291">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ac94-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac94-292">CommonParameters</span></span>
<span data-ttu-id="7ac94-293">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ac94-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac94-294">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ac94-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac94-295">입력</span><span class="sxs-lookup"><span data-stu-id="7ac94-295">INPUTS</span></span>

### <span data-ttu-id="7ac94-296">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7ac94-296">System.String</span></span>

### <span data-ttu-id="7ac94-297">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="7ac94-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="7ac94-298">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7ac94-298">System.Boolean</span></span>

## <span data-ttu-id="7ac94-299">출력</span><span class="sxs-lookup"><span data-stu-id="7ac94-299">OUTPUTS</span></span>

### <span data-ttu-id="7ac94-300">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="7ac94-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7ac94-301">상속자</span><span class="sxs-lookup"><span data-stu-id="7ac94-301">NOTES</span></span>

## <span data-ttu-id="7ac94-302">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ac94-302">RELATED LINKS</span></span>

[<span data-ttu-id="7ac94-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ac94-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="7ac94-304">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ac94-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="7ac94-305">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ac94-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="7ac94-306">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ac94-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="7ac94-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ac94-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="7ac94-308">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ac94-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="7ac94-309">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ac94-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


