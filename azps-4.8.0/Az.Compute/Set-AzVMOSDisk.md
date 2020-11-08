---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056726"
---
# <span data-ttu-id="0ea9c-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="0ea9c-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="0ea9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ea9c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea9c-103">가상 컴퓨터에서 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="0ea9c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ea9c-104">SYNTAX</span></span>

### <span data-ttu-id="0ea9c-105">DefaultParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0ea9c-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ea9c-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="0ea9c-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ea9c-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ea9c-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ea9c-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="0ea9c-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ea9c-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ea9c-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ea9c-110">설명은</span><span class="sxs-lookup"><span data-stu-id="0ea9c-110">DESCRIPTION</span></span>
<span data-ttu-id="0ea9c-111">**AzVMOSDisk** cmdlet은 가상 컴퓨터에서 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="0ea9c-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0ea9c-112">EXAMPLES</span></span>

### <span data-ttu-id="0ea9c-113">예제 1: 플랫폼 이미지에서 가상 컴퓨터의 속성 설정</span><span class="sxs-lookup"><span data-stu-id="0ea9c-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="0ea9c-114">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailabilitySet13 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="0ea9c-115">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0ea9c-116">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="0ea9c-117">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="0ea9c-118">마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="0ea9c-119">예제 2: 일반화 된 사용자 이미지의 가상 컴퓨터에 대 한 속성 설정</span><span class="sxs-lookup"><span data-stu-id="0ea9c-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="0ea9c-120">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailabilitySet13 이라는 가용성 집합을 가져와 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="0ea9c-121">두 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0ea9c-122">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="0ea9c-123">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="0ea9c-124">마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="0ea9c-125">예제 3: 특수화 된 사용자 이미지에서 가상 컴퓨터의 속성 설정</span><span class="sxs-lookup"><span data-stu-id="0ea9c-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="0ea9c-126">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailabilitySet13 이라는 가용성 집합을 가져와 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="0ea9c-127">두 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0ea9c-128">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="0ea9c-129">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="0ea9c-130">마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="0ea9c-131">예제 4: 가상 컴퓨터 운영 체제 디스크에서 디스크 암호화 설정 설정</span><span class="sxs-lookup"><span data-stu-id="0ea9c-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="0ea9c-132">이 예제에서는 가상 컴퓨터 운영 체제 디스크에 대 한 디스크 암호화 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="0ea9c-133">변수</span><span class="sxs-lookup"><span data-stu-id="0ea9c-133">PARAMETERS</span></span>

