---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496113"
---
# <span data-ttu-id="c2a53-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c2a53-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="c2a53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2a53-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a53-103">Vmss VM에 데이터 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="c2a53-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2a53-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2a53-105">설명</span><span class="sxs-lookup"><span data-stu-id="c2a53-105">DESCRIPTION</span></span>
<span data-ttu-id="c2a53-106">**Add-AzVmssVMDataDisk** cmdlet은 Vmss VM에 데이터 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="c2a53-107">예제</span><span class="sxs-lookup"><span data-stu-id="c2a53-107">EXAMPLES</span></span>

### <span data-ttu-id="c2a53-108">예제 1: Vmss VM에 관리되는 데이터 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="c2a53-109">첫 번째 명령은 기존 관리 디스크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="c2a53-110">다음 명령은 리소스 그룹 이름, vmss 이름 및 인스턴스 ID로 제공된 기존 Vmss VM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="c2a53-111">다음 명령은 관리 디스크를 VM에 로컬로 저장된 VM에 $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="c2a53-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="c2a53-112">마지막 명령은 추가된 데이터 디스크로 Vmss VM을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="c2a53-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2a53-113">PARAMETERS</span></span>

### <span data-ttu-id="c2a53-114">-캐싱</span><span class="sxs-lookup"><span data-stu-id="c2a53-114">-Caching</span></span>
<span data-ttu-id="c2a53-115">디스크의 캐싱 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="c2a53-116">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="c2a53-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2a53-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c2a53-117">ReadOnly</span></span>
- <span data-ttu-id="c2a53-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c2a53-118">ReadWrite</span></span>
- <span data-ttu-id="c2a53-119">None 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="c2a53-120">이 값을 변경하면 가상 머신이 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="c2a53-121">이 설정은 디스크의 일관성 및 성능에 영향을 미치고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-121">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a53-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="c2a53-122">-CreateOption</span></span>
<span data-ttu-id="c2a53-123">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만드는지, 빈 디스크를 만드는지 또는 기존 디스크를 연결할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="c2a53-124">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="c2a53-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2a53-125">연결합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-125">Attach.</span></span>
<span data-ttu-id="c2a53-126">특수한 디스크에서 가상 머신을 만들 때 이 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="c2a53-127">이 옵션을 지정할 때 *SourceImageUri* 매개 변수를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="c2a53-128">*VhdUri는* Azure 플랫폼에 VHD(가상 하드 디스크)의 위치를 가상 머신에 데이터 디스크로 연결하기 위해 필요한 모든 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="c2a53-129">비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-129">Empty.</span></span>
<span data-ttu-id="c2a53-130">빈 데이터 디스크를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="c2a53-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="c2a53-131">FromImage.</span></span>
<span data-ttu-id="c2a53-132">일반화된 이미지 또는 디스크에서 가상 머신을 만들 때 이 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="c2a53-133">이 옵션을 지정할 때 Azure 플랫폼에 데이터 디스크로 연결할 VHD의 위치를 알려 주기 위해 *SourceImageUri* 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="c2a53-134">*VhdUri* 매개 변수는 가상 머신에서 사용할 때 데이터 디스크 VHD가 저장될 위치를 식별하는 위치로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a53-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a53-135">-DefaultProfile</span></span>
<span data-ttu-id="c2a53-136">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2a53-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="c2a53-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="c2a53-138">고객 관리 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="c2a53-139">관리 디스크에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="c2a53-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="c2a53-140">-DiskSizeInGB</span></span>
<span data-ttu-id="c2a53-141">가상 머신에 연결할 빈 디스크의 크기를 기가바이트로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="c2a53-142">-Lun</span><span class="sxs-lookup"><span data-stu-id="c2a53-142">-Lun</span></span>
<span data-ttu-id="c2a53-143">데이터 디스크에 대한 LUN(논리 단위 번호)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a53-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="c2a53-144">-ManagedDiskId</span></span>
<span data-ttu-id="c2a53-145">관리 디스크의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-145">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a53-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c2a53-146">-StorageAccountType</span></span>
<span data-ttu-id="c2a53-147">관리 디스크의 저장소 계정 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="c2a53-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="c2a53-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="c2a53-149">데이터 디스크를 추가할 로컬 가상 머신 확장 집합 VM 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="c2a53-150">**Get-AzVmssVM** cmdlet을 사용하여 가상 머신 확장 집합 VM 개체를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a53-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="c2a53-151">-WriteAccelerator</span></span>
<span data-ttu-id="c2a53-152">관리되는 데이터 디스크에서 WriteAccelerator를 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="c2a53-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a53-153">CommonParameters</span></span>
<span data-ttu-id="c2a53-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a53-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a53-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c2a53-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a53-156">입력</span><span class="sxs-lookup"><span data-stu-id="c2a53-156">INPUTS</span></span>

### <span data-ttu-id="c2a53-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="c2a53-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="c2a53-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c2a53-158">System.Int32</span></span>

### <span data-ttu-id="c2a53-159">System.String</span><span class="sxs-lookup"><span data-stu-id="c2a53-159">System.String</span></span>

### <span data-ttu-id="c2a53-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="c2a53-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="c2a53-161">출력</span><span class="sxs-lookup"><span data-stu-id="c2a53-161">OUTPUTS</span></span>

### <span data-ttu-id="c2a53-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="c2a53-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="c2a53-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2a53-163">NOTES</span></span>

## <span data-ttu-id="c2a53-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2a53-164">RELATED LINKS</span></span>
