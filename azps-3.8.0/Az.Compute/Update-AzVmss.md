---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: bf8fa8c4b7d1d08cdb6d0c2c348f5c97a2788a4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044587"
---
# <span data-ttu-id="4d1db-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d1db-101">Update-AzVmss</span></span>

## <span data-ttu-id="4d1db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d1db-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1db-103">VMSS의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="4d1db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d1db-104">SYNTAX</span></span>

### <span data-ttu-id="4d1db-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d1db-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d1db-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d1db-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d1db-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4d1db-107">DESCRIPTION</span></span>
<span data-ttu-id="4d1db-108">**AzVmss** CMDLET은 Vmss (가상 컴퓨터 크기 집합)의 상태를 로컬 vmss 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="4d1db-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4d1db-109">EXAMPLES</span></span>

### <span data-ttu-id="4d1db-110">예제 1: VMSS의 상태를 로컬 VMSS 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="4d1db-111">이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS001 라는 VMSS의 상태를 로컬 VMSS 개체의 state로 업데이트 하 고 $LocalVMSS 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="4d1db-112">변수</span><span class="sxs-lookup"><span data-stu-id="4d1db-112">PARAMETERS</span></span>

### <span data-ttu-id="4d1db-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d1db-113">-AsJob</span></span>
<span data-ttu-id="4d1db-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4d1db-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="4d1db-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="4d1db-116">최신 버전의 이미지를 사용할 수 있게 되 면 이동 방식으로 확장 설정 인스턴스에 OS 업그레이드를 자동으로 적용할지 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="4d1db-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="4d1db-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="4d1db-118">VM의 상태 변경으로 인해 자동 복구가 일시 중단 되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="4d1db-119">상태 변경이 완료 된 후에 유예 시간이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="4d1db-120">이는 예기치 않은 복구 또는 우발적으로 수리 하는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="4d1db-121">기간을 ISO 8601 형식으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="4d1db-122">기본값은 5 분 (PT5M)입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-122">The default value is 5 minutes (PT5M).</span></span>

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

### <span data-ttu-id="4d1db-123">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="4d1db-123">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="4d1db-124">동시에 복구 되는 가상 컴퓨터의 백분율 (scaleset의 용량)입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-124">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="4d1db-125">기본 값은 20%입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-125">The default value is 20%.</span></span>

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

### <span data-ttu-id="4d1db-126">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="4d1db-126">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="4d1db-127">가상 컴퓨터 크기 집합에 부팅 진단을 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="4d1db-127">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4d1db-128">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="4d1db-128">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="4d1db-129">콘솔 출력과 스크린샷을 배치 하는 데 사용할 저장소 계정의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-129">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="4d1db-130">-CustomData</span><span class="sxs-lookup"><span data-stu-id="4d1db-130">-CustomData</span></span>
<span data-ttu-id="4d1db-131">사용자 지정 데이터의 base-64 인코딩된 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-131">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="4d1db-132">이는 가상 컴퓨터에 파일로 저장 된 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-132">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="4d1db-133">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-133">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="4d1db-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1db-134">-DefaultProfile</span></span>
<span data-ttu-id="4d1db-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d1db-136">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="4d1db-136">-DisableAutoRollback</span></span>
<span data-ttu-id="4d1db-137">자동 OS 업그레이드 정책에 대 한 자동 롤백 해제</span><span class="sxs-lookup"><span data-stu-id="4d1db-137">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="4d1db-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="4d1db-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="4d1db-139">이 cmdlet이 Linux OS에 대 한 암호 인증을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-139">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="4d1db-140">-Enable자동 복구</span><span class="sxs-lookup"><span data-stu-id="4d1db-140">-EnableAutomaticRepair</span></span>
<span data-ttu-id="4d1db-141">가상 머신 크기 집합에 대 한 자동 복구를 설정 하거나 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-141">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4d1db-142">-Enable자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="4d1db-142">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="4d1db-143">VMSS의 Windows 가상 컴퓨터를 자동 업데이트에 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-143">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="4d1db-144">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="4d1db-144">-IdentityId</span></span>
<span data-ttu-id="4d1db-145">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-145">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="4d1db-146">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-146">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="4d1db-147">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4d1db-147">-IdentityType</span></span>
<span data-ttu-id="4d1db-148">가상 컴퓨터 크기 집합에 사용 되는 id 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-148">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="4d1db-149">' SystemAssignedUserAssigned ' 형식에는 암시적으로 만든 id와 사용자가 할당 한 id 집합이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-149">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="4d1db-150">' 없음 ' 형식은 가상 컴퓨터 배율 집합에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-150">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="4d1db-151">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d1db-152">지정 된 SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="4d1db-152">SystemAssigned</span></span>
- <span data-ttu-id="4d1db-153">UserAssigned 됨</span><span class="sxs-lookup"><span data-stu-id="4d1db-153">UserAssigned</span></span>
- <span data-ttu-id="4d1db-154">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="4d1db-154">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="4d1db-155">않아야</span><span class="sxs-lookup"><span data-stu-id="4d1db-155">None</span></span>

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

