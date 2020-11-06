---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: de0f5fd2583f1622e750e71299a5753444feed1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532483"
---
# <span data-ttu-id="da13c-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="da13c-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="da13c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da13c-102">SYNOPSIS</span></span>
<span data-ttu-id="da13c-103">가상 컴퓨터 또는 Vmss VM에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-103">Adds a data disk to a virtual machine or a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da13c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da13c-104">SYNTAX</span></span>

### <span data-ttu-id="da13c-105">VmNormalDiskParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="da13c-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String>
 [[-SourceImageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da13c-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="da13c-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da13c-107">VmScaleSetVMParameterSetName</span><span class="sxs-lookup"><span data-stu-id="da13c-107">VmScaleSetVMParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [-ManagedDiskId] <String>
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da13c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="da13c-108">DESCRIPTION</span></span>
<span data-ttu-id="da13c-109">**Add-AzureRmVMDataDisk** cmdlet은 데이터 디스크를 가상 컴퓨터 또는 VMSS VM에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-109">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine or a Vmss VM.</span></span>
<span data-ttu-id="da13c-110">가상 컴퓨터를 만들 때 데이터 디스크를 추가 하거나 기존 가상 컴퓨터에 데이터 디스크를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-110">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="da13c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="da13c-111">EXAMPLES</span></span>

### <span data-ttu-id="da13c-112">예제 1: 새 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="da13c-112">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="da13c-113">첫 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="da13c-114">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="da13c-115">다음 세 개의 명령은 1 개의 데이터 디스크 경로를 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-115">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="da13c-116">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-116">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="da13c-117">마지막 세 개의 명령은 모두 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-117">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="da13c-118">명령은 디스크의 이름과 위치, 그리고 디스크의 다른 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-118">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="da13c-119">각 디스크의 URI는 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-119">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="da13c-120">예제 2: 기존 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="da13c-120">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="da13c-121">첫 번째 명령은 [AzureRmVM](./Get-AzureRmVM.md) cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-121">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="da13c-122">명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-122">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="da13c-123">두 번째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-123">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="da13c-124">마지막 명령은 ResourceGroup11의 $VirtualMachine에 저장 된 가상 컴퓨터의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-124">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="da13c-125">예제 3: 일반화 된 사용자 이미지의 새 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="da13c-125">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="da13c-126">첫 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-126">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="da13c-127">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-127">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="da13c-128">다음 두 명령은 데이터 이미지 및 데이터 디스크에 대 한 경로를 $DataImageUri 및 $DataDiskUri 변수에 각각 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-128">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="da13c-129">이 접근 방식은 다음 명령의 가독성을 개선 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-129">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="da13c-130">마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-130">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="da13c-131">명령은 디스크의 이름과 다른 디스크의 속성에 대 한 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-131">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="da13c-132">예제 4: 특수 사용자 이미지의 새 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="da13c-132">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="da13c-133">첫 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-133">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="da13c-134">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-134">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="da13c-135">다음 명령은 데이터 디스크의 경로를 $DataDiskUri 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-135">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="da13c-136">이 접근 방식은 다음 명령의 가독성을 개선 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-136">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="da13c-137">마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-137">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="da13c-138">명령은 디스크의 이름과 위치, 그리고 디스크의 다른 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-138">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

### <span data-ttu-id="da13c-139">예제 5: Vmss VM에 관리 되는 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="da13c-139">Example 5: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="da13c-140">첫 번째 명령은 관리 되는 기존 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-140">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="da13c-141">다음 명령은 리소스 그룹 이름, vmss 이름 및 인스턴스 ID로 주어진 기존 Vmss VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-141">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="da13c-142">다음 명령은 $VmssVM에 로컬로 저장 된 Vmss VM에 관리 되는 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-142">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="da13c-143">마지막 명령은 추가 된 데이터 디스크가 있는 Vmss VM을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-143">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="da13c-144">변수</span><span class="sxs-lookup"><span data-stu-id="da13c-144">PARAMETERS</span></span>

### <span data-ttu-id="da13c-145">-캐싱</span><span class="sxs-lookup"><span data-stu-id="da13c-145">-Caching</span></span>
<span data-ttu-id="da13c-146">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-146">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="da13c-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da13c-148">읽기</span><span class="sxs-lookup"><span data-stu-id="da13c-148">ReadOnly</span></span>
- <span data-ttu-id="da13c-149">쓰기</span><span class="sxs-lookup"><span data-stu-id="da13c-149">ReadWrite</span></span>
- <span data-ttu-id="da13c-150">없음 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-150">None The default value is ReadWrite.</span></span>
<span data-ttu-id="da13c-151">이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-151">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="da13c-152">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-152">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-153">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="da13c-153">-CreateOption</span></span>
<span data-ttu-id="da13c-154">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-154">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="da13c-155">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da13c-156">붙일.</span><span class="sxs-lookup"><span data-stu-id="da13c-156">Attach.</span></span>
<span data-ttu-id="da13c-157">특수 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-157">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="da13c-158">이 옵션을 지정 하는 경우 *Sourceimageuri* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="da13c-158">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="da13c-159">*VhdUri* 는 가상 컴퓨터에 데이터 디스크로 연결할 VHD (가상 하드 디스크)의 위치를 Azure platform에 알리기 위해 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-159">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="da13c-160">비울.</span><span class="sxs-lookup"><span data-stu-id="da13c-160">Empty.</span></span>
<span data-ttu-id="da13c-161">빈 데이터 디스크를 만들려면이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-161">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="da13c-162">FromImage.</span><span class="sxs-lookup"><span data-stu-id="da13c-162">FromImage.</span></span>
<span data-ttu-id="da13c-163">일반화 된 이미지 또는 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-163">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="da13c-164">이 옵션을 지정 하는 경우 데이터 디스크로 연결할 VHD의 위치를 Azure platform에 알려 주는 데에도 *Sourceimageuri* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-164">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="da13c-165">*VhdUri* 매개 변수는 가상 머신에서 사용할 때 데이터 디스크 VHD가 저장 될 위치를 식별 하는 위치로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-165">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da13c-166">-DefaultProfile</span></span>
<span data-ttu-id="da13c-167">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-168">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="da13c-168">-DiskSizeInGB</span></span>
<span data-ttu-id="da13c-169">가상 컴퓨터에 연결할 빈 디스크의 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-169">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-170">-Lun</span><span class="sxs-lookup"><span data-stu-id="da13c-170">-Lun</span></span>
<span data-ttu-id="da13c-171">데이터 디스크에 대 한 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-171">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="da13c-172">-ManagedDiskId</span></span>
<span data-ttu-id="da13c-173">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-173">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-174">-이름</span><span class="sxs-lookup"><span data-stu-id="da13c-174">-Name</span></span>
<span data-ttu-id="da13c-175">추가할 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-175">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="da13c-176">-SourceImageUri</span></span>
<span data-ttu-id="da13c-177">이 cmdlet이 연결 하는 디스크의 원본 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-177">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="da13c-178">-StorageAccountType</span></span>
<span data-ttu-id="da13c-179">관리 되는 디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-179">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="da13c-180">-VhdUri</span></span>
<span data-ttu-id="da13c-181">플랫폼 이미지 또는 사용자 이미지를 사용할 때 만들 VHD (가상 하드 디스크) 파일에 대 한 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-181">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="da13c-182">이 cmdlet은 이미지 blob (이진 대형 개체)를이 위치로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-182">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="da13c-183">가상 컴퓨터를 시작할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-183">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-184">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="da13c-184">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="da13c-185">데이터 디스크를 추가할 로컬 가상 컴퓨터 크기 집합 VM 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-185">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="da13c-186">**AzureRmVmssVM** cmdlet을 사용 하 여 가상 컴퓨터 확장 집합 VM 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-186">You can use the **Get-AzureRmVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-187">-VM</span><span class="sxs-lookup"><span data-stu-id="da13c-187">-VM</span></span>
<span data-ttu-id="da13c-188">데이터 디스크를 추가할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-188">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="da13c-189">**Get-AzureRmVM** cmdlet을 사용 하 여 가상 컴퓨터 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-189">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="da13c-190">**새 AzureRmVMConfig** cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-190">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-191">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="da13c-191">-WriteAccelerator</span></span>
<span data-ttu-id="da13c-192">관리 되는 데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-192">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da13c-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da13c-193">CommonParameters</span></span>
<span data-ttu-id="da13c-194">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da13c-195">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da13c-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da13c-196">입력</span><span class="sxs-lookup"><span data-stu-id="da13c-196">INPUTS</span></span>

### <span data-ttu-id="da13c-197">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-197">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="da13c-198">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="da13c-198">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="da13c-199">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="da13c-199">System.String</span></span>

### <span data-ttu-id="da13c-200">Microsoft. 관리. m m/. m m 형식</span><span class="sxs-lookup"><span data-stu-id="da13c-200">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="da13c-201">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="da13c-201">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="da13c-202">출력</span><span class="sxs-lookup"><span data-stu-id="da13c-202">OUTPUTS</span></span>

### <span data-ttu-id="da13c-203">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="da13c-203">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="da13c-204">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="da13c-204">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="da13c-205">상속자</span><span class="sxs-lookup"><span data-stu-id="da13c-205">NOTES</span></span>

## <span data-ttu-id="da13c-206">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da13c-206">RELATED LINKS</span></span>

[<span data-ttu-id="da13c-207">제거-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="da13c-207">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="da13c-208">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="da13c-208">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="da13c-209">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="da13c-209">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
