---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 6fe6f6345f9208a524e1162fb317b88c450f3909
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701194"
---
# <span data-ttu-id="81438-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="81438-101">Update-AzVmss</span></span>

## <span data-ttu-id="81438-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81438-102">SYNOPSIS</span></span>
<span data-ttu-id="81438-103">VMSS의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="81438-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81438-104">SYNTAX</span></span>

### <span data-ttu-id="81438-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="81438-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>] [-SkuTier <String>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>] [-PlanPublisher <String>]
 [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>] [-DisableAutoRollback <Boolean>]
 [-TimeZone <String>] [-PlanPromotionCode <String>] [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>]
 [-VhdContainer <String[]>] [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-SkuName <String>] [-ImageReferenceVersion <String>]
 [-PauseTimeBetweenBatches <String>] [-ImageUri <String>] [-PlanName <String>] [-PlanProduct <String>]
 [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>] [-CustomData <String>] [-LicenseType <String>]
 [-OsDiskCaching <CachingTypes>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81438-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="81438-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 -IdentityType <ResourceIdentityType> [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SkuTier <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>]
 [-PlanPublisher <String>] [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>]
 [-DisableAutoRollback <Boolean>] [-TimeZone <String>] [-PlanPromotionCode <String>]
 [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>] [-VhdContainer <String[]>]
 [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-SkuName <String>] [-ImageReferenceVersion <String>] [-PauseTimeBetweenBatches <String>] [-ImageUri <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>]
 [-CustomData <String>] [-LicenseType <String>] [-OsDiskCaching <CachingTypes>] [-IdentityId <String[]>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81438-107">설명은</span><span class="sxs-lookup"><span data-stu-id="81438-107">DESCRIPTION</span></span>
<span data-ttu-id="81438-108">**AzVmss** CMDLET은 Vmss (가상 컴퓨터 크기 집합)의 상태를 로컬 vmss 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="81438-109">예제의</span><span class="sxs-lookup"><span data-stu-id="81438-109">EXAMPLES</span></span>

### <span data-ttu-id="81438-110">예제 1: VMSS의 상태를 로컬 VMSS 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="81438-111">이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS001 라는 VMSS의 상태를 로컬 VMSS 개체의 state로 업데이트 하 고 $LocalVMSS 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="81438-112">변수</span><span class="sxs-lookup"><span data-stu-id="81438-112">PARAMETERS</span></span>

### <span data-ttu-id="81438-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81438-113">-AsJob</span></span>
<span data-ttu-id="81438-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="81438-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="81438-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="81438-116">최신 버전의 이미지를 사용할 수 있게 되 면 이동 방식으로 확장 설정 인스턴스에 OS 업그레이드를 자동으로 적용할지 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="81438-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="81438-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="81438-118">가상 컴퓨터 크기 집합에 부팅 진단을 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="81438-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="81438-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="81438-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="81438-120">콘솔 출력과 스크린샷을 배치 하는 데 사용할 저장소 계정의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="81438-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="81438-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="81438-121">-CustomData</span></span>
<span data-ttu-id="81438-122">사용자 지정 데이터의 base-64 인코딩된 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="81438-123">이는 가상 컴퓨터에 파일로 저장 된 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="81438-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="81438-124">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="81438-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="81438-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81438-125">-DefaultProfile</span></span>
<span data-ttu-id="81438-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81438-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81438-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="81438-127">-DisableAutoRollback</span></span>
<span data-ttu-id="81438-128">자동 OS 업그레이드 정책에 대 한 자동 롤백 해제</span><span class="sxs-lookup"><span data-stu-id="81438-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="81438-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="81438-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="81438-130">이 cmdlet이 Linux OS에 대 한 암호 인증을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="81438-131">-Enable자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="81438-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="81438-132">VMSS의 Windows 가상 컴퓨터를 자동 업데이트에 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="81438-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="81438-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="81438-133">-IdentityId</span></span>
<span data-ttu-id="81438-134">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="81438-135">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="81438-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="81438-136">-IdentityType</span></span>
<span data-ttu-id="81438-137">가상 컴퓨터 크기 집합에 사용 되는 id 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="81438-138">' SystemAssignedUserAssigned ' 형식에는 암시적으로 만든 id와 사용자가 할당 한 id 집합이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81438-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="81438-139">' 없음 ' 형식은 가상 컴퓨터 배율 집합에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="81438-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="81438-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="81438-141">지정 된 SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="81438-141">SystemAssigned</span></span>
- <span data-ttu-id="81438-142">UserAssigned 됨</span><span class="sxs-lookup"><span data-stu-id="81438-142">UserAssigned</span></span>
- <span data-ttu-id="81438-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="81438-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="81438-144">않아야</span><span class="sxs-lookup"><span data-stu-id="81438-144">None</span></span>

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

### <span data-ttu-id="81438-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="81438-145">-ImageReferenceId</span></span>
<span data-ttu-id="81438-146">이미지 참조 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="81438-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="81438-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="81438-148">VMImage (가상 컴퓨터 이미지) 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="81438-149">이미지 제안을 얻으려면 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="81438-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="81438-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="81438-151">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="81438-152">게시자를 얻으려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="81438-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="81438-153">-ImageReferenceSku</span></span>
<span data-ttu-id="81438-154">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="81438-155">Sku를 가져오려면 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="81438-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="81438-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="81438-157">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="81438-158">최신 버전을 사용 하려면 특정 버전 대신 최신 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="81438-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="81438-159">-ImageUri</span></span>
<span data-ttu-id="81438-160">사용자 이미지에 대 한 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="81438-161">VMSS는 사용자 이미지의 동일한 컨테이너에서 운영 체제 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81438-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="81438-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="81438-162">-LicenseType</span></span>
<span data-ttu-id="81438-163">라이선스 종류를 지정 합니다 (사용자 고유의 라이선스 시나리오를 가져오는 데 사용).</span><span class="sxs-lookup"><span data-stu-id="81438-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="81438-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="81438-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="81438-165">관리 디스크에 대 한 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="81438-166">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="81438-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="81438-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="81438-167">StandardLRS</span></span>
- <span data-ttu-id="81438-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="81438-168">PremiumLRS</span></span>

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

### <span data-ttu-id="81438-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="81438-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="81438-170">한 일괄 처리에서 롤링 업그레이드에 의해 동시에 업그레이드 되는 총 가상 머신 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="81438-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="81438-171">이는 최대이 고 이전 또는 이후 일괄 처리에서 비정상적인 인스턴스가 있으면 일괄 처리에서 인스턴스의 백분율이 더 높은 안정성을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81438-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="81438-172">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81438-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="81438-173">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="81438-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="81438-174">업그레이드 결과 또는 롤링 업그레이드 중단 전에 가상 컴퓨터 상태 검사를 통해 비정상 상태에 있는 것으로 볼 수 있는 배율 집합의 총 가상 머신 인스턴스 중 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="81438-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="81438-175">일괄 처리를 시작 하기 전에이 제약 조건을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="81438-176">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81438-176">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="81438-177">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="81438-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="81438-178">비정상 상태에 있는 것으로 확인 될 수 있는 업그레이드 된 가상 컴퓨터 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="81438-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="81438-179">이 검사는 각 일괄 처리가 업그레이드 된 후에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="81438-180">이 백분율이 초과 되 면 롤링 업데이트가 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81438-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="81438-181">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81438-181">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="81438-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="81438-182">-OsDiskCaching</span></span>
<span data-ttu-id="81438-183">운영 체제 디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="81438-184">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="81438-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="81438-185">않아야</span><span class="sxs-lookup"><span data-stu-id="81438-185">None</span></span>
- <span data-ttu-id="81438-186">읽기</span><span class="sxs-lookup"><span data-stu-id="81438-186">ReadOnly</span></span>
- <span data-ttu-id="81438-187">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="81438-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="81438-188">캐싱 값을 변경 하면 cmdlet이 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="81438-189">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="81438-189">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="81438-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="81438-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="81438-191">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="81438-192">-과잉 프로비저닝</span><span class="sxs-lookup"><span data-stu-id="81438-192">-Overprovision</span></span>
<span data-ttu-id="81438-193">Cmdlet이 VMSS를 프로 비전 하 고 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="81438-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="81438-194">-Pausetimeenwe일괄 처리</span><span class="sxs-lookup"><span data-stu-id="81438-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="81438-195">한 일괄 처리의 모든 가상 컴퓨터에 대 한 업데이트를 완료 하 고 다음 일괄 처리를 시작 하는 대기 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="81438-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="81438-196">기간을 ISO 8601 형식으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="81438-197">기본값은 0 초 (PT0S)입니다.</span><span class="sxs-lookup"><span data-stu-id="81438-197">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="81438-198">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="81438-198">-PlanName</span></span>
<span data-ttu-id="81438-199">계획 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-199">Specifies the plan name.</span></span>

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

### <span data-ttu-id="81438-200">계획 제품</span><span class="sxs-lookup"><span data-stu-id="81438-200">-PlanProduct</span></span>
<span data-ttu-id="81438-201">계획 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-201">Specifies the plan product.</span></span>

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

### <span data-ttu-id="81438-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="81438-202">-PlanPromotionCode</span></span>
<span data-ttu-id="81438-203">계획 프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-203">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="81438-204">-계획 Publisher</span><span class="sxs-lookup"><span data-stu-id="81438-204">-PlanPublisher</span></span>
<span data-ttu-id="81438-205">계획 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-205">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="81438-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="81438-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="81438-207">VMSS의 Windows 가상 컴퓨터에서 가상 컴퓨터 에이전트를 프로 비전 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="81438-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="81438-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81438-208">-ResourceGroupName</span></span>
<span data-ttu-id="81438-209">VMSS가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="81438-210">-Single배치 그룹</span><span class="sxs-lookup"><span data-stu-id="81438-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="81438-211">단일 배치 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-211">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="81438-212">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="81438-212">-SkuCapacity</span></span>
<span data-ttu-id="81438-213">VMSS의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-213">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="81438-214">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="81438-214">-SkuName</span></span>
<span data-ttu-id="81438-215">VMSS의 모든 인스턴스 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-215">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="81438-216">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="81438-216">-SkuTier</span></span>
<span data-ttu-id="81438-217">VMSS의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="81438-218">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="81438-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="81438-219">표준이</span><span class="sxs-lookup"><span data-stu-id="81438-219">Standard</span></span>
- <span data-ttu-id="81438-220">기본적</span><span class="sxs-lookup"><span data-stu-id="81438-220">Basic</span></span>

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

### <span data-ttu-id="81438-221">태그</span><span class="sxs-lookup"><span data-stu-id="81438-221">-Tag</span></span>
<span data-ttu-id="81438-222">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="81438-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="81438-223">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="81438-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="81438-224">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="81438-224">-TimeZone</span></span>
<span data-ttu-id="81438-225">Windows OS의 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="81438-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="81438-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="81438-227">하나 이상의 관리 되는 데이터 디스크를 가상 컴퓨터 크기 집합에서 UltraSSD_LRS 저장소 계정 유형과 함께 사용 하는 기능을 사용 하거나 사용 하지 않도록 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="81438-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="81438-228">저장소 계정 유형이 UltraSSD_LRS 관리 디스크는이 속성을 사용 하도록 설정 된 경우에만 VMSS에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81438-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="81438-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="81438-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="81438-230">확장 집합의 가상 컴퓨터로 업그레이드 모드를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="81438-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="81438-231">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="81438-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="81438-232">자동 번역</span><span class="sxs-lookup"><span data-stu-id="81438-232">Automatic</span></span>
- <span data-ttu-id="81438-233">수동</span><span class="sxs-lookup"><span data-stu-id="81438-233">Manual</span></span>
- <span data-ttu-id="81438-234">롤백할</span><span class="sxs-lookup"><span data-stu-id="81438-234">Rolling</span></span>

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

### <span data-ttu-id="81438-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="81438-235">-VhdContainer</span></span>
<span data-ttu-id="81438-236">VMSS의 운영 체제 디스크를 저장 하는 데 사용 되는 컨테이너 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="81438-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="81438-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="81438-238">로컬 VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="81438-239">VMSS 개체를 가져오려면 Get-AzVmss cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-239">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="81438-240">이 가상 컴퓨터 개체에는 VMSS의 업데이트 상태가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81438-240">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="81438-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="81438-241">-VMScaleSetName</span></span>
<span data-ttu-id="81438-242">이 cmdlet이 만드는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="81438-243">-확인</span><span class="sxs-lookup"><span data-stu-id="81438-243">-Confirm</span></span>
<span data-ttu-id="81438-244">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81438-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81438-245">-WhatIf</span></span>
<span data-ttu-id="81438-246">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="81438-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81438-247">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81438-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81438-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81438-248">CommonParameters</span></span>
<span data-ttu-id="81438-249">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81438-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81438-250">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81438-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81438-251">입력</span><span class="sxs-lookup"><span data-stu-id="81438-251">INPUTS</span></span>

### <span data-ttu-id="81438-252">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="81438-252">System.String</span></span>

### <span data-ttu-id="81438-253">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="81438-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="81438-254">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="81438-254">System.Boolean</span></span>

## <span data-ttu-id="81438-255">출력</span><span class="sxs-lookup"><span data-stu-id="81438-255">OUTPUTS</span></span>

### <span data-ttu-id="81438-256">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="81438-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="81438-257">상속자</span><span class="sxs-lookup"><span data-stu-id="81438-257">NOTES</span></span>

## <span data-ttu-id="81438-258">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81438-258">RELATED LINKS</span></span>

[<span data-ttu-id="81438-259">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="81438-259">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="81438-260">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="81438-260">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="81438-261">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="81438-261">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="81438-262">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="81438-262">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="81438-263">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="81438-263">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="81438-264">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="81438-264">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="81438-265">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="81438-265">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