### <span data-ttu-id="4d1db-156">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="4d1db-156">-ImageReferenceId</span></span>
<span data-ttu-id="4d1db-157">이미지 참조 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-157">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="4d1db-158">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="4d1db-158">-ImageReferenceOffer</span></span>
<span data-ttu-id="4d1db-159">VMImage (가상 컴퓨터 이미지) 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-159">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="4d1db-160">이미지 제안을 얻으려면 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-160">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="4d1db-161">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="4d1db-161">-ImageReferencePublisher</span></span>
<span data-ttu-id="4d1db-162">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-162">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="4d1db-163">게시자를 얻으려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-163">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4d1db-164">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="4d1db-164">-ImageReferenceSku</span></span>
<span data-ttu-id="4d1db-165">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-165">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="4d1db-166">Sku를 가져오려면 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-166">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="4d1db-167">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="4d1db-167">-ImageReferenceVersion</span></span>
<span data-ttu-id="4d1db-168">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-168">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="4d1db-169">최신 버전을 사용 하려면 특정 버전 대신 최신 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-169">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="4d1db-170">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="4d1db-170">-ImageUri</span></span>
<span data-ttu-id="4d1db-171">사용자 이미지에 대 한 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-171">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="4d1db-172">VMSS는 사용자 이미지의 동일한 컨테이너에서 운영 체제 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-172">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="4d1db-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4d1db-173">-LicenseType</span></span>
<span data-ttu-id="4d1db-174">라이선스 종류를 지정 합니다 (사용자 고유의 라이선스 시나리오를 가져오는 데 사용).</span><span class="sxs-lookup"><span data-stu-id="4d1db-174">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="4d1db-175">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4d1db-175">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="4d1db-176">관리 디스크에 대 한 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-176">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="4d1db-177">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d1db-178">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="4d1db-178">StandardLRS</span></span>
- <span data-ttu-id="4d1db-179">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="4d1db-179">PremiumLRS</span></span>

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

