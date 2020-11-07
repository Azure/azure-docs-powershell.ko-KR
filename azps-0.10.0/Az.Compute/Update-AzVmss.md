---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 5e3bafbc667cc0e26eb6469e681ca9355b4f307f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876845"
---
# <span data-ttu-id="7349e-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7349e-101">Update-AzVmss</span></span>

## <span data-ttu-id="7349e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7349e-102">SYNOPSIS</span></span>
<span data-ttu-id="7349e-103">VMSS의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="7349e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7349e-104">SYNTAX</span></span>

### <span data-ttu-id="7349e-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="7349e-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7349e-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7349e-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] -IdentityType <ResourceIdentityType>
 [-SkuName <String>] [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>]
 [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>]
 [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7349e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7349e-107">DESCRIPTION</span></span>
<span data-ttu-id="7349e-108">**AzVmss** CMDLET은 Vmss (가상 컴퓨터 크기 집합)의 상태를 로컬 vmss 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="7349e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7349e-109">EXAMPLES</span></span>

### <span data-ttu-id="7349e-110">예제 1: VMSS의 상태를 로컬 VMSS 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="7349e-111">이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS001 라는 VMSS의 상태를 로컬 VMSS 개체의 state로 업데이트 하 고 $LocalVMSS 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="7349e-112">변수</span><span class="sxs-lookup"><span data-stu-id="7349e-112">PARAMETERS</span></span>

### <span data-ttu-id="7349e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7349e-113">-AsJob</span></span>
<span data-ttu-id="7349e-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7349e-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="7349e-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="7349e-116">최신 버전의 이미지를 사용할 수 있게 되 면 이동 방식으로 확장 설정 인스턴스에 OS 업그레이드를 자동으로 적용할지 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="7349e-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="7349e-118">가상 컴퓨터 크기 집합에 부팅 진단을 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="7349e-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="7349e-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="7349e-120">콘솔 출력과 스크린샷을 배치 하는 데 사용할 저장소 계정의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="7349e-121">-CustomData</span></span>
<span data-ttu-id="7349e-122">사용자 지정 데이터의 base-64 인코딩된 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="7349e-123">이는 가상 컴퓨터에 파일로 저장 된 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="7349e-124">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7349e-125">-DefaultProfile</span></span>
<span data-ttu-id="7349e-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7349e-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="7349e-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="7349e-128">이 cmdlet이 Linux OS에 대 한 암호 인증을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-129">-Enable자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="7349e-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="7349e-130">VMSS의 Windows 가상 컴퓨터를 자동 업데이트에 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-131">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="7349e-131">-IdentityId</span></span>
<span data-ttu-id="7349e-132">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="7349e-133">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7349e-134">-IdentityType</span></span>
<span data-ttu-id="7349e-135">가상 컴퓨터 크기 집합에 사용 되는 id 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="7349e-136">' SystemAssignedUserAssigned ' 형식에는 암시적으로 만든 id와 사용자가 할당 한 id 집합이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="7349e-137">' 없음 ' 형식은 가상 컴퓨터 배율 집합에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="7349e-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7349e-139">지정 된 SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="7349e-139">SystemAssigned</span></span>
- <span data-ttu-id="7349e-140">UserAssigned 됨</span><span class="sxs-lookup"><span data-stu-id="7349e-140">UserAssigned</span></span>
- <span data-ttu-id="7349e-141">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="7349e-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="7349e-142">않아야</span><span class="sxs-lookup"><span data-stu-id="7349e-142">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-143">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="7349e-143">-ImageReferenceId</span></span>
<span data-ttu-id="7349e-144">이미지 참조 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-144">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-145">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="7349e-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="7349e-146">VMImage (가상 컴퓨터 이미지) 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="7349e-147">이미지 제안을 얻으려면 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-147">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-148">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="7349e-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="7349e-149">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="7349e-150">게시자를 얻으려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-150">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-151">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="7349e-151">-ImageReferenceSku</span></span>
<span data-ttu-id="7349e-152">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="7349e-153">Sku를 가져오려면 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-153">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-154">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="7349e-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="7349e-155">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="7349e-156">최신 버전을 사용 하려면 특정 버전 대신 최신 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-157">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="7349e-157">-ImageUri</span></span>
<span data-ttu-id="7349e-158">사용자 이미지에 대 한 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="7349e-159">VMSS는 사용자 이미지의 동일한 컨테이너에서 운영 체제 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7349e-160">-LicenseType</span></span>
<span data-ttu-id="7349e-161">라이선스 종류를 지정 합니다 (사용자 고유의 라이선스 시나리오를 가져오는 데 사용).</span><span class="sxs-lookup"><span data-stu-id="7349e-161">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7349e-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="7349e-163">관리 디스크에 대 한 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="7349e-164">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7349e-165">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="7349e-165">StandardLRS</span></span>
- <span data-ttu-id="7349e-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="7349e-166">PremiumLRS</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-167">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="7349e-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="7349e-168">한 일괄 처리에서 롤링 업그레이드에 의해 동시에 업그레이드 되는 총 가상 머신 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="7349e-169">이는 최대이 고 이전 또는 이후 일괄 처리에서 비정상적인 인스턴스가 있으면 일괄 처리에서 인스턴스의 백분율이 더 높은 안정성을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="7349e-170">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-170">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-171">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="7349e-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="7349e-172">업그레이드 결과 또는 롤링 업그레이드 중단 전에 가상 컴퓨터 상태 검사를 통해 비정상 상태에 있는 것으로 볼 수 있는 배율 집합의 총 가상 머신 인스턴스 중 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="7349e-173">일괄 처리를 시작 하기 전에이 제약 조건을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="7349e-174">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-174">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-175">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="7349e-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="7349e-176">비정상 상태에 있는 것으로 확인 될 수 있는 업그레이드 된 가상 컴퓨터 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="7349e-177">이 검사는 각 일괄 처리가 업그레이드 된 후에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="7349e-178">이 백분율이 초과 되 면 롤링 업데이트가 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="7349e-179">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-179">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="7349e-180">-OsDiskCaching</span></span>
<span data-ttu-id="7349e-181">운영 체제 디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="7349e-182">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7349e-183">않아야</span><span class="sxs-lookup"><span data-stu-id="7349e-183">None</span></span>
- <span data-ttu-id="7349e-184">읽기</span><span class="sxs-lookup"><span data-stu-id="7349e-184">ReadOnly</span></span>
- <span data-ttu-id="7349e-185">쓰기</span><span class="sxs-lookup"><span data-stu-id="7349e-185">ReadWrite</span></span>

<span data-ttu-id="7349e-186">기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="7349e-187">캐싱 값을 변경 하면 cmdlet이 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="7349e-188">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-188">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7349e-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="7349e-190">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-191">-과잉 프로비저닝</span><span class="sxs-lookup"><span data-stu-id="7349e-191">-Overprovision</span></span>
<span data-ttu-id="7349e-192">Cmdlet이 VMSS를 프로 비전 하 고 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-193">-Pausetimeenwe일괄 처리</span><span class="sxs-lookup"><span data-stu-id="7349e-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="7349e-194">한 일괄 처리의 모든 가상 컴퓨터에 대 한 업데이트를 완료 하 고 다음 일괄 처리를 시작 하는 대기 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="7349e-195">기간을 ISO 8601 형식으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="7349e-196">기본값은 0 초 (PT0S)입니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-196">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-197">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="7349e-197">-PlanName</span></span>
<span data-ttu-id="7349e-198">계획 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-198">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-199">계획 제품</span><span class="sxs-lookup"><span data-stu-id="7349e-199">-PlanProduct</span></span>
<span data-ttu-id="7349e-200">계획 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-200">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="7349e-201">-PlanPromotionCode</span></span>
<span data-ttu-id="7349e-202">계획 프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-202">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-203">-계획 Publisher</span><span class="sxs-lookup"><span data-stu-id="7349e-203">-PlanPublisher</span></span>
<span data-ttu-id="7349e-204">계획 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-204">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="7349e-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="7349e-206">VMSS의 Windows 가상 컴퓨터에서 가상 컴퓨터 에이전트를 프로 비전 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7349e-207">-ResourceGroupName</span></span>
<span data-ttu-id="7349e-208">VMSS가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-209">-Single배치 그룹</span><span class="sxs-lookup"><span data-stu-id="7349e-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="7349e-210">단일 배치 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-210">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-211">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7349e-211">-SkuCapacity</span></span>
<span data-ttu-id="7349e-212">VMSS의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-212">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-213">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="7349e-213">-SkuName</span></span>
<span data-ttu-id="7349e-214">VMSS의 모든 인스턴스 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-214">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-215">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="7349e-215">-SkuTier</span></span>
<span data-ttu-id="7349e-216">VMSS의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="7349e-217">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7349e-218">표준이</span><span class="sxs-lookup"><span data-stu-id="7349e-218">Standard</span></span>
- <span data-ttu-id="7349e-219">기본적</span><span class="sxs-lookup"><span data-stu-id="7349e-219">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-220">태그</span><span class="sxs-lookup"><span data-stu-id="7349e-220">-Tag</span></span>
<span data-ttu-id="7349e-221">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7349e-222">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="7349e-222">For example:</span></span>

<span data-ttu-id="7349e-223">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7349e-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-224">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="7349e-224">-TimeZone</span></span>
<span data-ttu-id="7349e-225">Windows OS의 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="7349e-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="7349e-227">확장 집합의 가상 컴퓨터로 업그레이드 모드를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="7349e-228">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7349e-229">자동 번역</span><span class="sxs-lookup"><span data-stu-id="7349e-229">Automatic</span></span>
- <span data-ttu-id="7349e-230">수동</span><span class="sxs-lookup"><span data-stu-id="7349e-230">Manual</span></span>
- <span data-ttu-id="7349e-231">롤백할</span><span class="sxs-lookup"><span data-stu-id="7349e-231">Rolling</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="7349e-232">-VhdContainer</span></span>
<span data-ttu-id="7349e-233">VMSS의 운영 체제 디스크를 저장 하는 데 사용 되는 컨테이너 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7349e-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7349e-235">로컬 VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="7349e-236">VMSS 개체를 가져오려면 Get-AzVmss cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-236">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="7349e-237">이 가상 컴퓨터 개체에는 VMSS의 업데이트 상태가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-237">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7349e-238">-VMScaleSetName</span></span>
<span data-ttu-id="7349e-239">이 cmdlet이 만드는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-240">-확인</span><span class="sxs-lookup"><span data-stu-id="7349e-240">-Confirm</span></span>
<span data-ttu-id="7349e-241">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-241">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7349e-242">-WhatIf</span></span>
<span data-ttu-id="7349e-243">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7349e-244">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-244">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7349e-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7349e-245">CommonParameters</span></span>
<span data-ttu-id="7349e-246">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7349e-247">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7349e-247">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7349e-248">입력</span><span class="sxs-lookup"><span data-stu-id="7349e-248">INPUTS</span></span>

### <span data-ttu-id="7349e-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7349e-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="7349e-250">' VirtualMachineScaleSet ' 매개 변수는 파이프라인에서 ' VirtualMachineScaleSet ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7349e-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="7349e-251">출력</span><span class="sxs-lookup"><span data-stu-id="7349e-251">OUTPUTS</span></span>

### <span data-ttu-id="7349e-252">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="7349e-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7349e-253">상속자</span><span class="sxs-lookup"><span data-stu-id="7349e-253">NOTES</span></span>

## <span data-ttu-id="7349e-254">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7349e-254">RELATED LINKS</span></span>

[<span data-ttu-id="7349e-255">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7349e-255">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="7349e-256">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="7349e-256">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="7349e-257">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7349e-257">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="7349e-258">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7349e-258">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="7349e-259">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7349e-259">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="7349e-260">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7349e-260">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="7349e-261">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7349e-261">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


