---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 339d63fe02c8286dc5867428269dc2e2afe342d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697153"
---
# <span data-ttu-id="16823-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="16823-101">Update-AzVM</span></span>

## <span data-ttu-id="16823-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16823-102">SYNOPSIS</span></span>
<span data-ttu-id="16823-103">Azure 가상 컴퓨터의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="16823-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16823-104">SYNTAX</span></span>

### <span data-ttu-id="16823-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="16823-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16823-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="16823-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16823-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="16823-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16823-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="16823-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16823-109">설명은</span><span class="sxs-lookup"><span data-stu-id="16823-109">DESCRIPTION</span></span>
<span data-ttu-id="16823-110">**업데이트 AzVM** Cmdlet은 Azure 가상 컴퓨터의 상태를 가상 컴퓨터 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="16823-111">예제의</span><span class="sxs-lookup"><span data-stu-id="16823-111">EXAMPLES</span></span>

### <span data-ttu-id="16823-112">예제 1: 가상 컴퓨터 업데이트</span><span class="sxs-lookup"><span data-stu-id="16823-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="16823-113">이 명령은 ResourceGroup11에서 가상 머신 ($VirtualMachine)를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="16823-114">이 명령은 $VirtualMachine 변수에 저장 된 가상 컴퓨터 개체를 사용 하 여 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="16823-115">가상 컴퓨터 개체를 가져오려면 **AzVM** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="16823-116">변수</span><span class="sxs-lookup"><span data-stu-id="16823-116">PARAMETERS</span></span>

### <span data-ttu-id="16823-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16823-117">-AsJob</span></span>
<span data-ttu-id="16823-118">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="16823-119">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="16823-119">-AssignIdentity</span></span>
<span data-ttu-id="16823-120">가상 컴퓨터에 대해 시스템 할당 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-120">Specify the system-assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="16823-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16823-121">-DefaultProfile</span></span>
<span data-ttu-id="16823-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16823-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16823-123">-Id</span><span class="sxs-lookup"><span data-stu-id="16823-123">-Id</span></span>
<span data-ttu-id="16823-124">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="16823-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="16823-125">-IdentityId</span></span>
<span data-ttu-id="16823-126">가상 컴퓨터와 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="16823-127">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 Id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="16823-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="16823-128">-IdentityType</span></span>
<span data-ttu-id="16823-129">가상 컴퓨터에 사용 되는 id 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="16823-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="16823-130">유효한 값은 SystemAssigned, UserAssigned, SystemAssignedUserAssigned 및 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="16823-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="16823-131">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="16823-131">-MaxPrice</span></span>
<span data-ttu-id="16823-132">우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-132">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="16823-133">이 가격은 미국 달러입니다.</span><span class="sxs-lookup"><span data-stu-id="16823-133">This price is in US Dollars.</span></span> <span data-ttu-id="16823-134">이 가격은 VM 크기에 대 한 현재의 낮은 우선 순위 가격과 비교 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16823-134">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="16823-135">또한 우선 순위가 낮은 VM/VMSS의 생성/업데이트가 수행 될 때 가격이 비교 되 고 maxPrice가 현재 낮은 우선 순위의 가격 보다 더 큰 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-135">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="16823-136">MaxPrice는 VM/VMSS를 만든 후 현재 낮은 우선 순위의 가격이 maxPrice를 초과 하는 경우 우선 순위가 낮은 VM/VMSS를 제거 하는 데도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16823-136">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="16823-137">가능한 값은 다음과 같습니다. 0 보다 큰 10 진수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="16823-137">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="16823-138">예: 0.01538.</span><span class="sxs-lookup"><span data-stu-id="16823-138">Example: 0.01538.</span></span>  <span data-ttu-id="16823-139">-1은 낮은 우선 순위의 VM/VMSS가 가격 이유로 제거 되어서는 안 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16823-139">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="16823-140">또한 기본 최대 가격은 사용자가 제공 하지 않는 경우-1입니다.</span><span class="sxs-lookup"><span data-stu-id="16823-140">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="16823-141">-NoWait</span><span class="sxs-lookup"><span data-stu-id="16823-141">-NoWait</span></span>
<span data-ttu-id="16823-142">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-142">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="16823-143">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-143">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="16823-144">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="16823-144">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="16823-145">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-145">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="16823-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16823-146">-ResourceGroupName</span></span>
<span data-ttu-id="16823-147">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-147">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16823-148">태그</span><span class="sxs-lookup"><span data-stu-id="16823-148">-Tag</span></span>
<span data-ttu-id="16823-149">이름-값 쌍 집합을 사용 하 여 리소스 및 리소스 그룹에 태그를 지정할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-149">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="16823-150">리소스에 태그를 추가 하면 리소스 그룹에서 리소스를 그룹화 하 고 고유한 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16823-150">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="16823-151">각 리소스 또는 리소스 그룹은 최대 15 개의 태그를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16823-151">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="16823-152">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="16823-152">-UltraSSDEnabled</span></span>
<span data-ttu-id="16823-153">VM에서 저장소 계정 유형이 UltraSSD_LRS 하나 이상의 관리 되는 데이터 디스크를 포함 하는 기능을 사용 하거나 사용 하지 않도록 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="16823-153">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="16823-154">저장소 계정 유형이 UltraSSD_LRS 인 관리 디스크는이 속성을 사용 하도록 설정한 경우에만 가상 컴퓨터에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16823-154">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="16823-155">-VM</span><span class="sxs-lookup"><span data-stu-id="16823-155">-VM</span></span>
<span data-ttu-id="16823-156">로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-156">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="16823-157">가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-157">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="16823-158">이 가상 컴퓨터 개체에는 가상 컴퓨터에 대 한 업데이트 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16823-158">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="16823-159">-확인</span><span class="sxs-lookup"><span data-stu-id="16823-159">-Confirm</span></span>
<span data-ttu-id="16823-160">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16823-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16823-161">-WhatIf</span></span>
<span data-ttu-id="16823-162">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16823-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16823-163">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16823-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16823-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16823-164">CommonParameters</span></span>
<span data-ttu-id="16823-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16823-166">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="16823-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16823-167">입력</span><span class="sxs-lookup"><span data-stu-id="16823-167">INPUTS</span></span>

### <span data-ttu-id="16823-168">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="16823-168">System.String</span></span>

### <span data-ttu-id="16823-169">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="16823-169">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="16823-170">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="16823-170">System.Boolean</span></span>

## <span data-ttu-id="16823-171">출력</span><span class="sxs-lookup"><span data-stu-id="16823-171">OUTPUTS</span></span>

### <span data-ttu-id="16823-172">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="16823-172">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="16823-173">상속자</span><span class="sxs-lookup"><span data-stu-id="16823-173">NOTES</span></span>

## <span data-ttu-id="16823-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16823-174">RELATED LINKS</span></span>

[<span data-ttu-id="16823-175">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="16823-175">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="16823-176">새로운 AzVM</span><span class="sxs-lookup"><span data-stu-id="16823-176">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="16823-177">제거-AzVM</span><span class="sxs-lookup"><span data-stu-id="16823-177">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="16823-178">다시 시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="16823-178">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="16823-179">시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="16823-179">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="16823-180">중지-AzVM</span><span class="sxs-lookup"><span data-stu-id="16823-180">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="16823-181">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="16823-181">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


