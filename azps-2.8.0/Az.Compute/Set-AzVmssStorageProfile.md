---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 883c976df7223a03421550f2a27c2baf51be4dcb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697187"
---
# <span data-ttu-id="7c9a1-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7c9a1-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="7c9a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="7c9a1-103">VMSS의 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="7c9a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c9a1-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c9a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c9a1-105">DESCRIPTION</span></span>
<span data-ttu-id="7c9a1-106">**AzVmssStorageProfile** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 대 한 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="7c9a1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c9a1-107">EXAMPLES</span></span>

### <span data-ttu-id="7c9a1-108">예제 1: VMSS의 저장소 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="7c9a1-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="7c9a1-109">이 명령은 ContosoVMSS 이라는 VMSS에 대 한 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="7c9a1-110">변수</span><span class="sxs-lookup"><span data-stu-id="7c9a1-110">PARAMETERS</span></span>

### <span data-ttu-id="7c9a1-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="7c9a1-111">-DataDisk</span></span>
<span data-ttu-id="7c9a1-112">데이터 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="7c9a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c9a1-113">-DefaultProfile</span></span>
<span data-ttu-id="7c9a1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c9a1-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="7c9a1-115">-DiffDiskSetting</span></span>
<span data-ttu-id="7c9a1-116">운영 체제 디스크에 대 한 차이점 보관용 디스크 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="7c9a1-117">-이미지</span><span class="sxs-lookup"><span data-stu-id="7c9a1-117">-Image</span></span>
<span data-ttu-id="7c9a1-118">사용자 이미지에 대 한 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-118">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="7c9a1-119">VMSS는 사용자 이미지의 동일한 컨테이너에서 운영 체제 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-119">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="7c9a1-120">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="7c9a1-120">-ImageReferenceId</span></span>
<span data-ttu-id="7c9a1-121">이미지 참조 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-121">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="7c9a1-122">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="7c9a1-122">-ImageReferenceOffer</span></span>
<span data-ttu-id="7c9a1-123">VMImage (가상 컴퓨터 이미지) 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-123">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="7c9a1-124">이미지 제안을 얻으려면 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="7c9a1-125">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="7c9a1-125">-ImageReferencePublisher</span></span>
<span data-ttu-id="7c9a1-126">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="7c9a1-127">게시자를 얻으려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="7c9a1-128">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="7c9a1-128">-ImageReferenceSku</span></span>
<span data-ttu-id="7c9a1-129">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-129">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="7c9a1-130">Sku를 가져오려면 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="7c9a1-131">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="7c9a1-131">-ImageReferenceVersion</span></span>
<span data-ttu-id="7c9a1-132">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-132">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="7c9a1-133">최신 버전을 사용 하려면 특정 버전 대신 최신 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="7c9a1-134">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="7c9a1-134">-ManagedDisk</span></span>
<span data-ttu-id="7c9a1-135">관리 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-135">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="7c9a1-136">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="7c9a1-136">-OsDiskCaching</span></span>
<span data-ttu-id="7c9a1-137">운영 체제 디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-137">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="7c9a1-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c9a1-139">읽기</span><span class="sxs-lookup"><span data-stu-id="7c9a1-139">ReadOnly</span></span>
- <span data-ttu-id="7c9a1-140">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-140">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="7c9a1-141">캐싱 값을 변경 하면 cmdlet이 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-141">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="7c9a1-142">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-142">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="7c9a1-143">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="7c9a1-143">-OsDiskCreateOption</span></span>
<span data-ttu-id="7c9a1-144">이 cmdlet이 VMSS 가상 컴퓨터를 만드는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-144">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="7c9a1-145">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c9a1-146">연결:이 값은 특수 디스크를 사용 하 여 VMSS 가상 컴퓨터를 만드는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-146">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="7c9a1-147">FromImage:이 값은 이미지를 사용 하 여 VMSS 가상 컴퓨터를 만드는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-147">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="7c9a1-148">플랫폼 이미지를 사용 하는 경우에는 *imageReference* 매개 변수도 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-148">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="7c9a1-149">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="7c9a1-149">-OsDiskName</span></span>
<span data-ttu-id="7c9a1-150">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-150">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="7c9a1-151">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="7c9a1-151">-OsDiskOsType</span></span>
<span data-ttu-id="7c9a1-152">디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-152">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="7c9a1-153">이는 플랫폼 이미지가 아닌 사용자 이미지 시나리오에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-153">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="7c9a1-154">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7c9a1-154">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="7c9a1-155">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-155">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="7c9a1-156">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="7c9a1-156">-VhdContainer</span></span>
<span data-ttu-id="7c9a1-157">VMSS의 운영 체제 디스크를 저장 하는 데 사용 되는 컨테이너 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-157">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="7c9a1-158">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7c9a1-158">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7c9a1-159">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-159">Specifies the VMSS object.</span></span>
<span data-ttu-id="7c9a1-160">개체를 가져오려면 New-AzVmssConfig 개체를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-160">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="7c9a1-161">-확인</span><span class="sxs-lookup"><span data-stu-id="7c9a1-161">-Confirm</span></span>
<span data-ttu-id="7c9a1-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c9a1-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c9a1-163">-WhatIf</span></span>
<span data-ttu-id="7c9a1-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c9a1-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c9a1-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c9a1-166">CommonParameters</span></span>
<span data-ttu-id="7c9a1-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c9a1-168">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c9a1-169">입력</span><span class="sxs-lookup"><span data-stu-id="7c9a1-169">INPUTS</span></span>

### <span data-ttu-id="7c9a1-170">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-170">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="7c9a1-171">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c9a1-171">System.String</span></span>

### <span data-ttu-id="7c9a1-172">시스템 Null 허용 ' 1 [[23.0.0.0], [[Microsoft Azure. 31bf3856ad364e35.-Management. 관리. t e;. i =, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="7c9a1-172">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7c9a1-173">시스템 Null 허용 ' 1 [[OperatingSystemTypes, Microsoft azure. 23.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7c9a1-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7c9a1-174">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="7c9a1-174">System.String[]</span></span>

### <span data-ttu-id="7c9a1-175">Microsoft VirtualMachineScaleSetDataDisk []을 (를)</span><span class="sxs-lookup"><span data-stu-id="7c9a1-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="7c9a1-176">출력</span><span class="sxs-lookup"><span data-stu-id="7c9a1-176">OUTPUTS</span></span>

### <span data-ttu-id="7c9a1-177">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-177">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7c9a1-178">상속자</span><span class="sxs-lookup"><span data-stu-id="7c9a1-178">NOTES</span></span>

## <span data-ttu-id="7c9a1-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c9a1-179">RELATED LINKS</span></span>

[<span data-ttu-id="7c9a1-180">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7c9a1-180">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="7c9a1-181">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7c9a1-181">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="7c9a1-182">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7c9a1-182">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="7c9a1-183">새로운 AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7c9a1-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


