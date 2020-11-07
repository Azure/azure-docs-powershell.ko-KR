---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: d19c039a5038c9327ea35a4f0b385e5472b748a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876848"
---
# <span data-ttu-id="a9913-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="a9913-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="a9913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9913-102">SYNOPSIS</span></span>
<span data-ttu-id="a9913-103">VMSS의 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="a9913-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9913-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-ManagedDisk <StorageAccountTypes>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9913-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a9913-105">DESCRIPTION</span></span>
<span data-ttu-id="a9913-106">**AzVmssStorageProfile** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 대 한 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a9913-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a9913-107">EXAMPLES</span></span>

### <span data-ttu-id="a9913-108">예제 1: VMSS의 저장소 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="a9913-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="a9913-109">이 명령은 ContosoVMSS 이라는 VMSS에 대 한 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="a9913-110">변수</span><span class="sxs-lookup"><span data-stu-id="a9913-110">PARAMETERS</span></span>

### <span data-ttu-id="a9913-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="a9913-111">-DataDisk</span></span>
<span data-ttu-id="a9913-112">데이터 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-112">Specifies the data disk object.</span></span>

```yaml
Type: VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9913-113">-DefaultProfile</span></span>
<span data-ttu-id="a9913-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9913-115">-이미지</span><span class="sxs-lookup"><span data-stu-id="a9913-115">-Image</span></span>
<span data-ttu-id="a9913-116">사용자 이미지에 대 한 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="a9913-117">VMSS는 사용자 이미지의 동일한 컨테이너에서 운영 체제 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="a9913-118">-ImageReferenceId</span></span>
<span data-ttu-id="a9913-119">이미지 참조 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-119">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="a9913-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="a9913-121">VMImage (가상 컴퓨터 이미지) 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="a9913-122">이미지 제안을 얻으려면 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-122">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="a9913-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="a9913-124">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="a9913-125">게시자를 얻으려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-125">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="a9913-126">-ImageReferenceSku</span></span>
<span data-ttu-id="a9913-127">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="a9913-128">Sku를 가져오려면 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-128">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="a9913-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="a9913-130">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="a9913-131">최신 버전을 사용 하려면 특정 버전 대신 최신 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a9913-132">-ManagedDisk</span></span>
<span data-ttu-id="a9913-133">관리 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-133">Specifies the managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="a9913-134">-OsDiskCaching</span></span>
<span data-ttu-id="a9913-135">운영 체제 디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="a9913-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a9913-137">읽기</span><span class="sxs-lookup"><span data-stu-id="a9913-137">ReadOnly</span></span>
- <span data-ttu-id="a9913-138">쓰기</span><span class="sxs-lookup"><span data-stu-id="a9913-138">ReadWrite</span></span>

<span data-ttu-id="a9913-139">기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="a9913-140">캐싱 값을 변경 하면 cmdlet이 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="a9913-141">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-141">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="a9913-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="a9913-143">이 cmdlet이 VMSS 가상 컴퓨터를 만드는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="a9913-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a9913-145">연결:이 값은 특수 디스크를 사용 하 여 VMSS 가상 컴퓨터를 만드는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="a9913-146">FromImage:이 값은 이미지를 사용 하 여 VMSS 가상 컴퓨터를 만드는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="a9913-147">플랫폼 이미지를 사용 하는 경우에는 *imageReference* 매개 변수도 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="a9913-148">-OsDiskName</span></span>
<span data-ttu-id="a9913-149">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-149">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="a9913-150">-OsDiskOsType</span></span>
<span data-ttu-id="a9913-151">디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="a9913-152">이는 플랫폼 이미지가 아닌 사용자 이미지 시나리오에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-152">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-153">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="a9913-153">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="a9913-154">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-154">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="a9913-155">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="a9913-155">-VhdContainer</span></span>
<span data-ttu-id="a9913-156">VMSS의 운영 체제 디스크를 저장 하는 데 사용 되는 컨테이너 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-156">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-157">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a9913-157">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a9913-158">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-158">Specifies the VMSS object.</span></span>
<span data-ttu-id="a9913-159">개체를 가져오려면 New-AzVmssConfig 개체를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-159">To obtain the object, use the New-AzVmssConfig object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-160">-확인</span><span class="sxs-lookup"><span data-stu-id="a9913-160">-Confirm</span></span>
<span data-ttu-id="a9913-161">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9913-162">-WhatIf</span></span>
<span data-ttu-id="a9913-163">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9913-164">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-164">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9913-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9913-165">CommonParameters</span></span>
<span data-ttu-id="a9913-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9913-167">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9913-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9913-168">입력</span><span class="sxs-lookup"><span data-stu-id="a9913-168">INPUTS</span></span>

###  
<span data-ttu-id="a9913-169">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9913-169">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a9913-170">출력</span><span class="sxs-lookup"><span data-stu-id="a9913-170">OUTPUTS</span></span>

### <span data-ttu-id="a9913-171">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="a9913-171">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a9913-172">상속자</span><span class="sxs-lookup"><span data-stu-id="a9913-172">NOTES</span></span>

## <span data-ttu-id="a9913-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9913-173">RELATED LINKS</span></span>

[<span data-ttu-id="a9913-174">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a9913-174">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="a9913-175">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a9913-175">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a9913-176">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a9913-176">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="a9913-177">새로운 AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a9913-177">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


