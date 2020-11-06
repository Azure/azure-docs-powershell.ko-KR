---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 60d525cc50b62350853755ae46698cbecb358654
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525547"
---
# <span data-ttu-id="f2e9b-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="f2e9b-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="f2e9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e9b-103">VMSS의 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2e9b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2e9b-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2e9b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2e9b-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e9b-106">**AzureRmVmssStorageProfile** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 대 한 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f2e9b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f2e9b-107">EXAMPLES</span></span>

### <span data-ttu-id="f2e9b-108">예제 1: VMSS의 저장소 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="f2e9b-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="f2e9b-109">이 명령은 ContosoVMSS 이라는 VMSS에 대 한 저장소 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="f2e9b-110">변수</span><span class="sxs-lookup"><span data-stu-id="f2e9b-110">PARAMETERS</span></span>

### <span data-ttu-id="f2e9b-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="f2e9b-111">-DataDisk</span></span>
<span data-ttu-id="f2e9b-112">데이터 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="f2e9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e9b-113">-DefaultProfile</span></span>
<span data-ttu-id="f2e9b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2e9b-115">-이미지</span><span class="sxs-lookup"><span data-stu-id="f2e9b-115">-Image</span></span>
<span data-ttu-id="f2e9b-116">사용자 이미지에 대 한 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="f2e9b-117">VMSS는 사용자 이미지의 동일한 컨테이너에서 운영 체제 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="f2e9b-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="f2e9b-118">-ImageReferenceId</span></span>
<span data-ttu-id="f2e9b-119">이미지 참조 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-119">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="f2e9b-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="f2e9b-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="f2e9b-121">VMImage (가상 컴퓨터 이미지) 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="f2e9b-122">이미지 제안을 얻으려면 Get-AzureRmVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="f2e9b-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="f2e9b-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="f2e9b-124">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="f2e9b-125">게시자를 얻으려면 Get-AzureRmVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="f2e9b-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="f2e9b-126">-ImageReferenceSku</span></span>
<span data-ttu-id="f2e9b-127">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="f2e9b-128">Sku를 가져오려면 Get-AzureRmVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="f2e9b-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="f2e9b-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="f2e9b-130">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="f2e9b-131">최신 버전을 사용 하려면 특정 버전 대신 최신 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="f2e9b-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f2e9b-132">-ManagedDisk</span></span>
<span data-ttu-id="f2e9b-133">관리 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-133">Specifies the managed disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e9b-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="f2e9b-134">-OsDiskCaching</span></span>
<span data-ttu-id="f2e9b-135">운영 체제 디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="f2e9b-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2e9b-137">읽기</span><span class="sxs-lookup"><span data-stu-id="f2e9b-137">ReadOnly</span></span>
- <span data-ttu-id="f2e9b-138">쓰기</span><span class="sxs-lookup"><span data-stu-id="f2e9b-138">ReadWrite</span></span>

<span data-ttu-id="f2e9b-139">기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="f2e9b-140">캐싱 값을 변경 하면 cmdlet이 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="f2e9b-141">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-141">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="f2e9b-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="f2e9b-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="f2e9b-143">이 cmdlet이 VMSS 가상 컴퓨터를 만드는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="f2e9b-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2e9b-145">연결:이 값은 특수 디스크를 사용 하 여 VMSS 가상 컴퓨터를 만드는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="f2e9b-146">FromImage:이 값은 이미지를 사용 하 여 VMSS 가상 컴퓨터를 만드는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="f2e9b-147">플랫폼 이미지를 사용 하는 경우에는 *imageReference* 매개 변수도 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e9b-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="f2e9b-148">-OsDiskName</span></span>
<span data-ttu-id="f2e9b-149">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="f2e9b-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="f2e9b-150">-OsDiskOsType</span></span>
<span data-ttu-id="f2e9b-151">디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="f2e9b-152">이는 플랫폼 이미지가 아닌 사용자 이미지 시나리오에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-152">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="f2e9b-153">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="f2e9b-153">-VhdContainer</span></span>
<span data-ttu-id="f2e9b-154">VMSS의 운영 체제 디스크를 저장 하는 데 사용 되는 컨테이너 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-154">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="f2e9b-155">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f2e9b-155">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f2e9b-156">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-156">Specifies the VMSS object.</span></span>
<span data-ttu-id="f2e9b-157">개체를 가져오려면 New-AzureRmVmssConfig 개체를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-157">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

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

### <span data-ttu-id="f2e9b-158">-확인</span><span class="sxs-lookup"><span data-stu-id="f2e9b-158">-Confirm</span></span>
<span data-ttu-id="f2e9b-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2e9b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2e9b-160">-WhatIf</span></span>
<span data-ttu-id="f2e9b-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2e9b-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2e9b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e9b-163">CommonParameters</span></span>
<span data-ttu-id="f2e9b-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e9b-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2e9b-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e9b-166">입력</span><span class="sxs-lookup"><span data-stu-id="f2e9b-166">INPUTS</span></span>

###  
<span data-ttu-id="f2e9b-167">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e9b-167">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f2e9b-168">출력</span><span class="sxs-lookup"><span data-stu-id="f2e9b-168">OUTPUTS</span></span>

## <span data-ttu-id="f2e9b-169">상속자</span><span class="sxs-lookup"><span data-stu-id="f2e9b-169">NOTES</span></span>

## <span data-ttu-id="f2e9b-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2e9b-170">RELATED LINKS</span></span>

[<span data-ttu-id="f2e9b-171">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f2e9b-171">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="f2e9b-172">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f2e9b-172">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f2e9b-173">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f2e9b-173">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="f2e9b-174">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f2e9b-174">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


