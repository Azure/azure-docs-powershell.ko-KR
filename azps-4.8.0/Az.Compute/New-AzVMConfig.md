---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 8c20a6be76f77a74082090d1386054a23b9b9ea0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212418"
---
# <span data-ttu-id="6fc98-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="6fc98-101">New-AzVMConfig</span></span>

## <span data-ttu-id="6fc98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fc98-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc98-103">구성할 수 있는 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="6fc98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6fc98-104">SYNTAX</span></span>

### <span data-ttu-id="6fc98-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6fc98-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fc98-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fc98-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fc98-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6fc98-107">DESCRIPTION</span></span>
<span data-ttu-id="6fc98-108">**AzVMConfig** Cmdlet은 Azure에 대해 구성할 수 있는 로컬 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="6fc98-109">다른 cmdlet을 사용 하 여 AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, Set-AzVMOSDisk 등의 가상 컴퓨터 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="6fc98-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6fc98-110">EXAMPLES</span></span>

### <span data-ttu-id="6fc98-111">예제 1: 가상 컴퓨터 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="6fc98-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="6fc98-112">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailabilitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="6fc98-113">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6fc98-114">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6fc98-115">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="6fc98-116">변수</span><span class="sxs-lookup"><span data-stu-id="6fc98-116">PARAMETERS</span></span>