### <span data-ttu-id="4d1db-180">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="4d1db-180">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="4d1db-181">한 일괄 처리에서 롤링 업그레이드에 의해 동시에 업그레이드 되는 총 가상 머신 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-181">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="4d1db-182">이는 최대이 고 이전 또는 이후 일괄 처리에서 비정상적인 인스턴스가 있으면 일괄 처리에서 인스턴스의 백분율이 더 높은 안정성을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-182">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="4d1db-183">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-183">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="4d1db-184">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="4d1db-184">-MaxPrice</span></span>
<span data-ttu-id="4d1db-185">우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-185">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="4d1db-186">이 가격은 미국 달러입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-186">This price is in US Dollars.</span></span> <span data-ttu-id="4d1db-187">이 가격은 VM 크기에 대 한 현재의 낮은 우선 순위 가격과 비교 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-187">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="4d1db-188">또한 우선 순위가 낮은 VM/VMSS의 생성/업데이트가 수행 될 때 가격이 비교 되 고 maxPrice가 현재 낮은 우선 순위의 가격 보다 더 큰 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-188">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="4d1db-189">MaxPrice는 VM/VMSS를 만든 후 현재 낮은 우선 순위의 가격이 maxPrice를 초과 하는 경우 우선 순위가 낮은 VM/VMSS를 제거 하는 데도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-189">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="4d1db-190">가능한 값은 다음과 같습니다. 0 보다 큰 10 진수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-190">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="4d1db-191">예: 0.01538.</span><span class="sxs-lookup"><span data-stu-id="4d1db-191">Example: 0.01538.</span></span>  <span data-ttu-id="4d1db-192">-1은 낮은 우선 순위의 VM/VMSS가 가격 이유로 제거 되어서는 안 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-192">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="4d1db-193">또한 기본 최대 가격은 사용자가 제공 하지 않는 경우-1입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-193">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="4d1db-194">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="4d1db-194">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="4d1db-195">업그레이드 결과 또는 롤링 업그레이드 중단 전에 가상 컴퓨터 상태 검사를 통해 비정상 상태에 있는 것으로 볼 수 있는 배율 집합의 총 가상 머신 인스턴스 중 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-195">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="4d1db-196">일괄 처리를 시작 하기 전에이 제약 조건을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-196">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="4d1db-197">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-197">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="4d1db-198">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="4d1db-198">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="4d1db-199">비정상 상태에 있는 것으로 확인 될 수 있는 업그레이드 된 가상 컴퓨터 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-199">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="4d1db-200">이 검사는 각 일괄 처리가 업그레이드 된 후에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-200">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="4d1db-201">이 백분율이 초과 되 면 롤링 업데이트가 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-201">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="4d1db-202">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-202">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="4d1db-203">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="4d1db-203">-OsDiskCaching</span></span>
<span data-ttu-id="4d1db-204">운영 체제 디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-204">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="4d1db-205">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-205">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d1db-206">않아야</span><span class="sxs-lookup"><span data-stu-id="4d1db-206">None</span></span>
- <span data-ttu-id="4d1db-207">읽기</span><span class="sxs-lookup"><span data-stu-id="4d1db-207">ReadOnly</span></span>
- <span data-ttu-id="4d1db-208">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-208">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="4d1db-209">캐싱 값을 변경 하면 cmdlet이 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-209">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="4d1db-210">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-210">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="4d1db-211">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4d1db-211">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="4d1db-212">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-212">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="4d1db-213">-과잉 프로비저닝</span><span class="sxs-lookup"><span data-stu-id="4d1db-213">-Overprovision</span></span>
<span data-ttu-id="4d1db-214">Cmdlet이 VMSS를 프로 비전 하 고 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-214">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="4d1db-215">-Pausetimeenwe일괄 처리</span><span class="sxs-lookup"><span data-stu-id="4d1db-215">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="4d1db-216">한 일괄 처리의 모든 가상 컴퓨터에 대 한 업데이트를 완료 하 고 다음 일괄 처리를 시작 하는 대기 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-216">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="4d1db-217">기간을 ISO 8601 형식으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-217">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="4d1db-218">기본값은 0 초 (PT0S)입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-218">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="4d1db-219">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="4d1db-219">-PlanName</span></span>
<span data-ttu-id="4d1db-220">계획 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-220">Specifies the plan name.</span></span>

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

### <span data-ttu-id="4d1db-221">계획 제품</span><span class="sxs-lookup"><span data-stu-id="4d1db-221">-PlanProduct</span></span>
<span data-ttu-id="4d1db-222">계획 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-222">Specifies the plan product.</span></span>

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

