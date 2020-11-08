---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219084"
---
# <span data-ttu-id="1f3d5-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1f3d5-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="1f3d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f3d5-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3d5-103">Vmss VM에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="1f3d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f3d5-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f3d5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1f3d5-105">DESCRIPTION</span></span>
<span data-ttu-id="1f3d5-106">**Add-AzVmssVMDataDisk** Cmdlet은 VMSS VM에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="1f3d5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1f3d5-107">EXAMPLES</span></span>

### <span data-ttu-id="1f3d5-108">예제 1: Vmss VM에 관리 되는 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="1f3d5-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="1f3d5-109">첫 번째 명령은 관리 되는 기존 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="1f3d5-110">다음 명령은 리소스 그룹 이름, vmss 이름 및 인스턴스 ID로 주어진 기존 Vmss VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="1f3d5-111">다음 명령은 $VmssVM에 로컬로 저장 된 Vmss VM에 관리 되는 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="1f3d5-112">마지막 명령은 추가 된 데이터 디스크가 있는 Vmss VM을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="1f3d5-113">변수</span><span class="sxs-lookup"><span data-stu-id="1f3d5-113">PARAMETERS</span></span>

### <span data-ttu-id="1f3d5-114">-캐싱</span><span class="sxs-lookup"><span data-stu-id="1f3d5-114">-Caching</span></span>
<span data-ttu-id="1f3d5-115">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="1f3d5-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1f3d5-117">읽기</span><span class="sxs-lookup"><span data-stu-id="1f3d5-117">ReadOnly</span></span>
- <span data-ttu-id="1f3d5-118">쓰기</span><span class="sxs-lookup"><span data-stu-id="1f3d5-118">ReadWrite</span></span>
- <span data-ttu-id="1f3d5-119">없음 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="1f3d5-120">이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="1f3d5-121">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="1f3d5-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="1f3d5-122">-CreateOption</span></span>
<span data-ttu-id="1f3d5-123">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="1f3d5-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1f3d5-125">붙일.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-125">Attach.</span></span>
<span data-ttu-id="1f3d5-126">특수 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="1f3d5-127">이 옵션을 지정 하는 경우 *Sourceimageuri* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="1f3d5-128">*VhdUri* 는 가상 컴퓨터에 데이터 디스크로 연결할 VHD (가상 하드 디스크)의 위치를 Azure platform에 알리기 위해 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="1f3d5-129">비울.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-129">Empty.</span></span>
<span data-ttu-id="1f3d5-130">빈 데이터 디스크를 만들려면이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="1f3d5-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-131">FromImage.</span></span>
<span data-ttu-id="1f3d5-132">일반화 된 이미지 또는 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="1f3d5-133">이 옵션을 지정 하는 경우 데이터 디스크로 연결할 VHD의 위치를 Azure platform에 알려 주는 데에도 *Sourceimageuri* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="1f3d5-134">*VhdUri* 매개 변수는 가상 머신에서 사용할 때 데이터 디스크 VHD가 저장 될 위치를 식별 하는 위치로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="1f3d5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3d5-135">-DefaultProfile</span></span>
<span data-ttu-id="1f3d5-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f3d5-137">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="1f3d5-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="1f3d5-138">고객 관리 디스크 암호화 집합의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="1f3d5-139">이는 관리 디스크에 대해서만 지정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="1f3d5-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="1f3d5-140">-DiskSizeInGB</span></span>
<span data-ttu-id="1f3d5-141">가상 컴퓨터에 연결할 빈 디스크의 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="1f3d5-142">-Lun</span><span class="sxs-lookup"><span data-stu-id="1f3d5-142">-Lun</span></span>
<span data-ttu-id="1f3d5-143">데이터 디스크에 대 한 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="1f3d5-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="1f3d5-144">-ManagedDiskId</span></span>
<span data-ttu-id="1f3d5-145">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-145">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="1f3d5-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="1f3d5-146">-StorageAccountType</span></span>
<span data-ttu-id="1f3d5-147">관리 되는 디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="1f3d5-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1f3d5-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="1f3d5-149">데이터 디스크를 추가할 로컬 가상 컴퓨터 크기 집합 VM 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="1f3d5-150">**AzVmssVM** cmdlet을 사용 하 여 가상 컴퓨터 확장 집합 VM 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="1f3d5-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="1f3d5-151">-WriteAccelerator</span></span>
<span data-ttu-id="1f3d5-152">관리 되는 데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="1f3d5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3d5-153">CommonParameters</span></span>
<span data-ttu-id="1f3d5-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3d5-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3d5-156">입력</span><span class="sxs-lookup"><span data-stu-id="1f3d5-156">INPUTS</span></span>

### <span data-ttu-id="1f3d5-157">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="1f3d5-158">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-158">System.Int32</span></span>

### <span data-ttu-id="1f3d5-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f3d5-159">System.String</span></span>

### <span data-ttu-id="1f3d5-160">Microsoft. 관리. m m/. m m 형식</span><span class="sxs-lookup"><span data-stu-id="1f3d5-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="1f3d5-161">출력</span><span class="sxs-lookup"><span data-stu-id="1f3d5-161">OUTPUTS</span></span>

### <span data-ttu-id="1f3d5-162">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="1f3d5-163">상속자</span><span class="sxs-lookup"><span data-stu-id="1f3d5-163">NOTES</span></span>

## <span data-ttu-id="1f3d5-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f3d5-164">RELATED LINKS</span></span>