### <span data-ttu-id="6fc98-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="6fc98-117">-AvailabilitySetId</span></span>
<span data-ttu-id="6fc98-118">가용성 집합의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="6fc98-119">가용성 집합 개체를 가져오려면 Get-AzAvailabilitySet cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="6fc98-120">가용성 집합 개체에 ID 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="6fc98-121">동일한 가용성 집합에 지정 된 가상 머신이 다른 노드에 할당 되어 가용성을 최대화 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="6fc98-122">가용성 집합에 대 한 자세한 내용은 [가상 컴퓨터의 가용성 관리](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6fc98-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="6fc98-123">Azure에서 예정 된 유지 관리에 대 한 자세한 내용은 [azure에서 가상 머신에 대 한 계획 된 유지 관리](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6fc98-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="6fc98-124">현재 VM은 만들 때 가용성 집합에만 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="6fc98-125">VM이 추가 되는 가용성 집합은 가용성 집합 리소스와 동일한 리소스 그룹에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="6fc98-126">기존 VM을 가용성 집합에 추가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="6fc98-127">이 속성은 null이 아닌 virtualMachineScaleSet reference와 함께 존재할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="6fc98-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc98-128">-DefaultProfile</span></span>
<span data-ttu-id="6fc98-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fc98-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="6fc98-130">-EnableUltraSSD</span></span>
<span data-ttu-id="6fc98-131">하나 이상의 관리 되는 데이터 디스크를 VM의 UltraSSD_LRS 저장소 계정 유형과 함께 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="6fc98-132">저장소 계정 유형이 UltraSSD_LRS 인 관리 디스크는이 속성을 사용 하도록 설정한 경우에만 가상 컴퓨터에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="6fc98-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="6fc98-133">-EvictionPolicy</span></span>
<span data-ttu-id="6fc98-134">Azure 스폿 가상 컴퓨터에 대 한 제거 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="6fc98-135">지원 되는 값은 ' 할당 취소 ' 및 ' 삭제 '입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="6fc98-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="6fc98-136">-HostId</span></span>
<span data-ttu-id="6fc98-137">호스트의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-137">The Id of Host</span></span>

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

### <span data-ttu-id="6fc98-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="6fc98-138">-IdentityId</span></span>
<span data-ttu-id="6fc98-139">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="6fc98-140">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="6fc98-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6fc98-141">-IdentityType</span></span>
<span data-ttu-id="6fc98-142">가상 컴퓨터의 id입니다 (구성 된 경우).</span><span class="sxs-lookup"><span data-stu-id="6fc98-142">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="6fc98-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6fc98-143">-LicenseType</span></span>
<span data-ttu-id="6fc98-144">라이선스 형식-고유한 라이선스 시나리오를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-144">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="6fc98-145">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="6fc98-145">-MaxPrice</span></span>
<span data-ttu-id="6fc98-146">우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-146">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="6fc98-147">이 가격은 미국 달러입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-147">This price is in US Dollars.</span></span> <span data-ttu-id="6fc98-148">이 가격은 VM 크기에 대 한 현재의 낮은 우선 순위 가격과 비교 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-148">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="6fc98-149">또한 우선 순위가 낮은 VM/VMSS의 생성/업데이트가 수행 될 때 가격이 비교 되 고 maxPrice가 현재 낮은 우선 순위의 가격 보다 더 큰 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-149">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="6fc98-150">MaxPrice는 VM/VMSS를 만든 후 현재 낮은 우선 순위의 가격이 maxPrice를 초과 하는 경우 우선 순위가 낮은 VM/VMSS를 제거 하는 데도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-150">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="6fc98-151">가능한 값은 다음과 같습니다. 0 보다 큰 10 진수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-151">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="6fc98-152">예: 0.01538.</span><span class="sxs-lookup"><span data-stu-id="6fc98-152">Example: 0.01538.</span></span>  <span data-ttu-id="6fc98-153">-1은 낮은 우선 순위의 VM/VMSS가 가격 이유로 제거 되어서는 안 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-153">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="6fc98-154">또한 기본 최대 가격은 사용자가 제공 하지 않는 경우-1입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-154">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="6fc98-155">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="6fc98-155">-EncryptionAtHost</span></span>
<span data-ttu-id="6fc98-156">EncryptionAtHost 속성은 사용자가 가상 컴퓨터 또는 가상 컴퓨터 크기 집합에 대 한 호스트 암호화를 사용 하거나 사용 하지 않도록 요청할 때 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-156">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="6fc98-157">이렇게 하면 호스트 자체의 리소스/임시 디스크를 포함 하 여 모든 디스크에 대 한 암호화가 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-157">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="6fc98-158">기본값: 리소스에 대해이 속성을 true로 설정 하지 않는 한 호스트의 암호화를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-158">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="6fc98-159">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="6fc98-159">-Priority</span></span>
<span data-ttu-id="6fc98-160">가상 컴퓨터에 대 한 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-160">The priority for the virtual machine.</span></span>  <span data-ttu-id="6fc98-161">' 일반 ', ' 스폿 ' 및 ' Low ' 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-161">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="6fc98-162">' 일반 '은 일반 가상 컴퓨터에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-162">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="6fc98-163">' 스폿 '은 가상 컴퓨터를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-163">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="6fc98-164">' Low '는 스폿 가상 컴퓨터에도 사용할 수 있지만 ' 스폿 '으로 대체 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-164">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="6fc98-165">' 낮음 ' 대신 ' 스폿 '을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="6fc98-165">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="6fc98-166">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="6fc98-166">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="6fc98-167">이 가상 컴퓨터에 사용할 근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-167">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="6fc98-168">태그</span><span class="sxs-lookup"><span data-stu-id="6fc98-168">-Tags</span></span>
<span data-ttu-id="6fc98-169">리소스에 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-169">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="6fc98-170">-VMName</span><span class="sxs-lookup"><span data-stu-id="6fc98-170">-VMName</span></span>
<span data-ttu-id="6fc98-171">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-171">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="6fc98-172">-VMSize</span><span class="sxs-lookup"><span data-stu-id="6fc98-172">-VMSize</span></span>
<span data-ttu-id="6fc98-173">가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-173">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="6fc98-174">-VmssId</span><span class="sxs-lookup"><span data-stu-id="6fc98-174">-VmssId</span></span>
<span data-ttu-id="6fc98-175">가상 머신 확장 집합의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-175">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="6fc98-176">-Zone</span><span class="sxs-lookup"><span data-stu-id="6fc98-176">-Zone</span></span>
<span data-ttu-id="6fc98-177">가상 컴퓨터에 대 한 가용성 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-177">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="6fc98-178">허용 되는 값은 영역의 기능에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-178">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="6fc98-179">허용 되는 값은 일반적으로 1, 2, 3입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-179">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="6fc98-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc98-180">CommonParameters</span></span>
<span data-ttu-id="6fc98-181">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc98-182">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6fc98-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc98-183">입력</span><span class="sxs-lookup"><span data-stu-id="6fc98-183">INPUTS</span></span>

### <span data-ttu-id="6fc98-184">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6fc98-184">System.String</span></span>

### <span data-ttu-id="6fc98-185">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="6fc98-185">System.String[]</span></span>

### <span data-ttu-id="6fc98-186">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="6fc98-186">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6fc98-187">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6fc98-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6fc98-188">출력</span><span class="sxs-lookup"><span data-stu-id="6fc98-188">OUTPUTS</span></span>

### <span data-ttu-id="6fc98-189">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc98-189">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6fc98-190">상속자</span><span class="sxs-lookup"><span data-stu-id="6fc98-190">NOTES</span></span>

## <span data-ttu-id="6fc98-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fc98-191">RELATED LINKS</span></span>

[<span data-ttu-id="6fc98-192">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="6fc98-192">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="6fc98-193">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="6fc98-193">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="6fc98-194">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="6fc98-194">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="6fc98-195">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6fc98-195">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


