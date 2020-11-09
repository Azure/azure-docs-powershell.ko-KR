---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308114"
---
# <span data-ttu-id="716fb-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="716fb-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="716fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="716fb-102">SYNOPSIS</span></span>
<span data-ttu-id="716fb-103">가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="716fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="716fb-104">SYNTAX</span></span>

### <span data-ttu-id="716fb-105">VmNormalDiskParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="716fb-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="716fb-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="716fb-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="716fb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="716fb-107">DESCRIPTION</span></span>
<span data-ttu-id="716fb-108">**추가-AzVMDataDisk** cmdlet은 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="716fb-109">가상 컴퓨터를 만들 때 데이터 디스크를 추가 하거나 기존 가상 컴퓨터에 데이터 디스크를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="716fb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="716fb-110">EXAMPLES</span></span>

### <span data-ttu-id="716fb-111">예제 1: 새 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="716fb-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="716fb-112">첫 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="716fb-113">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="716fb-114">다음 세 개의 명령은 1 개의 데이터 디스크 경로를 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="716fb-115">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="716fb-116">마지막 세 개의 명령은 모두 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="716fb-117">명령은 디스크의 이름과 위치, 그리고 디스크의 다른 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="716fb-118">각 디스크의 URI는 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="716fb-119">예제 2: 기존 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="716fb-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="716fb-120">첫 번째 명령은 [AzVM](./Get-AzVM.md) cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="716fb-121">명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="716fb-122">두 번째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="716fb-123">마지막 명령은 ResourceGroup11의 $VirtualMachine에 저장 된 가상 컴퓨터의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="716fb-124">예제 3: 일반화 된 사용자 이미지의 새 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="716fb-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="716fb-125">첫 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="716fb-126">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="716fb-127">다음 두 명령은 데이터 이미지 및 데이터 디스크에 대 한 경로를 $DataImageUri 및 $DataDiskUri 변수에 각각 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="716fb-128">이 접근 방식은 다음 명령의 가독성을 개선 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="716fb-129">마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="716fb-130">명령은 디스크의 이름과 다른 디스크의 속성에 대 한 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="716fb-131">예제 4: 특수 사용자 이미지의 새 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="716fb-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="716fb-132">첫 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="716fb-133">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="716fb-134">다음 명령은 데이터 디스크의 경로를 $DataDiskUri 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="716fb-135">이 접근 방식은 다음 명령의 가독성을 개선 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="716fb-136">마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="716fb-137">명령은 디스크의 이름과 위치, 그리고 디스크의 다른 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="716fb-138">변수</span><span class="sxs-lookup"><span data-stu-id="716fb-138">PARAMETERS</span></span>

