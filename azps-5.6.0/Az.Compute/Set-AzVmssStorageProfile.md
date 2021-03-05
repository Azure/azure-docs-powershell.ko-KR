---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: ec233765f401348895275291ddad0571d1ddfc85
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977483"
---
# <span data-ttu-id="71eb7-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="71eb7-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="71eb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="71eb7-103">VMSS에 대한 저장소 프로필 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="71eb7-104">구문</span><span class="sxs-lookup"><span data-stu-id="71eb7-104">SYNTAX</span></span>

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

## <span data-ttu-id="71eb7-105">설명</span><span class="sxs-lookup"><span data-stu-id="71eb7-105">DESCRIPTION</span></span>
<span data-ttu-id="71eb7-106">**Set-AzVmssStorageProfile** cmdlet은 VMSS(Virtual Machine Scale Set)에 대한 저장소 프로필 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="71eb7-107">예제</span><span class="sxs-lookup"><span data-stu-id="71eb7-107">EXAMPLES</span></span>

### <span data-ttu-id="71eb7-108">예제 1: VMSS에 대한 저장소 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="71eb7-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="71eb7-109">이 명령은 ContosoVMSS라는 VMSS에 대한 저장소 프로필 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="71eb7-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="71eb7-110">PARAMETERS</span></span>

### <span data-ttu-id="71eb7-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="71eb7-111">-DataDisk</span></span>
<span data-ttu-id="71eb7-112">데이터 디스크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="71eb7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71eb7-113">-DefaultProfile</span></span>
<span data-ttu-id="71eb7-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71eb7-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="71eb7-115">-DiffDiskSetting</span></span>
<span data-ttu-id="71eb7-116">운영 체제 디스크에 대한 다른 디스크 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="71eb7-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="71eb7-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="71eb7-118">고객 관리 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="71eb7-119">이는 관리 디스크에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="71eb7-120">-Image</span><span class="sxs-lookup"><span data-stu-id="71eb7-120">-Image</span></span>
<span data-ttu-id="71eb7-121">사용자 이미지에 대한 Blob URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="71eb7-122">VMSS는 사용자 이미지의 동일한 컨테이너에 운영 체제 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="71eb7-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="71eb7-123">-ImageReferenceId</span></span>
<span data-ttu-id="71eb7-124">이미지 참조 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="71eb7-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="71eb7-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="71eb7-126">VMImage(가상 머신 이미지) 제품 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="71eb7-127">이미지 제안을 얻은 경우 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="71eb7-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="71eb7-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="71eb7-129">VMImage의 게시자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="71eb7-130">퍼블리셔를 얻지 위해 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="71eb7-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="71eb7-131">-ImageReferenceSku</span></span>
<span data-ttu-id="71eb7-132">VMImage SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="71eb7-133">SKUS를 얻지 위해 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="71eb7-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="71eb7-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="71eb7-135">VMImage 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="71eb7-136">최신 버전을 사용하기 위해 특정 버전 대신 최신 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="71eb7-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="71eb7-137">-ManagedDisk</span></span>
<span data-ttu-id="71eb7-138">관리 디스크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="71eb7-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="71eb7-139">-OsDiskCaching</span></span>
<span data-ttu-id="71eb7-140">운영 체제 디스크의 캐싱 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="71eb7-141">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71eb7-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="71eb7-142">ReadOnly</span></span>
- <span data-ttu-id="71eb7-143">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="71eb7-144">캐싱 값을 변경하면 cmdlet이 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="71eb7-145">이 설정은 디스크의 일관성 및 성능에 영향을 미치게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="71eb7-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="71eb7-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="71eb7-147">이 cmdlet에서 VMSS 가상 머신을 만드는 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="71eb7-148">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71eb7-149">연결 : 이 값은 특수 디스크를 사용하여 VMSS 가상 머신을 만들 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="71eb7-150">FromImage : 이 값은 이미지를 사용하여 VMSS 가상 머신을 만들 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="71eb7-151">플랫폼 이미지를 사용하는 경우 *imageReference 매개 변수도 사용합니다.*</span><span class="sxs-lookup"><span data-stu-id="71eb7-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="71eb7-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="71eb7-152">-OsDiskName</span></span>
<span data-ttu-id="71eb7-153">운영 체제 디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-153">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="71eb7-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="71eb7-154">-OsDiskOsType</span></span>
<span data-ttu-id="71eb7-155">디스크의 운영 체제 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="71eb7-156">이 시나리오는 플랫폼 이미지가 아니라 사용자 이미지 시나리오에만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-156">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="71eb7-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="71eb7-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="71eb7-158">OS 디스크에서 WriteAccelerator를 사용하도록 설정하거나 사용하지 않도록 설정해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="71eb7-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="71eb7-159">-VhdContainer</span></span>
<span data-ttu-id="71eb7-160">VMSS에 대한 운영 체제 디스크를 저장하는 데 사용되는 컨테이너 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="71eb7-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="71eb7-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="71eb7-162">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="71eb7-163">개체를 구하기 위해 개체 New-AzVmssConfig 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="71eb7-164">-확인</span><span class="sxs-lookup"><span data-stu-id="71eb7-164">-Confirm</span></span>
<span data-ttu-id="71eb7-165">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71eb7-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71eb7-166">-WhatIf</span></span>
<span data-ttu-id="71eb7-167">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71eb7-168">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71eb7-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71eb7-169">CommonParameters</span></span>
<span data-ttu-id="71eb7-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71eb7-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71eb7-171">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71eb7-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71eb7-172">입력</span><span class="sxs-lookup"><span data-stu-id="71eb7-172">INPUTS</span></span>

### <span data-ttu-id="71eb7-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="71eb7-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="71eb7-174">System.String</span><span class="sxs-lookup"><span data-stu-id="71eb7-174">System.String</span></span>

### <span data-ttu-id="71eb7-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="71eb7-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="71eb7-176">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="71eb7-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="71eb7-177">System.String[]</span><span class="sxs-lookup"><span data-stu-id="71eb7-177">System.String[]</span></span>

### <span data-ttu-id="71eb7-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="71eb7-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="71eb7-179">출력</span><span class="sxs-lookup"><span data-stu-id="71eb7-179">OUTPUTS</span></span>

### <span data-ttu-id="71eb7-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="71eb7-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="71eb7-181">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71eb7-181">NOTES</span></span>

## <span data-ttu-id="71eb7-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71eb7-182">RELATED LINKS</span></span>

[<span data-ttu-id="71eb7-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="71eb7-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="71eb7-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="71eb7-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="71eb7-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="71eb7-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="71eb7-186">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="71eb7-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


