---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204685"
---
# <span data-ttu-id="0fee9-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="0fee9-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="0fee9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fee9-102">SYNOPSIS</span></span>
<span data-ttu-id="0fee9-103">VMSS에 대한 저장소 프로필 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="0fee9-104">구문</span><span class="sxs-lookup"><span data-stu-id="0fee9-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fee9-105">설명</span><span class="sxs-lookup"><span data-stu-id="0fee9-105">DESCRIPTION</span></span>
<span data-ttu-id="0fee9-106">**Set-AzVmssStorageProfile** cmdlet은 VMSS(Virtual Machine Scale Set)에 대한 저장소 프로필 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="0fee9-107">예제</span><span class="sxs-lookup"><span data-stu-id="0fee9-107">EXAMPLES</span></span>

### <span data-ttu-id="0fee9-108">예제 1: VMSS에 대한 저장소 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="0fee9-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="0fee9-109">이 명령은 ContosoVMSS라는 VMSS에 대한 저장소 프로필 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="0fee9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fee9-110">PARAMETERS</span></span>

### <span data-ttu-id="0fee9-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="0fee9-111">-DataDisk</span></span>
<span data-ttu-id="0fee9-112">데이터 디스크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-112">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fee9-113">-DefaultProfile</span></span>
<span data-ttu-id="0fee9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fee9-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="0fee9-115">-DiffDiskSetting</span></span>
<span data-ttu-id="0fee9-116">운영 체제 디스크에 대한 다른 디스크 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="0fee9-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="0fee9-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="0fee9-118">고객 관리 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="0fee9-119">관리 디스크에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="0fee9-120">-Image</span><span class="sxs-lookup"><span data-stu-id="0fee9-120">-Image</span></span>
<span data-ttu-id="0fee9-121">사용자 이미지에 대한 Blob URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="0fee9-122">VMSS는 사용자 이미지의 동일한 컨테이너에 운영 체제 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="0fee9-123">-ImageReferenceId</span></span>
<span data-ttu-id="0fee9-124">이미지 참조 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="0fee9-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="0fee9-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="0fee9-126">VMImage(가상 머신 이미지) 제안의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="0fee9-127">이미지 제안을 얻습니다. Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="0fee9-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="0fee9-129">VMImage의 게시자 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="0fee9-130">게시자를 얻습니다. Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="0fee9-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="0fee9-131">-ImageReferenceSku</span></span>
<span data-ttu-id="0fee9-132">VMImage SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="0fee9-133">SKUS를 얻습니다. Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="0fee9-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="0fee9-135">VMImage의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="0fee9-136">최신 버전을 사용하세요. 특정 버전 대신 최신 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="0fee9-137">-ManagedDisk</span></span>
<span data-ttu-id="0fee9-138">관리 디스크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="0fee9-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="0fee9-139">-OsDiskCaching</span></span>
<span data-ttu-id="0fee9-140">운영 체제 디스크의 캐싱 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="0fee9-141">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="0fee9-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0fee9-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0fee9-142">ReadOnly</span></span>
- <span data-ttu-id="0fee9-143">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="0fee9-144">캐싱 값을 변경하면 cmdlet이 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="0fee9-145">이 설정은 디스크의 일관성 및 성능에 영향을 미치고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="0fee9-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="0fee9-147">이 cmdlet이 VMSS 가상 머신을 만드는 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="0fee9-148">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="0fee9-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0fee9-149">연결: 이 값은 특수한 디스크를 사용하여 VMSS 가상 머신을 만들 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="0fee9-150">FromImage: 이 값은 이미지를 사용하여 VMSS 가상 머신을 만들 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="0fee9-151">플랫폼 이미지를 사용하는 경우 *imageReference 매개 변수도 사용합니다.*</span><span class="sxs-lookup"><span data-stu-id="0fee9-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="0fee9-152">-OsDiskName</span></span>
<span data-ttu-id="0fee9-153">운영 체제 디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-153">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="0fee9-154">-OsDiskOsType</span></span>
<span data-ttu-id="0fee9-155">디스크의 운영 체제 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="0fee9-156">이는 플랫폼 이미지가 아닌 사용자 이미지 시나리오에만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-156">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="0fee9-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="0fee9-158">OS 디스크에서 WriteAccelerator를 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="0fee9-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="0fee9-159">-VhdContainer</span></span>
<span data-ttu-id="0fee9-160">VMSS에 대한 운영 체제 디스크를 저장하는 데 사용되는 컨테이너 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0fee9-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0fee9-162">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="0fee9-163">개체를 얻습니다. New-AzVmssConfig 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fee9-164">-Confirm</span></span>
<span data-ttu-id="0fee9-165">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fee9-166">-WhatIf</span></span>
<span data-ttu-id="0fee9-167">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0fee9-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fee9-168">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fee9-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fee9-169">CommonParameters</span></span>
<span data-ttu-id="0fee9-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0fee9-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fee9-171">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0fee9-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fee9-172">입력</span><span class="sxs-lookup"><span data-stu-id="0fee9-172">INPUTS</span></span>

### <span data-ttu-id="0fee9-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0fee9-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="0fee9-174">System.String</span><span class="sxs-lookup"><span data-stu-id="0fee9-174">System.String</span></span>

### <span data-ttu-id="0fee9-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0fee9-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0fee9-176">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0fee9-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0fee9-177">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0fee9-177">System.String[]</span></span>

### <span data-ttu-id="0fee9-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="0fee9-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="0fee9-179">출력</span><span class="sxs-lookup"><span data-stu-id="0fee9-179">OUTPUTS</span></span>

### <span data-ttu-id="0fee9-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0fee9-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="0fee9-181">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0fee9-181">NOTES</span></span>

## <span data-ttu-id="0fee9-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fee9-182">RELATED LINKS</span></span>

[<span data-ttu-id="0fee9-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="0fee9-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="0fee9-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0fee9-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="0fee9-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0fee9-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="0fee9-186">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0fee9-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


