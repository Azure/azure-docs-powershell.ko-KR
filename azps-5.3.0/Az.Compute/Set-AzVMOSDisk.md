---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495914"
---
# <span data-ttu-id="279e7-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="279e7-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="279e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="279e7-102">SYNOPSIS</span></span>
<span data-ttu-id="279e7-103">가상 머신에서 운영 체제 디스크 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="279e7-104">구문</span><span class="sxs-lookup"><span data-stu-id="279e7-104">SYNTAX</span></span>

### <span data-ttu-id="279e7-105">DefaultParamSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="279e7-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="279e7-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="279e7-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="279e7-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="279e7-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="279e7-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="279e7-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="279e7-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="279e7-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="279e7-110">설명</span><span class="sxs-lookup"><span data-stu-id="279e7-110">DESCRIPTION</span></span>
<span data-ttu-id="279e7-111">**Set-AzVMOSDisk** cmdlet은 가상 머신에서 운영 체제 디스크 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="279e7-112">예제</span><span class="sxs-lookup"><span data-stu-id="279e7-112">EXAMPLES</span></span>

### <span data-ttu-id="279e7-113">예제 1: 플랫폼 이미지에서 가상 머신의 속성 설정</span><span class="sxs-lookup"><span data-stu-id="279e7-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="279e7-114">첫 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet13이라는 가용성 집합을 얻은 다음 해당 개체를 $AvailabilitySet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="279e7-115">두 번째 명령은 가상 머신 개체를 만든 다음 가상 머신 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="279e7-116">이 명령은 가상 머신에 이름 및 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="279e7-117">가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="279e7-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="279e7-118">마지막 명령은 가상 머신의 속성을 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="279e7-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="279e7-119">예제 2: 일반화된 사용자 이미지에서 가상 머신의 속성 설정</span><span class="sxs-lookup"><span data-stu-id="279e7-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="279e7-120">첫 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet13이라는 가용성 집합을 사용하여 해당 개체를 $AvailabilitySet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="279e7-121">두 번째 명령은 가상 머신 개체를 만들고 가상 머신 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="279e7-122">이 명령은 가상 머신에 이름 및 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="279e7-123">가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="279e7-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="279e7-124">마지막 명령은 가상 머신의 속성을 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="279e7-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="279e7-125">예제 3: 특수한 사용자 이미지에서 가상 머신의 속성 설정</span><span class="sxs-lookup"><span data-stu-id="279e7-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="279e7-126">첫 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet13이라는 가용성 집합을 사용하여 해당 개체를 $AvailabilitySet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="279e7-127">두 번째 명령은 가상 머신 개체를 만들고 가상 머신 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="279e7-128">이 명령은 가상 머신에 이름 및 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="279e7-129">가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="279e7-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="279e7-130">마지막 명령은 가상 머신의 속성을 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="279e7-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="279e7-131">예제 4: 가상 머신 운영 체제 디스크에서 디스크 암호화 설정 설정</span><span class="sxs-lookup"><span data-stu-id="279e7-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="279e7-132">이 예제에서는 가상 머신 운영 체제 디스크에서 디스크 암호화 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="279e7-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="279e7-133">PARAMETERS</span></span>

### <span data-ttu-id="279e7-134">-캐싱</span><span class="sxs-lookup"><span data-stu-id="279e7-134">-Caching</span></span>
<span data-ttu-id="279e7-135">운영 체제 디스크의 캐싱 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="279e7-136">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="279e7-136">Valid values are:</span></span> 
- <span data-ttu-id="279e7-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="279e7-137">ReadOnly</span></span>
- <span data-ttu-id="279e7-138">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="279e7-139">캐싱 값을 변경하면 가상 머신이 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="279e7-140">이 설정은 디스크의 성능에 영향을 미치고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-140">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="279e7-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="279e7-141">-CreateOption</span></span>
<span data-ttu-id="279e7-142">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만드는지 또는 기존 디스크를 연결할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="279e7-143">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="279e7-143">Valid values are:</span></span> 
- <span data-ttu-id="279e7-144">연결합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-144">Attach.</span></span>
<span data-ttu-id="279e7-145">특수한 디스크에서 가상 머신을 만들 때 이 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="279e7-146">이 옵션을 지정할 때 *SourceImageUri* 매개 변수를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="279e7-147">대신, Set-AzVMSourceImage cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="279e7-148">또한 *Windows* 또는 *Linux* 매개 변수를 사용하여 Azure 플랫폼에 VHD의 운영 체제 유형을 알려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="279e7-149">*VhdUri* 매개 변수는 Azure 플랫폼에 연결할 디스크의 위치를 알려면 충분합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="279e7-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="279e7-150">FromImage.</span></span>
<span data-ttu-id="279e7-151">플랫폼 이미지 또는 일반화된 사용자 이미지에서 가상 머신을 만들 수 있도록 이 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="279e7-152">일반화된 사용자 이미지의 경우 **Set-AzVMSourceImage** cmdlet을 사용하는 대신 Azure 플랫폼에 운영 체제 디스크 VHD의 위치와 유형을 알려 주기 위해 *SourceImageUri* 매개 변수와 *Windows* 또는 *Linux* 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="279e7-153">플랫폼 이미지의 경우 *VhdUri* 매개 변수로 충분합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="279e7-154">비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-154">Empty.</span></span>

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