### <span data-ttu-id="4d1db-223">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="4d1db-223">-PlanPromotionCode</span></span>
<span data-ttu-id="4d1db-224">계획 프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-224">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="4d1db-225">-계획 Publisher</span><span class="sxs-lookup"><span data-stu-id="4d1db-225">-PlanPublisher</span></span>
<span data-ttu-id="4d1db-226">계획 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-226">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="4d1db-227">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="4d1db-227">-ProvisionVMAgent</span></span>
<span data-ttu-id="4d1db-228">VMSS의 Windows 가상 컴퓨터에서 가상 컴퓨터 에이전트를 프로 비전 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-228">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="4d1db-229">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="4d1db-229">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="4d1db-230">이 배율 집합에 사용할 근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-230">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="4d1db-231">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d1db-231">-ResourceGroupName</span></span>
<span data-ttu-id="4d1db-232">VMSS가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-232">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="4d1db-233">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="4d1db-233">-ScaleInPolicy</span></span>
<span data-ttu-id="4d1db-234">가상 컴퓨터 배율 집합의 크기 조정을 할 때 따라야 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-234">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="4d1db-235">사용할 수 있는 값은 ' Default ', ' OldestVM ' 및 ' NewestVM '입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-235">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="4d1db-236">' Default ' 가상 컴퓨터 배율 집합이에서 크기를 조정 하면 영역에 대해 먼저 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-236">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="4d1db-237">그런 다음, 최대한 다양 한 장애 도메인에 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-237">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="4d1db-238">각 장애 도메인 내에서 제거 하도록 선택 된 가상 머신은 확장 기능에서 보호 되지 않는 최신 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-238">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="4d1db-239">' OldestVM ' 가상 컴퓨터 크기 조정 집합을 확장 하는 동안에는 스케일에서 보호 되지 않는 가장 오래 된 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-239">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="4d1db-240">영역 가상 컴퓨터 배율 집합의 경우에는 맨 먼저 범위에서 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-240">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="4d1db-241">각 영역 내에서 보호 되지 않는 가장 오래 된 가상 컴퓨터는 제거 하도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-241">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="4d1db-242">' NewestVM ' 가상 컴퓨터 배율 집합이 확장 되는 경우에는 스케일에서 보호 되지 않는 최신 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-242">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="4d1db-243">영역 가상 컴퓨터 배율 집합의 경우에는 맨 먼저 범위에서 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-243">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="4d1db-244">각 영역 내에서 보호 되지 않는 최신 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-244">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="4d1db-245">-Single배치 그룹</span><span class="sxs-lookup"><span data-stu-id="4d1db-245">-SinglePlacementGroup</span></span>
<span data-ttu-id="4d1db-246">단일 배치 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-246">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="4d1db-247">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="4d1db-247">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="4d1db-248">추가 과잉 프로 비전 된 Vm에서 확장이 실행 되지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-248">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="4d1db-249">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4d1db-249">-SkuCapacity</span></span>
<span data-ttu-id="4d1db-250">VMSS의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-250">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="4d1db-251">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="4d1db-251">-SkuName</span></span>
<span data-ttu-id="4d1db-252">VMSS의 모든 인스턴스 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-252">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="4d1db-253">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="4d1db-253">-SkuTier</span></span>
<span data-ttu-id="4d1db-254">VMSS의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-254">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="4d1db-255">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-255">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d1db-256">표준이</span><span class="sxs-lookup"><span data-stu-id="4d1db-256">Standard</span></span>
- <span data-ttu-id="4d1db-257">기본적</span><span class="sxs-lookup"><span data-stu-id="4d1db-257">Basic</span></span>

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