### <span data-ttu-id="716fb-139">-캐싱</span><span class="sxs-lookup"><span data-stu-id="716fb-139">-Caching</span></span>
<span data-ttu-id="716fb-140">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="716fb-141">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="716fb-142">읽기</span><span class="sxs-lookup"><span data-stu-id="716fb-142">ReadOnly</span></span>
- <span data-ttu-id="716fb-143">쓰기</span><span class="sxs-lookup"><span data-stu-id="716fb-143">ReadWrite</span></span>
- <span data-ttu-id="716fb-144">없음 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="716fb-145">이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="716fb-146">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="716fb-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="716fb-147">-CreateOption</span></span>
<span data-ttu-id="716fb-148">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="716fb-149">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="716fb-150">붙일.</span><span class="sxs-lookup"><span data-stu-id="716fb-150">Attach.</span></span>
<span data-ttu-id="716fb-151">특수 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="716fb-152">이 옵션을 지정 하는 경우 *Sourceimageuri* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="716fb-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="716fb-153">*VhdUri* 는 가상 컴퓨터에 데이터 디스크로 연결할 VHD (가상 하드 디스크)의 위치를 Azure platform에 알리기 위해 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="716fb-154">비울.</span><span class="sxs-lookup"><span data-stu-id="716fb-154">Empty.</span></span>
<span data-ttu-id="716fb-155">빈 데이터 디스크를 만들려면이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="716fb-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="716fb-156">FromImage.</span></span>
<span data-ttu-id="716fb-157">일반화 된 이미지 또는 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="716fb-158">이 옵션을 지정 하는 경우 데이터 디스크로 연결할 VHD의 위치를 Azure platform에 알려 주는 데에도 *Sourceimageuri* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="716fb-159">*VhdUri* 매개 변수는 가상 머신에서 사용할 때 데이터 디스크 VHD가 저장 될 위치를 식별 하는 위치로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="716fb-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716fb-160">-DefaultProfile</span></span>
<span data-ttu-id="716fb-161">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="716fb-162">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="716fb-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="716fb-163">고객 관리 디스크 암호화 집합의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="716fb-164">이는 관리 디스크에 대해서만 지정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="716fb-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="716fb-165">-DiskSizeInGB</span></span>
<span data-ttu-id="716fb-166">가상 컴퓨터에 연결할 빈 디스크의 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="716fb-167">-Lun</span><span class="sxs-lookup"><span data-stu-id="716fb-167">-Lun</span></span>
<span data-ttu-id="716fb-168">데이터 디스크에 대 한 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="716fb-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="716fb-169">-ManagedDiskId</span></span>
<span data-ttu-id="716fb-170">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-170">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="716fb-171">-이름</span><span class="sxs-lookup"><span data-stu-id="716fb-171">-Name</span></span>
<span data-ttu-id="716fb-172">추가할 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-172">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="716fb-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="716fb-173">-SourceImageUri</span></span>
<span data-ttu-id="716fb-174">이 cmdlet이 연결 하는 디스크의 원본 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="716fb-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="716fb-175">-StorageAccountType</span></span>
<span data-ttu-id="716fb-176">관리 되는 디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-176">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="716fb-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="716fb-177">-VhdUri</span></span>
<span data-ttu-id="716fb-178">플랫폼 이미지 또는 사용자 이미지를 사용할 때 만들 VHD (가상 하드 디스크) 파일에 대 한 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="716fb-179">이 cmdlet은 이미지 blob (이진 대형 개체)를이 위치로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="716fb-180">가상 컴퓨터를 시작할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-180">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="716fb-181">-VM</span><span class="sxs-lookup"><span data-stu-id="716fb-181">-VM</span></span>
<span data-ttu-id="716fb-182">데이터 디스크를 추가할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="716fb-183">**Get-AzVM** cmdlet을 사용 하 여 가상 컴퓨터 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="716fb-184">**새 AzVMConfig** cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="716fb-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="716fb-185">-WriteAccelerator</span></span>
<span data-ttu-id="716fb-186">관리 되는 데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="716fb-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716fb-187">CommonParameters</span></span>
<span data-ttu-id="716fb-188">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716fb-189">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="716fb-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716fb-190">입력</span><span class="sxs-lookup"><span data-stu-id="716fb-190">INPUTS</span></span>

### <span data-ttu-id="716fb-191">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="716fb-192">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="716fb-192">System.String</span></span>

### <span data-ttu-id="716fb-193">Microsoft. 관리. m m/. m m 형식</span><span class="sxs-lookup"><span data-stu-id="716fb-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="716fb-194">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="716fb-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="716fb-195">출력</span><span class="sxs-lookup"><span data-stu-id="716fb-195">OUTPUTS</span></span>

### <span data-ttu-id="716fb-196">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="716fb-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="716fb-197">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="716fb-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="716fb-198">상속자</span><span class="sxs-lookup"><span data-stu-id="716fb-198">NOTES</span></span>

## <span data-ttu-id="716fb-199">관련 링크</span><span class="sxs-lookup"><span data-stu-id="716fb-199">RELATED LINKS</span></span>

[<span data-ttu-id="716fb-200">제거-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="716fb-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="716fb-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="716fb-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="716fb-202">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="716fb-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
