---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmosdisk
schema: 2.0.0
ms.openlocfilehash: 8185b1072a6964941a4c6c837806d2df13f1cf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881105"
---
# <span data-ttu-id="50f6f-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="50f6f-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="50f6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="50f6f-103">가상 컴퓨터에서 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50f6f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50f6f-104">SYNTAX</span></span>

### <span data-ttu-id="50f6f-105">DefaultParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="50f6f-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50f6f-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="50f6f-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50f6f-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="50f6f-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50f6f-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="50f6f-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50f6f-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="50f6f-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50f6f-110">설명은</span><span class="sxs-lookup"><span data-stu-id="50f6f-110">DESCRIPTION</span></span>
<span data-ttu-id="50f6f-111">**AzureRmVMOSDisk** cmdlet은 가상 컴퓨터에서 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="50f6f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="50f6f-112">EXAMPLES</span></span>

### <span data-ttu-id="50f6f-113">예제 1: 플랫폼 이미지에서 가상 컴퓨터의 속성 설정</span><span class="sxs-lookup"><span data-stu-id="50f6f-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="50f6f-114">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet13 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="50f6f-115">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="50f6f-116">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="50f6f-117">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="50f6f-118">마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="50f6f-119">예제 2: 일반화 된 사용자 이미지의 가상 컴퓨터에 대 한 속성 설정</span><span class="sxs-lookup"><span data-stu-id="50f6f-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="50f6f-120">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet13 이라는 가용성 집합을 가져와 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="50f6f-121">두 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="50f6f-122">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="50f6f-123">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="50f6f-124">마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="50f6f-125">예제 3: 특수화 된 사용자 이미지에서 가상 컴퓨터의 속성 설정</span><span class="sxs-lookup"><span data-stu-id="50f6f-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="50f6f-126">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet13 이라는 가용성 집합을 가져와 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="50f6f-127">두 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="50f6f-128">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="50f6f-129">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="50f6f-130">마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="50f6f-131">예제 4: 가상 컴퓨터 운영 체제 디스크에서 디스크 암호화 설정 설정</span><span class="sxs-lookup"><span data-stu-id="50f6f-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="50f6f-132">이 예제에서는 가상 컴퓨터 운영 체제 디스크에 대 한 디스크 암호화 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="50f6f-133">변수</span><span class="sxs-lookup"><span data-stu-id="50f6f-133">PARAMETERS</span></span>

### <span data-ttu-id="50f6f-134">-캐싱</span><span class="sxs-lookup"><span data-stu-id="50f6f-134">-Caching</span></span>
<span data-ttu-id="50f6f-135">운영 체제 디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="50f6f-136">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-136">Valid values are:</span></span> 

- <span data-ttu-id="50f6f-137">읽기</span><span class="sxs-lookup"><span data-stu-id="50f6f-137">ReadOnly</span></span>
- <span data-ttu-id="50f6f-138">쓰기</span><span class="sxs-lookup"><span data-stu-id="50f6f-138">ReadWrite</span></span>

<span data-ttu-id="50f6f-139">기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="50f6f-140">캐싱 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="50f6f-141">이 설정은 디스크의 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-141">This setting affects the performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-142">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="50f6f-142">-CreateOption</span></span>
<span data-ttu-id="50f6f-143">이 cmdlet이 플랫폼 또는 사용자 이미지를 사용 하 여 가상 머신에서 디스크를 만들거나 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="50f6f-144">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-144">Valid values are:</span></span> 

