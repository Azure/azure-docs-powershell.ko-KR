---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199369"
---
# <span data-ttu-id="4a1f9-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4a1f9-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="4a1f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1f9-103">가상 머신에 데이터 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="4a1f9-104">구문</span><span class="sxs-lookup"><span data-stu-id="4a1f9-104">SYNTAX</span></span>

### <span data-ttu-id="4a1f9-105">VmNormalDiskParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4a1f9-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a1f9-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4a1f9-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a1f9-107">설명</span><span class="sxs-lookup"><span data-stu-id="4a1f9-107">DESCRIPTION</span></span>
<span data-ttu-id="4a1f9-108">**Add-AzVMDataDisk** cmdlet은 가상 머신에 데이터 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="4a1f9-109">가상 머신을 만들 때 데이터 디스크를 추가하거나 기존 가상 머신에 데이터 디스크를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="4a1f9-110">예제</span><span class="sxs-lookup"><span data-stu-id="4a1f9-110">EXAMPLES</span></span>

### <span data-ttu-id="4a1f9-111">예제 1: 새 가상 머신에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="4a1f9-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="4a1f9-112">첫 번째 명령은 가상 머신 개체를 만든 다음 가상 머신 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4a1f9-113">이 명령은 가상 머신에 이름 및 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4a1f9-114">다음 세 명령은 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03 변수에 세 개의 데이터 디스크의 경로를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="4a1f9-115">이 방법은 다음 명령의 가독성에만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="4a1f9-116">마지막 세 명령은 각각 데이터 디스크를 각 명령에 저장된 가상 머신에 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4a1f9-117">이 명령은 디스크의 이름과 위치 및 디스크의 다른 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="4a1f9-118">각 디스크의 URI는 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="4a1f9-119">예제 2: 기존 가상 머신에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="4a1f9-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="4a1f9-120">첫 번째 명령은 [Get-AzVM](./Get-AzVM.md) cmdlet을 사용하여 VirtualMachine07이라는 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="4a1f9-121">이 명령은 가상 머신을 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4a1f9-122">두 번째 명령은 데이터 디스크를 데이터 디스크에 저장된 가상 머신에 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4a1f9-123">마지막 명령은 ResourceGroup11에 저장된 가상 머신의 $VirtualMachine 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="4a1f9-124">예제 3: 일반화된 사용자 이미지에서 새 가상 머신에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="4a1f9-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="4a1f9-125">첫 번째 명령은 가상 머신 개체를 만들고 가상 머신 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4a1f9-126">이 명령은 가상 머신에 이름 및 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4a1f9-127">다음 두 명령은 데이터 이미지 및 데이터 디스크에 대한 경로를 각각 $DataImageUri $DataDiskUri 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="4a1f9-128">이 방법은 다음 명령의 가독성을 향상시키는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="4a1f9-129">마지막 명령은 데이터 디스크를 데이터 디스크에 저장된 가상 머신에 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4a1f9-130">이 명령은 디스크의 이름과 위치 및 디스크의 다른 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="4a1f9-131">예제 4: 특수한 사용자 이미지에서 새 가상 머신에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="4a1f9-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="4a1f9-132">첫 번째 명령은 가상 머신 개체를 만들고 가상 머신 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4a1f9-133">이 명령은 가상 머신에 이름 및 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4a1f9-134">다음 명령은 데이터 디스크의 경로를 변수에 $DataDiskUri 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="4a1f9-135">이 방법은 다음 명령의 가독성을 향상시키는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="4a1f9-136">마지막 명령은 데이터 디스크를 데이터 디스크에 저장된 가상 머신에 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4a1f9-137">이 명령은 디스크의 이름과 위치 및 디스크의 다른 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="4a1f9-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a1f9-138">PARAMETERS</span></span>

