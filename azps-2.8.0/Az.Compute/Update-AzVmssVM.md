---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: bc24cab117a3ada64c4e64118b4b9b86ebffef55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697146"
---
# <span data-ttu-id="9346a-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="9346a-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="9346a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9346a-102">SYNOPSIS</span></span>
<span data-ttu-id="9346a-103">Vmss VM의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="9346a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9346a-104">SYNTAX</span></span>

### <span data-ttu-id="9346a-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="9346a-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9346a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9346a-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9346a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9346a-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9346a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9346a-108">DESCRIPTION</span></span>
<span data-ttu-id="9346a-109">Vmss VM의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="9346a-110">지금까지 허용 되는 업데이트는 관리 되는 데이터 디스크를 추가 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="9346a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9346a-111">EXAMPLES</span></span>

### <span data-ttu-id="9346a-112">예제 1: New-AzVMDataDisk를 사용 하 여 Vmss VM에 관리 되는 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="9346a-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="9346a-113">첫 번째 명령은 관리 되는 기존 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="9346a-114">다음 명령은 관리 되는 디스크를 사용 하 여 데이터 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="9346a-115">다음 명령은 리소스 그룹 이름, vmss 이름 및 인스턴스 ID로 주어진 기존 Vmss VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="9346a-116">마지막 명령은 새 데이터 디스크를 추가 하 여 Vmss VM을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="9346a-117">예제 2: Add-AzVMDataDisk 사용 하 여 Vmss VM에 관리 되는 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="9346a-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="9346a-118">첫 번째 명령은 관리 되는 기존 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="9346a-119">다음 명령은 리소스 그룹 이름, vmss 이름 및 인스턴스 ID로 주어진 기존 Vmss VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="9346a-120">다음 명령은 $VmssVM에 로컬로 저장 된 Vmss VM에 관리 되는 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="9346a-121">마지막 명령은 추가 된 데이터 디스크가 있는 Vmss VM을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="9346a-122">변수</span><span class="sxs-lookup"><span data-stu-id="9346a-122">PARAMETERS</span></span>

### <span data-ttu-id="9346a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9346a-123">-AsJob</span></span>
<span data-ttu-id="9346a-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9346a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9346a-125">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="9346a-125">-DataDisk</span></span>

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

### <span data-ttu-id="9346a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9346a-126">-DefaultProfile</span></span>
<span data-ttu-id="9346a-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9346a-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9346a-128">-InstanceId</span></span>
<span data-ttu-id="9346a-129">VMSS VM의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-129">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="9346a-130">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="9346a-130">-ProtectFromScaleIn</span></span>
<span data-ttu-id="9346a-131">확장 작업 중에 가상 컴퓨터 확장 집합 VM이 삭제로 간주 되지 않아야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-131">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="9346a-132">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="9346a-132">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="9346a-133">VMSS에 시작 된 모델 업데이트 또는 작업 (확장 기능 포함)을 VMSS VM에 적용 하지 않아야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-133">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="9346a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9346a-134">-ResourceGroupName</span></span>
<span data-ttu-id="9346a-135">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-135">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="9346a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9346a-136">-ResourceId</span></span>
<span data-ttu-id="9346a-137">가상 머신 확장 집합 VM에 대 한 리소스 id</span><span class="sxs-lookup"><span data-stu-id="9346a-137">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="9346a-138">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="9346a-138">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="9346a-139">로컬 가상 컴퓨터 크기 조정 VM 개체 설정</span><span class="sxs-lookup"><span data-stu-id="9346a-139">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="9346a-140">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9346a-140">-VMScaleSetName</span></span>
<span data-ttu-id="9346a-141">가상 머신 크기 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-141">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="9346a-142">-확인</span><span class="sxs-lookup"><span data-stu-id="9346a-142">-Confirm</span></span>
<span data-ttu-id="9346a-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9346a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9346a-144">-WhatIf</span></span>
<span data-ttu-id="9346a-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9346a-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9346a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9346a-147">CommonParameters</span></span>
<span data-ttu-id="9346a-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9346a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9346a-149">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9346a-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9346a-150">입력</span><span class="sxs-lookup"><span data-stu-id="9346a-150">INPUTS</span></span>

### <span data-ttu-id="9346a-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9346a-151">System.String</span></span>

### <span data-ttu-id="9346a-152">Microsoft. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="9346a-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="9346a-153">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="9346a-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="9346a-154">출력</span><span class="sxs-lookup"><span data-stu-id="9346a-154">OUTPUTS</span></span>

### <span data-ttu-id="9346a-155">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="9346a-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="9346a-156">상속자</span><span class="sxs-lookup"><span data-stu-id="9346a-156">NOTES</span></span>

## <span data-ttu-id="9346a-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9346a-157">RELATED LINKS</span></span>