---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 62349410e3858978166fd9c5356a8c6b568b9600
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352034"
---
# <span data-ttu-id="5dcd8-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5dcd8-101">New-AzVMConfig</span></span>

## <span data-ttu-id="5dcd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dcd8-102">SYNOPSIS</span></span>
<span data-ttu-id="5dcd8-103">구성 가능한 가상 머신 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="5dcd8-104">구문</span><span class="sxs-lookup"><span data-stu-id="5dcd8-104">SYNTAX</span></span>

### <span data-ttu-id="5dcd8-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5dcd8-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5dcd8-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dcd8-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dcd8-107">설명</span><span class="sxs-lookup"><span data-stu-id="5dcd8-107">DESCRIPTION</span></span>
<span data-ttu-id="5dcd8-108">**New-AzVMConfig** cmdlet은 Azure에 대해 구성 가능한 로컬 가상 머신 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="5dcd8-109">다른 cmdlet을 사용하여 Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface 및 Set-AzVMOSDisk와 같은 가상 머신 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="5dcd8-110">예제</span><span class="sxs-lookup"><span data-stu-id="5dcd8-110">EXAMPLES</span></span>

### <span data-ttu-id="5dcd8-111">예제 1: 가상 머신 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="5dcd8-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="5dcd8-112">첫 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 끈 다음 해당 개체를 $AvailabilitySet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="5dcd8-113">두 번째 명령은 가상 머신 개체를 만든 다음 가상 머신 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5dcd8-114">이 명령은 가상 머신에 이름 및 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="5dcd8-115">가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="5dcd8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dcd8-116">PARAMETERS</span></span>

