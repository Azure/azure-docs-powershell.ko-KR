---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194956"
---
# <span data-ttu-id="5b4a1-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="5b4a1-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="5b4a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b4a1-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4a1-103">Vmss VM의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="5b4a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b4a1-104">SYNTAX</span></span>

### <span data-ttu-id="5b4a1-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="5b4a1-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4a1-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="5b4a1-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4a1-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="5b4a1-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b4a1-108">설명</span><span class="sxs-lookup"><span data-stu-id="5b4a1-108">DESCRIPTION</span></span>
<span data-ttu-id="5b4a1-109">Vmss VM의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="5b4a1-110">지금은 유일하게 허용되는 업데이트는 관리되는 데이터 디스크를 추가하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="5b4a1-111">예제</span><span class="sxs-lookup"><span data-stu-id="5b4a1-111">EXAMPLES</span></span>

### <span data-ttu-id="5b4a1-112">예제 1: 다음을 사용하여 Vmss VM에 관리되는 데이터 디스크 New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5b4a1-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="5b4a1-113">첫 번째 명령은 기존 관리 디스크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="5b4a1-114">다음 명령은 관리 디스크를 사용하여 데이터 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="5b4a1-115">다음 명령은 리소스 그룹 이름, vmss 이름 및 인스턴스 ID로 제공된 기존 Vmss VM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="5b4a1-116">마지막 명령은 새 데이터 디스크를 추가하여 Vmss VM을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="5b4a1-117">예제 2: 다음을 사용하여 Vmss VM에 관리되는 데이터 디스크 Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5b4a1-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="5b4a1-118">첫 번째 명령은 기존 관리 디스크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="5b4a1-119">다음 명령은 리소스 그룹 이름, vmss 이름 및 인스턴스 ID로 제공된 기존 Vmss VM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="5b4a1-120">다음 명령은 관리 디스크를 VM에 로컬로 저장된 VM에 $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="5b4a1-121">마지막 명령은 추가된 데이터 디스크로 Vmss VM을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="5b4a1-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="5b4a1-122">Example 3</span></span>

<span data-ttu-id="5b4a1-123">Vmss VM의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="5b4a1-124">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="5b4a1-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="5b4a1-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b4a1-125">PARAMETERS</span></span>

### <span data-ttu-id="5b4a1-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b4a1-126">-AsJob</span></span>
<span data-ttu-id="5b4a1-127">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5b4a1-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b4a1-128">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="5b4a1-128">-DataDisk</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4a1-129">-DefaultProfile</span></span>
<span data-ttu-id="5b4a1-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b4a1-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5b4a1-131">-InstanceId</span></span>
<span data-ttu-id="5b4a1-132">VMSS VM의 인스턴스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-132">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a1-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="5b4a1-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="5b4a1-134">규모 확장 작업 중에 가상 머신 확장 집합 VM을 지우는 것으로 간주하지 말아야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="5b4a1-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="5b4a1-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="5b4a1-136">VMSS에서 시작된 모델 업데이트 또는 작업(규모 확장 포함)은 VMSS VM에 적용되지 말아야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="5b4a1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b4a1-137">-ResourceGroupName</span></span>
<span data-ttu-id="5b4a1-138">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-138">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a1-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b4a1-139">-ResourceId</span></span>
<span data-ttu-id="5b4a1-140">가상 머신 확장 집합 VM에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5b4a1-140">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a1-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="5b4a1-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="5b4a1-142">로컬 가상 머신 확장 집합 VM 개체</span><span class="sxs-lookup"><span data-stu-id="5b4a1-142">Local virtual machine scale set VM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a1-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5b4a1-143">-VMScaleSetName</span></span>
<span data-ttu-id="5b4a1-144">가상 머신 확장 집합의 이름</span><span class="sxs-lookup"><span data-stu-id="5b4a1-144">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a1-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b4a1-145">-Confirm</span></span>
<span data-ttu-id="5b4a1-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b4a1-147">-WhatIf</span></span>
<span data-ttu-id="5b4a1-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5b4a1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b4a1-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4a1-150">CommonParameters</span></span>
<span data-ttu-id="5b4a1-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4a1-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b4a1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4a1-153">입력</span><span class="sxs-lookup"><span data-stu-id="5b4a1-153">INPUTS</span></span>

### <span data-ttu-id="5b4a1-154">System.String</span><span class="sxs-lookup"><span data-stu-id="5b4a1-154">System.String</span></span>

### <span data-ttu-id="5b4a1-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="5b4a1-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="5b4a1-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="5b4a1-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="5b4a1-157">출력</span><span class="sxs-lookup"><span data-stu-id="5b4a1-157">OUTPUTS</span></span>

### <span data-ttu-id="5b4a1-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="5b4a1-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="5b4a1-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b4a1-159">NOTES</span></span>

## <span data-ttu-id="5b4a1-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b4a1-160">RELATED LINKS</span></span>
