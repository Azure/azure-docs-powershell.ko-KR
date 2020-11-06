---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMOSDisk.md
ms.openlocfilehash: 89a45e785252d1351e41e895cc610a75cbf6c5fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530390"
---
# <span data-ttu-id="b4027-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="b4027-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="b4027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4027-102">SYNOPSIS</span></span>
<span data-ttu-id="b4027-103">가상 컴퓨터에서 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4027-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4027-104">SYNTAX</span></span>

### <span data-ttu-id="b4027-105">DefaultParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b4027-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4027-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="b4027-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4027-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4027-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4027-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="b4027-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4027-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4027-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4027-110">설명은</span><span class="sxs-lookup"><span data-stu-id="b4027-110">DESCRIPTION</span></span>
<span data-ttu-id="b4027-111">**AzureRmVMOSDisk** cmdlet은 가상 컴퓨터에서 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="b4027-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b4027-112">EXAMPLES</span></span>

### <span data-ttu-id="b4027-113">예제 1: 플랫폼 이미지에서 가상 컴퓨터의 속성 설정</span><span class="sxs-lookup"><span data-stu-id="b4027-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="b4027-114">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet13 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="b4027-115">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b4027-116">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b4027-117">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="b4027-118">마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="b4027-119">예제 2: 일반화 된 사용자 이미지의 가상 컴퓨터에 대 한 속성 설정</span><span class="sxs-lookup"><span data-stu-id="b4027-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="b4027-120">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet13 이라는 가용성 집합을 가져와 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="b4027-121">두 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b4027-122">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b4027-123">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="b4027-124">마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="b4027-125">예제 3: 특수화 된 사용자 이미지에서 가상 컴퓨터의 속성 설정</span><span class="sxs-lookup"><span data-stu-id="b4027-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="b4027-126">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet13 이라는 가용성 집합을 가져와 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="b4027-127">두 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b4027-128">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b4027-129">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="b4027-130">마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="b4027-131">예제 4: 가상 컴퓨터 운영 체제 디스크에서 디스크 암호화 설정 설정</span><span class="sxs-lookup"><span data-stu-id="b4027-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="b4027-132">이 예제에서는 가상 컴퓨터 운영 체제 디스크에 대 한 디스크 암호화 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="b4027-133">변수</span><span class="sxs-lookup"><span data-stu-id="b4027-133">PARAMETERS</span></span>

### <span data-ttu-id="b4027-134">-캐싱</span><span class="sxs-lookup"><span data-stu-id="b4027-134">-Caching</span></span>
<span data-ttu-id="b4027-135">운영 체제 디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="b4027-136">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-136">Valid values are:</span></span> 
- <span data-ttu-id="b4027-137">읽기</span><span class="sxs-lookup"><span data-stu-id="b4027-137">ReadOnly</span></span>
- <span data-ttu-id="b4027-138">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="b4027-139">캐싱 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="b4027-140">이 설정은 디스크의 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-140">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="b4027-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="b4027-141">-CreateOption</span></span>
<span data-ttu-id="b4027-142">이 cmdlet이 플랫폼 또는 사용자 이미지를 사용 하 여 가상 머신에서 디스크를 만들거나 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="b4027-143">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-143">Valid values are:</span></span> 
- <span data-ttu-id="b4027-144">붙일.</span><span class="sxs-lookup"><span data-stu-id="b4027-144">Attach.</span></span>
<span data-ttu-id="b4027-145">특수 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="b4027-146">이 옵션을 지정 하는 경우 *Sourceimageuri* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="b4027-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="b4027-147">대신 Set-AzureRmVMSourceImage cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-147">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="b4027-148">또한 *Windows* 또는 *Linux* 를 사용 하 여 매개 변수를 사용 하 여 azure platform에 VHD의 운영 체제 유형을 알려 주어 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="b4027-149">*VhdUri* 매개 변수는 연결할 디스크의 위치를 azure platform에 알리는 데 충분 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="b4027-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="b4027-150">FromImage.</span></span>
<span data-ttu-id="b4027-151">플랫폼 이미지 또는 일반화 된 사용자 이미지에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="b4027-152">일반화 된 사용자 이미지의 경우 **AzureRmVMSourceImage** cmdlet을 사용 하는 대신 운영 체제 디스크 VHD의 위치와 유형을 Azure 플랫폼에 알리기 위해 *Sourceimageuri* 매개 변수와 *Windows* 또는 *Linux* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="b4027-153">플랫폼 이미지의 경우 *VhdUri* 매개 변수만 있으면 충분 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="b4027-154">비울.</span><span class="sxs-lookup"><span data-stu-id="b4027-154">Empty.</span></span>

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