- <span data-ttu-id="50f6f-145">붙일.</span><span class="sxs-lookup"><span data-stu-id="50f6f-145">Attach.</span></span>
<span data-ttu-id="50f6f-146">특수 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="50f6f-147">이 옵션을 지정 하는 경우 *Sourceimageuri* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="50f6f-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="50f6f-148">대신 Set-AzureRmVMSourceImage cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-148">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="50f6f-149">또한 *Windows* 또는 *Linux* 매개 변수 사용을 사용 하 여 azure2 플랫폼에 VHD의 운영 체제 유형을 알려 주어 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="50f6f-150">*VhdUri* 매개 변수는 azure2 platform에 연결할 디스크의 위치를 알려 줄 수 있을 만큼 충분 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="50f6f-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="50f6f-151">FromImage.</span></span>
<span data-ttu-id="50f6f-152">플랫폼 이미지 또는 일반화 된 사용자 이미지에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="50f6f-153">일반화 된 사용자 이미지의 경우 **AzureRmVMSourceImage** cmdlet을 사용 하는 대신 운영 체제 디스크 VHD의 위치와 유형을 Azure 플랫폼에 알리기 위해 *Sourceimageuri* 매개 변수와 *Windows* 또는 *Linux* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="50f6f-154">플랫폼 이미지의 경우 *VhdUri* 매개 변수만 있으면 충분 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="50f6f-155">비울.</span><span class="sxs-lookup"><span data-stu-id="50f6f-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f6f-156">-DefaultProfile</span></span>
<span data-ttu-id="50f6f-157">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-158">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="50f6f-158">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="50f6f-159">디스크 암호화 키의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-159">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-160">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="50f6f-160">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="50f6f-161">디스크 암호화 키를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-161">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="50f6f-162">-DiskSizeInGB</span></span>
<span data-ttu-id="50f6f-163">운영 체제 디스크의 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-163">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-164">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="50f6f-164">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="50f6f-165">키 암호화 키의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-165">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-166">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="50f6f-166">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="50f6f-167">키 암호화 키를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-167">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="50f6f-168">-Linux</span></span>
<span data-ttu-id="50f6f-169">사용자 이미지의 운영 체제를 Linux로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-169">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="50f6f-170">사용자 이미지 기반 가상 컴퓨터 배포에 대해이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-170">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-171">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="50f6f-171">-ManagedDiskId</span></span>
<span data-ttu-id="50f6f-172">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-172">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-173">-이름</span><span class="sxs-lookup"><span data-stu-id="50f6f-173">-Name</span></span>
<span data-ttu-id="50f6f-174">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-174">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-175">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="50f6f-175">-SourceImageUri</span></span>
<span data-ttu-id="50f6f-176">사용자 이미지 시나리오에 대 한 VHD의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-176">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="50f6f-177">-StorageAccountType</span></span>
<span data-ttu-id="50f6f-178">관리 되는 디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-178">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-179">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="50f6f-179">-VhdUri</span></span>
<span data-ttu-id="50f6f-180">VHD (가상 하드 디스크)의 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-180">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="50f6f-181">이미지 기반 가상 컴퓨터의 경우이 매개 변수는 플랫폼 이미지 또는 사용자 이미지가 지정 된 경우 만들 VHD 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-181">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="50f6f-182">가상 컴퓨터를 시작 하기 위해 이미지 BLOB (이진 대형 개체)를 복사 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-182">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="50f6f-183">디스크 기반 가상 컴퓨터 부팅 시나리오의 경우이 매개 변수는 가상 컴퓨터가 시작에 직접 사용 하는 VHD 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-183">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-184">-VM</span><span class="sxs-lookup"><span data-stu-id="50f6f-184">-VM</span></span>
<span data-ttu-id="50f6f-185">운영 체제 디스크 속성을 설정할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-185">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="50f6f-186">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-186">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-187">-Windows</span><span class="sxs-lookup"><span data-stu-id="50f6f-187">-Windows</span></span>
<span data-ttu-id="50f6f-188">사용자 이미지의 운영 체제가 Windows 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-188">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-189">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="50f6f-189">-WriteAccelerator</span></span>
<span data-ttu-id="50f6f-190">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f6f-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f6f-191">CommonParameters</span></span>
<span data-ttu-id="50f6f-192">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f6f-193">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50f6f-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f6f-194">입력</span><span class="sxs-lookup"><span data-stu-id="50f6f-194">INPUTS</span></span>

### <span data-ttu-id="50f6f-195">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="50f6f-195">PSVirtualMachine</span></span>
<span data-ttu-id="50f6f-196">' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-196">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="50f6f-197">출력</span><span class="sxs-lookup"><span data-stu-id="50f6f-197">OUTPUTS</span></span>

### <span data-ttu-id="50f6f-198">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f6f-198">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="50f6f-199">상속자</span><span class="sxs-lookup"><span data-stu-id="50f6f-199">NOTES</span></span>

## <span data-ttu-id="50f6f-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50f6f-200">RELATED LINKS</span></span>

[<span data-ttu-id="50f6f-201">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="50f6f-201">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="50f6f-202">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="50f6f-202">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="50f6f-203">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="50f6f-203">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