### <span data-ttu-id="4d1db-258">태그</span><span class="sxs-lookup"><span data-stu-id="4d1db-258">-Tag</span></span>
<span data-ttu-id="4d1db-259">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-259">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4d1db-260">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4d1db-260">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4d1db-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4d1db-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="4d1db-262">구성 가능한 기간 (분) 삭제 되는 가상 컴퓨터는 이벤트가 자동으로 승인 되기 전에 종료 예약 된 이벤트를 승인 해야 합니다 (시간 초과).</span><span class="sxs-lookup"><span data-stu-id="4d1db-262">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="4d1db-263">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="4d1db-263">-TerminateScheduledEvents</span></span>
<span data-ttu-id="4d1db-264">종료 예약 된 이벤트를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-264">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="4d1db-265">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="4d1db-265">-TimeZone</span></span>
<span data-ttu-id="4d1db-266">Windows OS의 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-266">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="4d1db-267">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="4d1db-267">-UltraSSDEnabled</span></span>
<span data-ttu-id="4d1db-268">하나 이상의 관리 되는 데이터 디스크를 가상 컴퓨터 크기 집합에서 UltraSSD_LRS 저장소 계정 유형과 함께 사용 하는 기능을 사용 하거나 사용 하지 않도록 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-268">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="4d1db-269">저장소 계정 유형이 UltraSSD_LRS 관리 디스크는이 속성을 사용 하도록 설정 된 경우에만 VMSS에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-269">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="4d1db-270">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="4d1db-270">-UpgradePolicyMode</span></span>
<span data-ttu-id="4d1db-271">확장 집합의 가상 컴퓨터로 업그레이드 모드를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-271">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="4d1db-272">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-272">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d1db-273">자동 번역</span><span class="sxs-lookup"><span data-stu-id="4d1db-273">Automatic</span></span>
- <span data-ttu-id="4d1db-274">수동</span><span class="sxs-lookup"><span data-stu-id="4d1db-274">Manual</span></span>
- <span data-ttu-id="4d1db-275">롤백할</span><span class="sxs-lookup"><span data-stu-id="4d1db-275">Rolling</span></span>

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

### <span data-ttu-id="4d1db-276">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="4d1db-276">-VhdContainer</span></span>
<span data-ttu-id="4d1db-277">VMSS의 운영 체제 디스크를 저장 하는 데 사용 되는 컨테이너 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-277">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="4d1db-278">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4d1db-278">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4d1db-279">로컬 VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-279">Specifies a local VMSS object.</span></span>
<span data-ttu-id="4d1db-280">VMSS 개체를 가져오려면 Get-AzVmss cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-280">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="4d1db-281">이 가상 컴퓨터 개체에는 VMSS의 업데이트 상태가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-281">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="4d1db-282">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4d1db-282">-VMScaleSetName</span></span>
<span data-ttu-id="4d1db-283">이 cmdlet이 만드는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-283">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4d1db-284">-확인</span><span class="sxs-lookup"><span data-stu-id="4d1db-284">-Confirm</span></span>
<span data-ttu-id="4d1db-285">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-285">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d1db-286">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d1db-286">-WhatIf</span></span>
<span data-ttu-id="4d1db-287">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-287">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d1db-288">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-288">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d1db-289">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1db-289">CommonParameters</span></span>
<span data-ttu-id="4d1db-290">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1db-290">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1db-291">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d1db-291">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1db-292">입력</span><span class="sxs-lookup"><span data-stu-id="4d1db-292">INPUTS</span></span>

### <span data-ttu-id="4d1db-293">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4d1db-293">System.String</span></span>

### <span data-ttu-id="4d1db-294">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="4d1db-294">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4d1db-295">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4d1db-295">System.Boolean</span></span>

## <span data-ttu-id="4d1db-296">출력</span><span class="sxs-lookup"><span data-stu-id="4d1db-296">OUTPUTS</span></span>

### <span data-ttu-id="4d1db-297">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="4d1db-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4d1db-298">상속자</span><span class="sxs-lookup"><span data-stu-id="4d1db-298">NOTES</span></span>

## <span data-ttu-id="4d1db-299">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d1db-299">RELATED LINKS</span></span>

[<span data-ttu-id="4d1db-300">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d1db-300">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="4d1db-301">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d1db-301">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="4d1db-302">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d1db-302">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="4d1db-303">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d1db-303">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="4d1db-304">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d1db-304">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="4d1db-305">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d1db-305">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="4d1db-306">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d1db-306">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


