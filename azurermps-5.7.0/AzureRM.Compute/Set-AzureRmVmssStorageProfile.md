---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 26f61261bd8fd1c2d5fc2bbdacec71f73db91fb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531738"
---
# <span data-ttu-id="b8134-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b8134-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="b8134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8134-102">SYNOPSIS</span></span>
<span data-ttu-id="b8134-103">VMSS의 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8134-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8134-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [-OsDiskName <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8134-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8134-105">DESCRIPTION</span></span>
<span data-ttu-id="b8134-106">**AzureRmVmssStorageProfile** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 대 한 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b8134-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b8134-107">EXAMPLES</span></span>

### <span data-ttu-id="b8134-108">예제 1: VMSS의 저장소 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="b8134-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="b8134-109">이 명령은 ContosoVMSS 이라는 VMSS에 대 한 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="b8134-110">변수</span><span class="sxs-lookup"><span data-stu-id="b8134-110">PARAMETERS</span></span>

### <span data-ttu-id="b8134-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="b8134-111">-DataDisk</span></span>
<span data-ttu-id="b8134-112">데이터 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="b8134-113">-이미지</span><span class="sxs-lookup"><span data-stu-id="b8134-113">-Image</span></span>
<span data-ttu-id="b8134-114">사용자 이미지에 대 한 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-114">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="b8134-115">VMSS는 사용자 이미지의 동일한 컨테이너에서 운영 체제 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-115">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="b8134-116">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="b8134-116">-ImageReferenceId</span></span>
<span data-ttu-id="b8134-117">이미지 참조 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-117">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="b8134-118">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="b8134-118">-ImageReferenceOffer</span></span>
<span data-ttu-id="b8134-119">VMImage (가상 컴퓨터 이미지) 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-119">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="b8134-120">이미지 제안을 얻으려면 Get-AzureRmVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-120">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="b8134-121">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="b8134-121">-ImageReferencePublisher</span></span>
<span data-ttu-id="b8134-122">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-122">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="b8134-123">게시자를 얻으려면 Get-AzureRmVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-123">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="b8134-124">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="b8134-124">-ImageReferenceSku</span></span>
<span data-ttu-id="b8134-125">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-125">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="b8134-126">Sku를 가져오려면 Get-AzureRmVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-126">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="b8134-127">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="b8134-127">-ImageReferenceVersion</span></span>
<span data-ttu-id="b8134-128">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-128">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="b8134-129">최신 버전을 사용 하려면 특정 버전 대신 최신 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-129">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="b8134-130">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b8134-130">-ManagedDisk</span></span>
<span data-ttu-id="b8134-131">관리 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-131">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="b8134-132">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="b8134-132">-OsDiskCaching</span></span>
<span data-ttu-id="b8134-133">운영 체제 디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-133">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="b8134-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8134-135">읽기</span><span class="sxs-lookup"><span data-stu-id="b8134-135">ReadOnly</span></span>
- <span data-ttu-id="b8134-136">쓰기</span><span class="sxs-lookup"><span data-stu-id="b8134-136">ReadWrite</span></span>

<span data-ttu-id="b8134-137">기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-137">The default value is ReadWrite.</span></span>
<span data-ttu-id="b8134-138">캐싱 값을 변경 하면 cmdlet이 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-138">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="b8134-139">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-139">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="b8134-140">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="b8134-140">-OsDiskCreateOption</span></span>
<span data-ttu-id="b8134-141">이 cmdlet이 VMSS 가상 컴퓨터를 만드는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-141">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="b8134-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8134-143">연결:이 값은 특수 디스크를 사용 하 여 VMSS 가상 컴퓨터를 만드는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-143">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="b8134-144">FromImage:이 값은 이미지를 사용 하 여 VMSS 가상 컴퓨터를 만드는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-144">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="b8134-145">플랫폼 이미지를 사용 하는 경우에는 *imageReference* 매개 변수도 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-145">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="b8134-146">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="b8134-146">-OsDiskName</span></span>
<span data-ttu-id="b8134-147">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-147">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8134-148">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="b8134-148">-OsDiskOsType</span></span>
<span data-ttu-id="b8134-149">디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-149">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="b8134-150">이는 플랫폼 이미지가 아닌 사용자 이미지 시나리오에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-150">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="b8134-151">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="b8134-151">-VhdContainer</span></span>
<span data-ttu-id="b8134-152">VMSS의 운영 체제 디스크를 저장 하는 데 사용 되는 컨테이너 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-152">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="b8134-153">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b8134-153">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b8134-154">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-154">Specifies the VMSS object.</span></span>
<span data-ttu-id="b8134-155">개체를 가져오려면 New-AzureRmVmssConfig 개체를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-155">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8134-156">-확인</span><span class="sxs-lookup"><span data-stu-id="b8134-156">-Confirm</span></span>
<span data-ttu-id="b8134-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8134-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8134-158">-WhatIf</span></span>
<span data-ttu-id="b8134-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8134-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8134-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8134-161">CommonParameters</span></span>
<span data-ttu-id="b8134-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8134-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8134-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8134-164">입력</span><span class="sxs-lookup"><span data-stu-id="b8134-164">INPUTS</span></span>

###  
<span data-ttu-id="b8134-165">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8134-165">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b8134-166">출력</span><span class="sxs-lookup"><span data-stu-id="b8134-166">OUTPUTS</span></span>

## <span data-ttu-id="b8134-167">상속자</span><span class="sxs-lookup"><span data-stu-id="b8134-167">NOTES</span></span>

## <span data-ttu-id="b8134-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8134-168">RELATED LINKS</span></span>

[<span data-ttu-id="b8134-169">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="b8134-169">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="b8134-170">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b8134-170">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="b8134-171">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="b8134-171">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="b8134-172">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b8134-172">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


