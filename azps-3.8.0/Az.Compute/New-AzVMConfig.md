---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: a53d8cc94ffcc34ddf32d9cfec3b543b0bd006e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034906"
---
# <span data-ttu-id="ce0c1-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ce0c1-101">New-AzVMConfig</span></span>

## <span data-ttu-id="ce0c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce0c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0c1-103">구성할 수 있는 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="ce0c1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce0c1-104">SYNTAX</span></span>

### <span data-ttu-id="ce0c1-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ce0c1-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce0c1-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce0c1-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce0c1-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce0c1-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce0c1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ce0c1-108">DESCRIPTION</span></span>
<span data-ttu-id="ce0c1-109">**AzVMConfig** Cmdlet은 Azure에 대해 구성할 수 있는 로컬 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="ce0c1-110">다른 cmdlet을 사용 하 여 AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, Set-AzVMOSDisk 등의 가상 컴퓨터 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="ce0c1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ce0c1-111">EXAMPLES</span></span>

### <span data-ttu-id="ce0c1-112">예제 1: 가상 컴퓨터 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ce0c1-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="ce0c1-113">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailabilitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-113">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="ce0c1-114">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ce0c1-115">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ce0c1-116">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="ce0c1-117">변수</span><span class="sxs-lookup"><span data-stu-id="ce0c1-117">PARAMETERS</span></span>

### <span data-ttu-id="ce0c1-118">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="ce0c1-118">-AssignIdentity</span></span>
<span data-ttu-id="ce0c1-119">시스템에서 가상 컴퓨터용으로 할당 된 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0c1-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="ce0c1-120">-AvailabilitySetId</span></span>
<span data-ttu-id="ce0c1-121">가용성 집합의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="ce0c1-122">가용성 집합 개체를 가져오려면 Get-AzAvailabilitySet cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="ce0c1-123">가용성 집합 개체에 ID 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="ce0c1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0c1-124">-DefaultProfile</span></span>
<span data-ttu-id="ce0c1-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce0c1-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="ce0c1-126">-EnableUltraSSD</span></span>
<span data-ttu-id="ce0c1-127">하나 이상의 관리 되는 데이터 디스크를 VM의 UltraSSD_LRS 저장소 계정 유형과 함께 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="ce0c1-128">저장소 계정 유형이 UltraSSD_LRS 인 관리 디스크는이 속성을 사용 하도록 설정한 경우에만 가상 컴퓨터에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="ce0c1-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce0c1-129">-EvictionPolicy</span></span>
<span data-ttu-id="ce0c1-130">낮은 우선 순위의 가상 컴퓨터에 대 한 제거 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-130">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="ce0c1-131">' 할당 되지 않음 ' 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-131">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="ce0c1-132">-HostId</span><span class="sxs-lookup"><span data-stu-id="ce0c1-132">-HostId</span></span>
<span data-ttu-id="ce0c1-133">호스트의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-133">The Id of Host</span></span>

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

