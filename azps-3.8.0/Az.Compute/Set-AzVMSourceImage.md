---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a1ed1fa266638891507b6853199bff23d23aa1b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044622"
---
# <span data-ttu-id="5718d-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="5718d-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="5718d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5718d-102">SYNOPSIS</span></span>
<span data-ttu-id="5718d-103">가상 컴퓨터의 이미지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="5718d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5718d-104">SYNTAX</span></span>

### <span data-ttu-id="5718d-105">ImageReferenceSkuParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5718d-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5718d-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5718d-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5718d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5718d-107">DESCRIPTION</span></span>
<span data-ttu-id="5718d-108">**AzVMSourceImage** cmdlet은 가상 컴퓨터에 사용할 플랫폼 이미지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="5718d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5718d-109">EXAMPLES</span></span>

### <span data-ttu-id="5718d-110">예제 1: 이미지의 값 설정</span><span class="sxs-lookup"><span data-stu-id="5718d-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="5718d-111">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailabilitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="5718d-112">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5718d-113">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="5718d-114">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="5718d-115">마지막 명령은 publisher 이름, 제안, SKU 및 버전에 대 한 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="5718d-116">**AzVMImagePublisher** , **get-AzVMImageOffer** , **get-AzVMImageSku** 및 **get-AzVMImage** cmdlet은 이러한 설정을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-116">The **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** , and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="5718d-117">변수</span><span class="sxs-lookup"><span data-stu-id="5718d-117">PARAMETERS</span></span>

### <span data-ttu-id="5718d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5718d-118">-DefaultProfile</span></span>
<span data-ttu-id="5718d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5718d-120">-Id</span><span class="sxs-lookup"><span data-stu-id="5718d-120">-Id</span></span>
<span data-ttu-id="5718d-121">ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-121">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5718d-122">-제공</span><span class="sxs-lookup"><span data-stu-id="5718d-122">-Offer</span></span>
<span data-ttu-id="5718d-123">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="5718d-124">이미지 제안을 얻으려면 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5718d-125">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="5718d-125">-PublisherName</span></span>
<span data-ttu-id="5718d-126">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="5718d-127">게시자를 얻으려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5718d-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="5718d-128">-Skus</span></span>
<span data-ttu-id="5718d-129">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="5718d-130">Sku를 가져오려면 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5718d-131">-버전</span><span class="sxs-lookup"><span data-stu-id="5718d-131">-Version</span></span>
<span data-ttu-id="5718d-132">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="5718d-133">최신 버전을 사용 하려면 특정 버전 대신 최신 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5718d-134">-VM</span><span class="sxs-lookup"><span data-stu-id="5718d-134">-VM</span></span>
<span data-ttu-id="5718d-135">구성할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-135">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5718d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5718d-136">CommonParameters</span></span>
<span data-ttu-id="5718d-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5718d-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5718d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5718d-139">입력</span><span class="sxs-lookup"><span data-stu-id="5718d-139">INPUTS</span></span>

### <span data-ttu-id="5718d-140">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="5718d-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5718d-141">System.String</span></span>

## <span data-ttu-id="5718d-142">출력</span><span class="sxs-lookup"><span data-stu-id="5718d-142">OUTPUTS</span></span>

### <span data-ttu-id="5718d-143">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="5718d-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5718d-144">상속자</span><span class="sxs-lookup"><span data-stu-id="5718d-144">NOTES</span></span>

## <span data-ttu-id="5718d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5718d-145">RELATED LINKS</span></span>

[<span data-ttu-id="5718d-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5718d-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="5718d-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5718d-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="5718d-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="5718d-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="5718d-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="5718d-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="5718d-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="5718d-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="5718d-151">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5718d-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


