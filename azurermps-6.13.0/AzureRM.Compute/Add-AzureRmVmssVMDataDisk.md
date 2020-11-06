---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssVMDataDisk.md
ms.openlocfilehash: c4a4aa530f29de93458f618dbf45f639fe873f1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531409"
---
# <span data-ttu-id="7c574-101">Add-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7c574-101">Add-AzureRmVmssVMDataDisk</span></span>

## <span data-ttu-id="7c574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c574-102">SYNOPSIS</span></span>
<span data-ttu-id="7c574-103">Vmss VM에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-103">Adds a data disk to a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c574-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c574-104">SYNTAX</span></span>

```
Add-AzureRmVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c574-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c574-105">DESCRIPTION</span></span>
<span data-ttu-id="7c574-106">**Add-AzureRmVmssVMDataDisk** Cmdlet은 VMSS VM에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-106">The **Add-AzureRmVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="7c574-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c574-107">EXAMPLES</span></span>

### <span data-ttu-id="7c574-108">예제 1: Vmss VM에 관리 되는 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="7c574-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="7c574-109">첫 번째 명령은 관리 되는 기존 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="7c574-110">다음 명령은 리소스 그룹 이름, vmss 이름 및 인스턴스 ID로 주어진 기존 Vmss VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="7c574-111">다음 명령은 $VmssVM에 로컬로 저장 된 Vmss VM에 관리 되는 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="7c574-112">마지막 명령은 추가 된 데이터 디스크가 있는 Vmss VM을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="7c574-113">변수</span><span class="sxs-lookup"><span data-stu-id="7c574-113">PARAMETERS</span></span>

### <span data-ttu-id="7c574-114">-캐싱</span><span class="sxs-lookup"><span data-stu-id="7c574-114">-Caching</span></span>
<span data-ttu-id="7c574-115">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="7c574-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c574-117">읽기</span><span class="sxs-lookup"><span data-stu-id="7c574-117">ReadOnly</span></span>
- <span data-ttu-id="7c574-118">쓰기</span><span class="sxs-lookup"><span data-stu-id="7c574-118">ReadWrite</span></span>
- <span data-ttu-id="7c574-119">없음 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="7c574-120">이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="7c574-121">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="7c574-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="7c574-122">-CreateOption</span></span>
<span data-ttu-id="7c574-123">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="7c574-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c574-125">붙일.</span><span class="sxs-lookup"><span data-stu-id="7c574-125">Attach.</span></span>
<span data-ttu-id="7c574-126">특수 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="7c574-127">이 옵션을 지정 하는 경우 *Sourceimageuri* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="7c574-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="7c574-128">*VhdUri* 는 가상 컴퓨터에 데이터 디스크로 연결할 VHD (가상 하드 디스크)의 위치를 Azure platform에 알리기 위해 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="7c574-129">비울.</span><span class="sxs-lookup"><span data-stu-id="7c574-129">Empty.</span></span>
<span data-ttu-id="7c574-130">빈 데이터 디스크를 만들려면이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="7c574-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="7c574-131">FromImage.</span></span>
<span data-ttu-id="7c574-132">일반화 된 이미지 또는 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="7c574-133">이 옵션을 지정 하는 경우 데이터 디스크로 연결할 VHD의 위치를 Azure platform에 알려 주는 데에도 *Sourceimageuri* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="7c574-134">*VhdUri* 매개 변수는 가상 머신에서 사용할 때 데이터 디스크 VHD가 저장 될 위치를 식별 하는 위치로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="7c574-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c574-135">-DefaultProfile</span></span>
<span data-ttu-id="7c574-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c574-137">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="7c574-137">-DiskSizeInGB</span></span>
<span data-ttu-id="7c574-138">가상 컴퓨터에 연결할 빈 디스크의 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-138">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="7c574-139">-Lun</span><span class="sxs-lookup"><span data-stu-id="7c574-139">-Lun</span></span>
<span data-ttu-id="7c574-140">데이터 디스크에 대 한 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-140">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="7c574-141">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="7c574-141">-ManagedDiskId</span></span>
<span data-ttu-id="7c574-142">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-142">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="7c574-143">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7c574-143">-StorageAccountType</span></span>
<span data-ttu-id="7c574-144">관리 되는 디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-144">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="7c574-145">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="7c574-145">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="7c574-146">데이터 디스크를 추가할 로컬 가상 컴퓨터 크기 집합 VM 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-146">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="7c574-147">**AzureRmVmssVM** cmdlet을 사용 하 여 가상 컴퓨터 확장 집합 VM 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-147">You can use the **Get-AzureRmVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c574-148">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7c574-148">-WriteAccelerator</span></span>
<span data-ttu-id="7c574-149">관리 되는 데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-149">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="7c574-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c574-150">CommonParameters</span></span>
<span data-ttu-id="7c574-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c574-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c574-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c574-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c574-153">입력</span><span class="sxs-lookup"><span data-stu-id="7c574-153">INPUTS</span></span>

### <span data-ttu-id="7c574-154">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="7c574-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="7c574-155">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="7c574-155">System.Int32</span></span>

### <span data-ttu-id="7c574-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c574-156">System.String</span></span>

### <span data-ttu-id="7c574-157">Microsoft. 관리. m m/. m m 형식</span><span class="sxs-lookup"><span data-stu-id="7c574-157">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="7c574-158">출력</span><span class="sxs-lookup"><span data-stu-id="7c574-158">OUTPUTS</span></span>

### <span data-ttu-id="7c574-159">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="7c574-159">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="7c574-160">상속자</span><span class="sxs-lookup"><span data-stu-id="7c574-160">NOTES</span></span>

## <span data-ttu-id="7c574-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c574-161">RELATED LINKS</span></span>