### <span data-ttu-id="4a1f9-139">-캐싱</span><span class="sxs-lookup"><span data-stu-id="4a1f9-139">-Caching</span></span>
<span data-ttu-id="4a1f9-140">디스크의 캐싱 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="4a1f9-141">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="4a1f9-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a1f9-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4a1f9-142">ReadOnly</span></span>
- <span data-ttu-id="4a1f9-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4a1f9-143">ReadWrite</span></span>
- <span data-ttu-id="4a1f9-144">None 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="4a1f9-145">이 값을 변경하면 가상 머신이 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="4a1f9-146">이 설정은 디스크의 일관성 및 성능에 영향을 미치고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="4a1f9-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="4a1f9-147">-CreateOption</span></span>
<span data-ttu-id="4a1f9-148">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만드는지, 빈 디스크를 만드는지 또는 기존 디스크를 연결할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="4a1f9-149">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="4a1f9-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a1f9-150">연결합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-150">Attach.</span></span>
<span data-ttu-id="4a1f9-151">특수한 디스크에서 가상 머신을 만들 때 이 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="4a1f9-152">이 옵션을 지정할 때 *SourceImageUri* 매개 변수를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="4a1f9-153">*VhdUri는* Azure 플랫폼에 VHD(가상 하드 디스크)의 위치를 가상 머신에 데이터 디스크로 연결하기 위해 필요한 모든 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="4a1f9-154">비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-154">Empty.</span></span>
<span data-ttu-id="4a1f9-155">빈 데이터 디스크를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="4a1f9-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-156">FromImage.</span></span>
<span data-ttu-id="4a1f9-157">일반화된 이미지 또는 디스크에서 가상 머신을 만들 때 이 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="4a1f9-158">이 옵션을 지정할 때 Azure 플랫폼에 데이터 디스크로 연결할 VHD의 위치를 알려 주기 위해 *SourceImageUri* 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="4a1f9-159">*VhdUri* 매개 변수는 가상 머신에서 사용할 때 데이터 디스크 VHD가 저장될 위치를 식별하는 위치로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="4a1f9-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a1f9-160">-DefaultProfile</span></span>
<span data-ttu-id="4a1f9-161">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a1f9-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="4a1f9-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="4a1f9-163">고객 관리 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="4a1f9-164">관리 디스크에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="4a1f9-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="4a1f9-165">-DiskSizeInGB</span></span>
<span data-ttu-id="4a1f9-166">가상 머신에 연결할 빈 디스크의 크기를 기가바이트로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="4a1f9-167">-Lun</span><span class="sxs-lookup"><span data-stu-id="4a1f9-167">-Lun</span></span>
<span data-ttu-id="4a1f9-168">데이터 디스크에 대한 LUN(논리 단위 번호)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="4a1f9-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="4a1f9-169">-ManagedDiskId</span></span>
<span data-ttu-id="4a1f9-170">관리 디스크의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-170">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="4a1f9-171">-Name</span><span class="sxs-lookup"><span data-stu-id="4a1f9-171">-Name</span></span>
<span data-ttu-id="4a1f9-172">추가할 데이터 디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-172">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1f9-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="4a1f9-173">-SourceImageUri</span></span>
<span data-ttu-id="4a1f9-174">이 cmdlet이 연결한 디스크의 원본 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="4a1f9-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4a1f9-175">-StorageAccountType</span></span>
<span data-ttu-id="4a1f9-176">관리 디스크의 저장소 계정 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1f9-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="4a1f9-177">-VhdUri</span></span>
<span data-ttu-id="4a1f9-178">플랫폼 이미지 또는 사용자 이미지를 사용할 때 만들 VHD(가상 하드 디스크) 파일에 대한 URI(Uniform Resource Identifier)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="4a1f9-179">이 cmdlet은 이미지 이진 큰 개체(Blob)를 이 위치에 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="4a1f9-180">가상 머신을 시작할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-180">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="4a1f9-181">-VM</span><span class="sxs-lookup"><span data-stu-id="4a1f9-181">-VM</span></span>
<span data-ttu-id="4a1f9-182">데이터 디스크를 추가할 로컬 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="4a1f9-183">**Get-AzVM** cmdlet을 사용하여 가상 머신 개체를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="4a1f9-184">**New-AzVMConfig** cmdlet을 사용하여 가상 머신 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1f9-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4a1f9-185">-WriteAccelerator</span></span>
<span data-ttu-id="4a1f9-186">관리되는 데이터 디스크에서 WriteAccelerator를 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a1f9-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1f9-187">CommonParameters</span></span>
<span data-ttu-id="4a1f9-188">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1f9-189">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a1f9-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1f9-190">입력</span><span class="sxs-lookup"><span data-stu-id="4a1f9-190">INPUTS</span></span>

### <span data-ttu-id="4a1f9-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4a1f9-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4a1f9-192">System.String</span><span class="sxs-lookup"><span data-stu-id="4a1f9-192">System.String</span></span>

### <span data-ttu-id="4a1f9-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="4a1f9-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="4a1f9-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4a1f9-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4a1f9-195">출력</span><span class="sxs-lookup"><span data-stu-id="4a1f9-195">OUTPUTS</span></span>

### <span data-ttu-id="4a1f9-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4a1f9-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4a1f9-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4a1f9-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="4a1f9-198">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a1f9-198">NOTES</span></span>

## <span data-ttu-id="4a1f9-199">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a1f9-199">RELATED LINKS</span></span>

[<span data-ttu-id="4a1f9-200">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4a1f9-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="4a1f9-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4a1f9-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4a1f9-202">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4a1f9-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)