### <span data-ttu-id="b4027-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4027-155">-DefaultProfile</span></span>
<span data-ttu-id="b4027-156">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4027-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="b4027-157">-DiffDiskSetting</span></span>
<span data-ttu-id="b4027-158">운영 체제 디스크에 대 한 차이점 보관용 디스크 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="b4027-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="b4027-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="b4027-160">디스크 암호화 키의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-160">Specifies the location of the disk encryption key.</span></span>

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

### <span data-ttu-id="b4027-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="b4027-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="b4027-162">디스크 암호화 키를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

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

### <span data-ttu-id="b4027-163">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="b4027-163">-DiskSizeInGB</span></span>
<span data-ttu-id="b4027-164">운영 체제 디스크의 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-164">Specifies the size, in GB, of the operating system disk.</span></span>

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

### <span data-ttu-id="b4027-165">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="b4027-165">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="b4027-166">키 암호화 키의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-166">Specifies the location of the key encryption key.</span></span>

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

### <span data-ttu-id="b4027-167">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="b4027-167">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="b4027-168">키 암호화 키를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-168">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

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

### <span data-ttu-id="b4027-169">-Linux</span><span class="sxs-lookup"><span data-stu-id="b4027-169">-Linux</span></span>
<span data-ttu-id="b4027-170">사용자 이미지의 운영 체제를 Linux로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-170">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="b4027-171">사용자 이미지 기반 가상 컴퓨터 배포에 대해이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-171">Specify this parameter for user image based virtual machine deployment.</span></span>

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

### <span data-ttu-id="b4027-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="b4027-172">-ManagedDiskId</span></span>
<span data-ttu-id="b4027-173">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-173">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="b4027-174">-이름</span><span class="sxs-lookup"><span data-stu-id="b4027-174">-Name</span></span>
<span data-ttu-id="b4027-175">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-175">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="b4027-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="b4027-176">-SourceImageUri</span></span>
<span data-ttu-id="b4027-177">사용자 이미지 시나리오에 대 한 VHD의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-177">Specifies the URI of the VHD for user image scenarios.</span></span>

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

### <span data-ttu-id="b4027-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b4027-178">-StorageAccountType</span></span>
<span data-ttu-id="b4027-179">관리 되는 디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-179">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="b4027-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="b4027-180">-VhdUri</span></span>
<span data-ttu-id="b4027-181">VHD (가상 하드 디스크)의 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-181">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="b4027-182">이미지 기반 가상 컴퓨터의 경우이 매개 변수는 플랫폼 이미지 또는 사용자 이미지가 지정 된 경우 만들 VHD 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-182">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="b4027-183">가상 컴퓨터를 시작 하기 위해 이미지 BLOB (이진 대형 개체)를 복사 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-183">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="b4027-184">디스크 기반 가상 컴퓨터 부팅 시나리오의 경우이 매개 변수는 가상 컴퓨터가 시작에 직접 사용 하는 VHD 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-184">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

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

### <span data-ttu-id="b4027-185">-VM</span><span class="sxs-lookup"><span data-stu-id="b4027-185">-VM</span></span>
<span data-ttu-id="b4027-186">운영 체제 디스크 속성을 설정할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-186">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="b4027-187">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-187">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="b4027-188">-Windows</span><span class="sxs-lookup"><span data-stu-id="b4027-188">-Windows</span></span>
<span data-ttu-id="b4027-189">사용자 이미지의 운영 체제가 Windows 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-189">Indicates that the operating system on the user image is Windows.</span></span>

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

### <span data-ttu-id="b4027-190">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b4027-190">-WriteAccelerator</span></span>
<span data-ttu-id="b4027-191">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="b4027-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4027-192">CommonParameters</span></span>
<span data-ttu-id="b4027-193">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4027-194">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4027-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4027-195">입력</span><span class="sxs-lookup"><span data-stu-id="b4027-195">INPUTS</span></span>

### <span data-ttu-id="b4027-196">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>
<span data-ttu-id="b4027-197">매개 변수: VM (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b4027-197">Parameters: VM (ByValue)</span></span>

## <span data-ttu-id="b4027-198">출력</span><span class="sxs-lookup"><span data-stu-id="b4027-198">OUTPUTS</span></span>

### <span data-ttu-id="b4027-199">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4027-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b4027-200">상속자</span><span class="sxs-lookup"><span data-stu-id="b4027-200">NOTES</span></span>

## <span data-ttu-id="b4027-201">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4027-201">RELATED LINKS</span></span>

[<span data-ttu-id="b4027-202">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b4027-202">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b4027-203">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b4027-203">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="b4027-204">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="b4027-204">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