### <span data-ttu-id="0ea9c-134">-캐싱</span><span class="sxs-lookup"><span data-stu-id="0ea9c-134">-Caching</span></span>
<span data-ttu-id="0ea9c-135">운영 체제 디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="0ea9c-136">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-136">Valid values are:</span></span> 
- <span data-ttu-id="0ea9c-137">읽기</span><span class="sxs-lookup"><span data-stu-id="0ea9c-137">ReadOnly</span></span>
- <span data-ttu-id="0ea9c-138">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="0ea9c-139">캐싱 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="0ea9c-140">이 설정은 디스크의 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-140">This setting affects the performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="0ea9c-141">-CreateOption</span></span>
<span data-ttu-id="0ea9c-142">이 cmdlet이 플랫폼 또는 사용자 이미지를 사용 하 여 가상 머신에서 디스크를 만들거나 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="0ea9c-143">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-143">Valid values are:</span></span> 
- <span data-ttu-id="0ea9c-144">붙일.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-144">Attach.</span></span>
<span data-ttu-id="0ea9c-145">특수 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="0ea9c-146">이 옵션을 지정 하는 경우 *Sourceimageuri* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="0ea9c-147">대신 Set-AzVMSourceImage cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="0ea9c-148">또한 *Windows* 또는 *Linux* 를 사용 하 여 매개 변수를 사용 하 여 azure platform에 VHD의 운영 체제 유형을 알려 주어 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="0ea9c-149">*VhdUri* 매개 변수는 연결할 디스크의 위치를 azure platform에 알리는 데 충분 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="0ea9c-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-150">FromImage.</span></span>
<span data-ttu-id="0ea9c-151">플랫폼 이미지 또는 일반화 된 사용자 이미지에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="0ea9c-152">일반화 된 사용자 이미지의 경우 **AzVMSourceImage** cmdlet을 사용 하는 대신 운영 체제 디스크 VHD의 위치와 유형을 Azure 플랫폼에 알리기 위해 *Sourceimageuri* 매개 변수와 *Windows* 또는 *Linux* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="0ea9c-153">플랫폼 이미지의 경우 *VhdUri* 매개 변수만 있으면 충분 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="0ea9c-154">비울.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-154">Empty.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea9c-155">-DefaultProfile</span></span>
<span data-ttu-id="0ea9c-156">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ea9c-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="0ea9c-157">-DiffDiskSetting</span></span>
<span data-ttu-id="0ea9c-158">운영 체제 디스크에 대 한 차이점 보관용 디스크 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="0ea9c-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="0ea9c-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="0ea9c-160">디스크 암호화 키의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-160">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0ea9c-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="0ea9c-162">디스크 암호화 키를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-163">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="0ea9c-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="0ea9c-164">고객 관리 디스크 암호화 집합의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="0ea9c-165">이는 관리 디스크에 대해서만 지정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-165">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="0ea9c-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0ea9c-166">-DiskSizeInGB</span></span>
<span data-ttu-id="0ea9c-167">운영 체제 디스크의 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-167">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="0ea9c-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="0ea9c-169">키 암호화 키의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-169">Specifies the location of the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0ea9c-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="0ea9c-171">키 암호화 키를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="0ea9c-172">-Linux</span></span>
<span data-ttu-id="0ea9c-173">사용자 이미지의 운영 체제를 Linux로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="0ea9c-174">사용자 이미지 기반 가상 컴퓨터 배포에 대해이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-174">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-175">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="0ea9c-175">-ManagedDiskId</span></span>
<span data-ttu-id="0ea9c-176">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-176">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="0ea9c-177">-이름</span><span class="sxs-lookup"><span data-stu-id="0ea9c-177">-Name</span></span>
<span data-ttu-id="0ea9c-178">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-178">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="0ea9c-179">-SourceImageUri</span></span>
<span data-ttu-id="0ea9c-180">사용자 이미지 시나리오에 대 한 VHD의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-180">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0ea9c-181">-StorageAccountType</span></span>
<span data-ttu-id="0ea9c-182">관리 되는 디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-182">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="0ea9c-183">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="0ea9c-183">-VhdUri</span></span>
<span data-ttu-id="0ea9c-184">VHD (가상 하드 디스크)의 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="0ea9c-185">이미지 기반 가상 컴퓨터의 경우이 매개 변수는 플랫폼 이미지 또는 사용자 이미지가 지정 된 경우 만들 VHD 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="0ea9c-186">가상 컴퓨터를 시작 하기 위해 이미지 BLOB (이진 대형 개체)를 복사 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="0ea9c-187">디스크 기반 가상 컴퓨터 부팅 시나리오의 경우이 매개 변수는 가상 컴퓨터가 시작에 직접 사용 하는 VHD 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-188">-VM</span><span class="sxs-lookup"><span data-stu-id="0ea9c-188">-VM</span></span>
<span data-ttu-id="0ea9c-189">운영 체제 디스크 속성을 설정할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="0ea9c-190">가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="0ea9c-191">-Windows</span></span>
<span data-ttu-id="0ea9c-192">사용자 이미지의 운영 체제가 Windows 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-192">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea9c-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="0ea9c-193">-WriteAccelerator</span></span>
<span data-ttu-id="0ea9c-194">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="0ea9c-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea9c-195">CommonParameters</span></span>
<span data-ttu-id="0ea9c-196">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea9c-197">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea9c-198">입력</span><span class="sxs-lookup"><span data-stu-id="0ea9c-198">INPUTS</span></span>

### <span data-ttu-id="0ea9c-199">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0ea9c-200">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0ea9c-200">System.String</span></span>

## <span data-ttu-id="0ea9c-201">출력</span><span class="sxs-lookup"><span data-stu-id="0ea9c-201">OUTPUTS</span></span>

### <span data-ttu-id="0ea9c-202">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="0ea9c-203">상속자</span><span class="sxs-lookup"><span data-stu-id="0ea9c-203">NOTES</span></span>

## <span data-ttu-id="0ea9c-204">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ea9c-204">RELATED LINKS</span></span>

[<span data-ttu-id="0ea9c-205">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="0ea9c-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="0ea9c-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0ea9c-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="0ea9c-207">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="0ea9c-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