### <span data-ttu-id="279e7-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279e7-155">-DefaultProfile</span></span>
<span data-ttu-id="279e7-156">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="279e7-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="279e7-157">-DiffDiskSetting</span></span>
<span data-ttu-id="279e7-158">운영 체제 디스크에 대한 다른 디스크 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="279e7-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="279e7-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="279e7-160">디스크 암호화 키의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-160">Specifies the location of the disk encryption key.</span></span>

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

### <span data-ttu-id="279e7-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="279e7-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="279e7-162">디스크 암호화 키를 포함하는 Key Vault의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

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

### <span data-ttu-id="279e7-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="279e7-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="279e7-164">고객 관리 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="279e7-165">관리 디스크에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-165">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="279e7-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="279e7-166">-DiskSizeInGB</span></span>
<span data-ttu-id="279e7-167">운영 체제 디스크의 크기를 GB로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-167">Specifies the size, in GB, of the operating system disk.</span></span>

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

### <span data-ttu-id="279e7-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="279e7-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="279e7-169">키 암호화 키의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-169">Specifies the location of the key encryption key.</span></span>

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

### <span data-ttu-id="279e7-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="279e7-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="279e7-171">키 암호화 키를 포함하는 Key Vault의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

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

### <span data-ttu-id="279e7-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="279e7-172">-Linux</span></span>
<span data-ttu-id="279e7-173">사용자 이미지의 운영 체제가 Linux인 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="279e7-174">사용자 이미지 기반 가상 머신 배포에 대해 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-174">Specify this parameter for user image based virtual machine deployment.</span></span>

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

### <span data-ttu-id="279e7-175">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="279e7-175">-ManagedDiskId</span></span>
<span data-ttu-id="279e7-176">관리 디스크의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-176">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="279e7-177">-Name</span><span class="sxs-lookup"><span data-stu-id="279e7-177">-Name</span></span>
<span data-ttu-id="279e7-178">운영 체제 디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-178">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="279e7-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="279e7-179">-SourceImageUri</span></span>
<span data-ttu-id="279e7-180">사용자 이미지 시나리오에 대한 VHD의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-180">Specifies the URI of the VHD for user image scenarios.</span></span>

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

### <span data-ttu-id="279e7-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="279e7-181">-StorageAccountType</span></span>
<span data-ttu-id="279e7-182">관리 디스크의 저장소 계정 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-182">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="279e7-183">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="279e7-183">-VhdUri</span></span>
<span data-ttu-id="279e7-184">VHD(가상 하드 디스크)의 URI(Uniform Resource Identifier)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="279e7-185">이미지 기반 가상 머신의 경우 이 매개 변수는 플랫폼 이미지 또는 사용자 이미지를 지정할 때 만들 VHD 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="279e7-186">가상 머신을 시작하기 위해 이미지 BLOB(이진 큰 개체)를 복사하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="279e7-187">디스크 기반 가상 머신 부팅 시나리오의 경우 이 매개 변수는 가상 머신이 시작하는 데 직접 사용하는 VHD 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

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

### <span data-ttu-id="279e7-188">-VM</span><span class="sxs-lookup"><span data-stu-id="279e7-188">-VM</span></span>
<span data-ttu-id="279e7-189">운영 체제 디스크 속성을 설정할 로컬 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="279e7-190">가상 머신 개체를 얻습니다. Get-AzVM cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="279e7-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="279e7-191">-Windows</span></span>
<span data-ttu-id="279e7-192">사용자 이미지의 운영 체제가 Windows인 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-192">Indicates that the operating system on the user image is Windows.</span></span>

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

### <span data-ttu-id="279e7-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="279e7-193">-WriteAccelerator</span></span>
<span data-ttu-id="279e7-194">OS 디스크에서 WriteAccelerator를 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="279e7-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279e7-195">CommonParameters</span></span>
<span data-ttu-id="279e7-196">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="279e7-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279e7-197">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="279e7-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279e7-198">입력</span><span class="sxs-lookup"><span data-stu-id="279e7-198">INPUTS</span></span>

### <span data-ttu-id="279e7-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="279e7-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="279e7-200">System.String</span><span class="sxs-lookup"><span data-stu-id="279e7-200">System.String</span></span>

## <span data-ttu-id="279e7-201">출력</span><span class="sxs-lookup"><span data-stu-id="279e7-201">OUTPUTS</span></span>

### <span data-ttu-id="279e7-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="279e7-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="279e7-203">참고 사항</span><span class="sxs-lookup"><span data-stu-id="279e7-203">NOTES</span></span>

## <span data-ttu-id="279e7-204">관련 링크</span><span class="sxs-lookup"><span data-stu-id="279e7-204">RELATED LINKS</span></span>

[<span data-ttu-id="279e7-205">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="279e7-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="279e7-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="279e7-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="279e7-207">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="279e7-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