### <span data-ttu-id="ce0c1-134">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="ce0c1-134">-IdentityId</span></span>
<span data-ttu-id="ce0c1-135">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-135">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="ce0c1-136">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-136">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ce0c1-137">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ce0c1-137">-IdentityType</span></span>
<span data-ttu-id="ce0c1-138">가상 컴퓨터의 id입니다 (구성 된 경우).</span><span class="sxs-lookup"><span data-stu-id="ce0c1-138">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="ce0c1-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ce0c1-139">-LicenseType</span></span>
<span data-ttu-id="ce0c1-140">라이선스 형식-고유한 라이선스 시나리오를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-140">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ce0c1-141">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="ce0c1-141">-MaxPrice</span></span>
<span data-ttu-id="ce0c1-142">우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-142">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="ce0c1-143">이 가격은 미국 달러입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-143">This price is in US Dollars.</span></span> <span data-ttu-id="ce0c1-144">이 가격은 VM 크기에 대 한 현재의 낮은 우선 순위 가격과 비교 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-144">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="ce0c1-145">또한 우선 순위가 낮은 VM/VMSS의 생성/업데이트가 수행 될 때 가격이 비교 되 고 maxPrice가 현재 낮은 우선 순위의 가격 보다 더 큰 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-145">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="ce0c1-146">MaxPrice는 VM/VMSS를 만든 후 현재 낮은 우선 순위의 가격이 maxPrice를 초과 하는 경우 우선 순위가 낮은 VM/VMSS를 제거 하는 데도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-146">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="ce0c1-147">가능한 값은 다음과 같습니다. 0 보다 큰 10 진수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-147">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="ce0c1-148">예: 0.01538.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-148">Example: 0.01538.</span></span>  <span data-ttu-id="ce0c1-149">-1은 낮은 우선 순위의 VM/VMSS가 가격 이유로 제거 되어서는 안 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-149">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="ce0c1-150">또한 기본 최대 가격은 사용자가 제공 하지 않는 경우-1입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-150">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="ce0c1-151">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="ce0c1-151">-Priority</span></span>
<span data-ttu-id="ce0c1-152">가상 컴퓨터에 대 한 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-152">The priority for the virtual machine.</span></span>  <span data-ttu-id="ce0c1-153">' 일반 ', ' 스폿 ' 및 ' Low ' 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-153">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="ce0c1-154">' 일반 '은 일반 가상 컴퓨터에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-154">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="ce0c1-155">' 스폿 '은 가상 컴퓨터를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-155">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="ce0c1-156">' Low '는 스폿 가상 컴퓨터에도 사용할 수 있지만 ' 스폿 '으로 대체 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-156">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="ce0c1-157">' 낮음 ' 대신 ' 스폿 '을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-157">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="ce0c1-158">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="ce0c1-158">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="ce0c1-159">이 가상 컴퓨터에 사용할 근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-159">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="ce0c1-160">태그</span><span class="sxs-lookup"><span data-stu-id="ce0c1-160">-Tags</span></span>
<span data-ttu-id="ce0c1-161">리소스에 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-161">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="ce0c1-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="ce0c1-162">-VMName</span></span>
<span data-ttu-id="ce0c1-163">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-163">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="ce0c1-164">-VMSize</span><span class="sxs-lookup"><span data-stu-id="ce0c1-164">-VMSize</span></span>
<span data-ttu-id="ce0c1-165">가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-165">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="ce0c1-166">-VmssId</span><span class="sxs-lookup"><span data-stu-id="ce0c1-166">-VmssId</span></span>
<span data-ttu-id="ce0c1-167">가상 머신 확장 집합의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-167">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="ce0c1-168">-Zone</span><span class="sxs-lookup"><span data-stu-id="ce0c1-168">-Zone</span></span>
<span data-ttu-id="ce0c1-169">가상 컴퓨터에 대 한 가용성 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-169">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="ce0c1-170">허용 되는 값은 영역의 기능에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-170">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="ce0c1-171">허용 되는 값은 일반적으로 1, 2, 3입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-171">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="ce0c1-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0c1-172">CommonParameters</span></span>
<span data-ttu-id="ce0c1-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0c1-174">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0c1-175">입력</span><span class="sxs-lookup"><span data-stu-id="ce0c1-175">INPUTS</span></span>

### <span data-ttu-id="ce0c1-176">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ce0c1-176">System.String</span></span>

### <span data-ttu-id="ce0c1-177">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="ce0c1-177">System.String[]</span></span>

### <span data-ttu-id="ce0c1-178">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ce0c1-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ce0c1-179">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce0c1-179">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ce0c1-180">출력</span><span class="sxs-lookup"><span data-stu-id="ce0c1-180">OUTPUTS</span></span>

### <span data-ttu-id="ce0c1-181">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-181">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ce0c1-182">상속자</span><span class="sxs-lookup"><span data-stu-id="ce0c1-182">NOTES</span></span>

## <span data-ttu-id="ce0c1-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce0c1-183">RELATED LINKS</span></span>

[<span data-ttu-id="ce0c1-184">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="ce0c1-184">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="ce0c1-185">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ce0c1-185">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="ce0c1-186">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="ce0c1-186">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="ce0c1-187">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce0c1-187">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