### <span data-ttu-id="5dcd8-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="5dcd8-117">-AvailabilitySetId</span></span>
<span data-ttu-id="5dcd8-118">가용성 집합의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="5dcd8-119">가용성 집합 개체를 얻습니다. Get-AzAvailabilitySet cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="5dcd8-120">가용성 집합 개체에는 ID 속성이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="5dcd8-121">동일한 가용성 집합에 지정된 가상 머신은 가용성을 최대화하기 위해 서로 다른 노드에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="5dcd8-122">가용성 집합에 대한 자세한 내용은 가상 머신의 [가용성 관리를 참조하세요.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="5dcd8-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="5dcd8-123">Azure 계획된 유지 관리에 대한 자세한 내용은 Azure에서 가상 머신에 대한 [계획된 유지 관리 참조](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="5dcd8-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="5dcd8-124">현재 VM은 생성 시 가용성 집합에만 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="5dcd8-125">VM이 추가되는 가용성 집합은 가용성 집합 리소스와 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="5dcd8-126">기존 VM을 가용성 집합에 추가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="5dcd8-127">이 속성은 null이 아닌 properties.virtualMachineScaleSet 참조와 함께 존재할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dcd8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dcd8-128">-DefaultProfile</span></span>
<span data-ttu-id="5dcd8-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dcd8-130">-EnableUltrassd</span><span class="sxs-lookup"><span data-stu-id="5dcd8-130">-EnableUltraSSD</span></span>
<span data-ttu-id="5dcd8-131">VM에서 저장소 계정 유형이 UltraSSD_LRS 하나 이상의 관리되는 데이터 디스크를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="5dcd8-132">저장소 계정 유형이 UltraSSD_LRS 관리 디스크는 이 속성을 사용하는 UltraSSD_LRS 가상 머신에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="5dcd8-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="5dcd8-133">-EvictionPolicy</span></span>
<span data-ttu-id="5dcd8-134">Azure Spot 가상 머신에 대한 지우기 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="5dcd8-135">지원되는 값은 'Deallocate' 및 'Delete'입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="5dcd8-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="5dcd8-136">-HostId</span></span>
<span data-ttu-id="5dcd8-137">호스트의 ID</span><span class="sxs-lookup"><span data-stu-id="5dcd8-137">The Id of Host</span></span>

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

### <span data-ttu-id="5dcd8-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="5dcd8-138">-IdentityId</span></span>
<span data-ttu-id="5dcd8-139">가상 머신 확장 집합과 연결된 사용자 ID 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="5dcd8-140">사용자 ARM ID 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' 형식의 리소스 ID로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="5dcd8-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5dcd8-141">-IdentityType</span></span>
<span data-ttu-id="5dcd8-142">구성된 경우 가상 머신의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-142">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dcd8-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5dcd8-143">-LicenseType</span></span>
<span data-ttu-id="5dcd8-144">가상 머신에 대한 이미지 또는 디스크의 사용이 허가된 경우를 나타내는 라이선스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-144">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="5dcd8-145">Windows Server에 사용할 수 있는 값은</span><span class="sxs-lookup"><span data-stu-id="5dcd8-145">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="5dcd8-146">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="5dcd8-146">Windows_Client</span></span>
- <span data-ttu-id="5dcd8-147">Windows_Server Linux Server 운영 체제에 사용할 수 있는 값은</span><span class="sxs-lookup"><span data-stu-id="5dcd8-147">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="5dcd8-148">RHEL_BYOS(RHEL의 경우)</span><span class="sxs-lookup"><span data-stu-id="5dcd8-148">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="5dcd8-149">SLES_BYOS(SUSE의 경우)</span><span class="sxs-lookup"><span data-stu-id="5dcd8-149">SLES_BYOS (for SUSE)</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dcd8-150">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="5dcd8-150">-MaxPrice</span></span>
<span data-ttu-id="5dcd8-151">우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-151">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="5dcd8-152">이 가격은 미국 달러입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-152">This price is in US Dollars.</span></span> <span data-ttu-id="5dcd8-153">이 가격은 VM 크기에 대한 현재 낮은 우선 순위 가격과 비교됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-153">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="5dcd8-154">또한 우선 순위가 낮은 VM/VMSS를 만들/업데이트할 때 가격을 비교하고 maxPrice가 현재 낮은 우선 순위 가격보다 큰 경우 작업이 성공합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-154">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="5dcd8-155">또한 현재 우선 순위가 낮은 가격이 VM/VMSS를 생성한 후 maxPrice를 초과하는 경우 maxPrice는 우선 순위가 낮은 VM/VMSS를 지우는 데도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-155">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="5dcd8-156">가능한 값은 0보다 큰 모든 10진수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-156">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="5dcd8-157">예: 0.01538.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-157">Example: 0.01538.</span></span>  <span data-ttu-id="5dcd8-158">-1은 가격상의 이유로 우선 순위가 낮은 VM/VMSS를 피하지 말아야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-158">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="5dcd8-159">또한 사용자가 제공하지 않는 경우 기본 최대 가격은 -1입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-159">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="5dcd8-160">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="5dcd8-160">-EncryptionAtHost</span></span>
<span data-ttu-id="5dcd8-161">암호화AtHost 속성은 요청에서 사용자가 가상 머신 또는 가상 머신 확장 집합에 대한 호스트 암호화를 활성화하거나 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-161">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="5dcd8-162">이렇게 하면 호스트 자체의 리소스/임시 디스크를 포함한 모든 디스크에 대한 암호화가 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-162">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="5dcd8-163">기본값: 이 속성이 리소스에 대해 true로 설정되지 않으면 호스트의 암호화가 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-163">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="5dcd8-164">-Priority</span><span class="sxs-lookup"><span data-stu-id="5dcd8-164">-Priority</span></span>
<span data-ttu-id="5dcd8-165">가상 머신에 대한 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-165">The priority for the virtual machine.</span></span>  <span data-ttu-id="5dcd8-166">지원되는 값만 'Regular', 'Spot' 및 'Low'입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-166">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="5dcd8-167">'일반'은 일반 가상 머신에 대한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-167">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="5dcd8-168">'Spot'은 스폿 가상 머신에 대한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-168">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="5dcd8-169">'낮음'은 스폿 가상 머신에도 사용되지만 'Spot'로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-169">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="5dcd8-170">'낮음' 대신 'Spot'을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-170">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="5dcd8-171">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="5dcd8-171">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="5dcd8-172">이 가상 머신에 사용할 근접 배치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-172">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="5dcd8-173">-Tags</span><span class="sxs-lookup"><span data-stu-id="5dcd8-173">-Tags</span></span>
<span data-ttu-id="5dcd8-174">리소스에 연결된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-174">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dcd8-175">-VMName</span><span class="sxs-lookup"><span data-stu-id="5dcd8-175">-VMName</span></span>
<span data-ttu-id="5dcd8-176">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-176">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dcd8-177">-VMSize</span><span class="sxs-lookup"><span data-stu-id="5dcd8-177">-VMSize</span></span>
<span data-ttu-id="5dcd8-178">가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-178">Specifies the size for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dcd8-179">-VmssId</span><span class="sxs-lookup"><span data-stu-id="5dcd8-179">-VmssId</span></span>
<span data-ttu-id="5dcd8-180">가상 머신 확장 집합의 ID</span><span class="sxs-lookup"><span data-stu-id="5dcd8-180">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="5dcd8-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="5dcd8-181">-Zone</span></span>
<span data-ttu-id="5dcd8-182">가상 머신에 대한 가용성 영역 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-182">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="5dcd8-183">허용되는 값은 지역의 기능에 따라 달라 습니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-183">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="5dcd8-184">허용되는 값은 일반적으로 1,2,3입니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-184">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="5dcd8-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dcd8-185">CommonParameters</span></span>
<span data-ttu-id="5dcd8-186">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dcd8-187">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dcd8-188">입력</span><span class="sxs-lookup"><span data-stu-id="5dcd8-188">INPUTS</span></span>

### <span data-ttu-id="5dcd8-189">System.String</span><span class="sxs-lookup"><span data-stu-id="5dcd8-189">System.String</span></span>

### <span data-ttu-id="5dcd8-190">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5dcd8-190">System.String[]</span></span>

### <span data-ttu-id="5dcd8-191">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5dcd8-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5dcd8-192">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5dcd8-192">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5dcd8-193">출력</span><span class="sxs-lookup"><span data-stu-id="5dcd8-193">OUTPUTS</span></span>

### <span data-ttu-id="5dcd8-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5dcd8-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5dcd8-195">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5dcd8-195">NOTES</span></span>

## <span data-ttu-id="5dcd8-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5dcd8-196">RELATED LINKS</span></span>

[<span data-ttu-id="5dcd8-197">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5dcd8-197">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="5dcd8-198">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5dcd8-198">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="5dcd8-199">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="5dcd8-199">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="5dcd8-200">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5dcd8-200">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


