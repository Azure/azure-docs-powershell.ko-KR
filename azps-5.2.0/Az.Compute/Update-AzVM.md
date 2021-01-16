---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366983"
---
# <span data-ttu-id="a6069-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6069-101">Update-AzVM</span></span>

## <span data-ttu-id="a6069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6069-102">SYNOPSIS</span></span>
<span data-ttu-id="a6069-103">Azure 가상 머신의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="a6069-104">구문</span><span class="sxs-lookup"><span data-stu-id="a6069-104">SYNTAX</span></span>

### <span data-ttu-id="a6069-105">ResourceGroupNameParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a6069-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6069-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6069-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6069-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a6069-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6069-108">설명</span><span class="sxs-lookup"><span data-stu-id="a6069-108">DESCRIPTION</span></span>
<span data-ttu-id="a6069-109">**Update-AzVM** cmdlet은 Azure 가상 머신의 상태를 가상 머신 개체의 상태로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="a6069-110">예제</span><span class="sxs-lookup"><span data-stu-id="a6069-110">EXAMPLES</span></span>

### <span data-ttu-id="a6069-111">예제 1: 가상 머신 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6069-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="a6069-112">이 명령은 ResourceGroup11에서 $VirtualMachine 가상 머신을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="a6069-113">이 명령은 $VirtualMachine 변수에 저장된 가상 머신 개체를 사용하여 $VirtualMachine 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a6069-114">가상 머신 개체를 얻습니다. **Get-AzVM** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="a6069-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6069-115">PARAMETERS</span></span>

### <span data-ttu-id="a6069-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6069-116">-AsJob</span></span>
<span data-ttu-id="a6069-117">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a6069-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6069-118">-DefaultProfile</span></span>
<span data-ttu-id="a6069-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6069-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="a6069-120">-HostId</span></span>
<span data-ttu-id="a6069-121">호스트의 ID</span><span class="sxs-lookup"><span data-stu-id="a6069-121">The Id of Host</span></span>

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

### <span data-ttu-id="a6069-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="a6069-122">-EncryptionAtHost</span></span>
<span data-ttu-id="a6069-123">암호화AtHost 속성은 요청에서 사용자가 가상 머신 또는 가상 머신 확장 집합에 대한 호스트 암호화를 활성화하거나 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="a6069-124">이렇게 하면 호스트 자체의 리소스/임시 디스크를 포함한 모든 디스크에 대한 암호화가 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

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

### <span data-ttu-id="a6069-125">-Id</span><span class="sxs-lookup"><span data-stu-id="a6069-125">-Id</span></span>
<span data-ttu-id="a6069-126">가상 머신의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-126">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6069-127">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="a6069-127">-IdentityId</span></span>
<span data-ttu-id="a6069-128">가상 머신과 연결된 사용자 ID 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="a6069-129">사용자 ID 참조는 ARM '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' 형식의 리소스 ID가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="a6069-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a6069-130">-IdentityType</span></span>
<span data-ttu-id="a6069-131">가상 머신에 사용되는 ID의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="a6069-132">유효한 값은 SystemAssigned, UserAssigned, SystemAssignedUserAssigned 및 None입니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="a6069-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="a6069-133">-MaxPrice</span></span>
<span data-ttu-id="a6069-134">우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="a6069-135">이 가격은 미국 달러입니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-135">This price is in US Dollars.</span></span> <span data-ttu-id="a6069-136">이 가격은 VM 크기에 대한 현재 낮은 우선 순위 가격과 비교됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="a6069-137">또한 우선 순위가 낮은 VM/VMSS를 만들/업데이트할 때 가격을 비교하고 maxPrice가 현재 낮은 우선 순위 가격보다 큰 경우 작업이 성공합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="a6069-138">또한 현재 우선 순위가 낮은 가격이 VM/VMSS를 생성한 후 maxPrice를 초과하는 경우 maxPrice는 우선 순위가 낮은 VM/VMSS를 지우는 데도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="a6069-139">가능한 값은 0보다 큰 모든 10진수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="a6069-140">예: 0.01538.</span><span class="sxs-lookup"><span data-stu-id="a6069-140">Example: 0.01538.</span></span>  <span data-ttu-id="a6069-141">-1은 가격상의 이유로 우선 순위가 낮은 VM/VMSS를 피하지 말아야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="a6069-142">또한 사용자가 제공하지 않는 경우 기본 최대 가격은 -1입니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-142">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="a6069-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a6069-143">-NoWait</span></span>
<span data-ttu-id="a6069-144">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a6069-145">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a6069-146">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="a6069-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="a6069-147">OS 디스크에서 WriteAccelerator를 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="a6069-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="a6069-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="a6069-149">이 가상 머신에 사용할 근접 배치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="a6069-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6069-150">-ResourceGroupName</span></span>
<span data-ttu-id="a6069-151">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6069-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6069-152">-Tag</span></span>
<span data-ttu-id="a6069-153">리소스 및 리소스 그룹을 이름-값 쌍 집합으로 태그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="a6069-154">리소스에 태그를 추가하면 리소스 그룹에서 리소스를 함께 그룹화하고 사용자 자신의 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="a6069-155">각 리소스 또는 리소스 그룹은 최대 15개 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="a6069-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="a6069-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="a6069-157">VM에 저장소 계정 유형이 있는 하나 이상의 관리되는 데이터 디스크를 UltraSSD_LRS 수 있는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="a6069-158">저장소 계정 유형이 UltraSSD_LRS 관리 디스크는 이 속성을 사용하는 UltraSSD_LRS 가상 머신에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="a6069-159">-VM</span><span class="sxs-lookup"><span data-stu-id="a6069-159">-VM</span></span>
<span data-ttu-id="a6069-160">로컬 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="a6069-161">가상 머신 개체를 얻습니다. Get-AzVM cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="a6069-162">이 가상 머신 개체에는 가상 머신에 대한 업데이트된 상태가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6069-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6069-163">-Confirm</span></span>
<span data-ttu-id="a6069-164">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6069-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6069-165">-WhatIf</span></span>
<span data-ttu-id="a6069-166">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a6069-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6069-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-167">The cmdlet is not run.</span></span>

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


### <span data-ttu-id="a6069-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6069-168">CommonParameters</span></span>
<span data-ttu-id="a6069-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6069-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6069-170">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6069-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6069-171">입력</span><span class="sxs-lookup"><span data-stu-id="a6069-171">INPUTS</span></span>

### <span data-ttu-id="a6069-172">System.String</span><span class="sxs-lookup"><span data-stu-id="a6069-172">System.String</span></span>

### <span data-ttu-id="a6069-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a6069-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a6069-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6069-174">System.Boolean</span></span>

## <span data-ttu-id="a6069-175">출력</span><span class="sxs-lookup"><span data-stu-id="a6069-175">OUTPUTS</span></span>

### <span data-ttu-id="a6069-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a6069-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a6069-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a6069-177">NOTES</span></span>

## <span data-ttu-id="a6069-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6069-178">RELATED LINKS</span></span>

[<span data-ttu-id="a6069-179">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6069-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a6069-180">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6069-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="a6069-181">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6069-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="a6069-182">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6069-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="a6069-183">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6069-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="a6069-184">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6069-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="a6069-185">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a6069-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


