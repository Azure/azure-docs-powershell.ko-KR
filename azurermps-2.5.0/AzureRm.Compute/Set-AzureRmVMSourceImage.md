---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsourceimage
schema: 2.0.0
ms.openlocfilehash: 5e07ba8ffceb42a94c41c0b21c62329f9dbe96a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881601"
---
# <span data-ttu-id="63788-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="63788-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="63788-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63788-102">SYNOPSIS</span></span>
<span data-ttu-id="63788-103">가상 컴퓨터의 이미지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63788-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63788-104">SYNTAX</span></span>

### <span data-ttu-id="63788-105">ImageReferenceSkuParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="63788-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63788-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63788-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63788-107">설명은</span><span class="sxs-lookup"><span data-stu-id="63788-107">DESCRIPTION</span></span>
<span data-ttu-id="63788-108">**AzureRmVMSourceImage** cmdlet은 가상 컴퓨터에 사용할 플랫폼 이미지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="63788-109">예제의</span><span class="sxs-lookup"><span data-stu-id="63788-109">EXAMPLES</span></span>

### <span data-ttu-id="63788-110">예제 1: 이미지의 값 설정</span><span class="sxs-lookup"><span data-stu-id="63788-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="63788-111">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="63788-112">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="63788-113">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="63788-114">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="63788-115">마지막 명령은 publisher 이름, 제안, SKU 및 버전에 대 한 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="63788-116">**AzureRmVMImagePublisher** , **get-AzureRmVMImageOffer** , **get-AzureRmVMImageSku** 및 **get-AzureRmVMImage** cmdlet은 이러한 설정을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63788-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="63788-117">변수</span><span class="sxs-lookup"><span data-stu-id="63788-117">PARAMETERS</span></span>

### <span data-ttu-id="63788-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63788-118">-DefaultProfile</span></span>
<span data-ttu-id="63788-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63788-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63788-120">-Id</span><span class="sxs-lookup"><span data-stu-id="63788-120">-Id</span></span>
<span data-ttu-id="63788-121">ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-121">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceIdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63788-122">-제공</span><span class="sxs-lookup"><span data-stu-id="63788-122">-Offer</span></span>
<span data-ttu-id="63788-123">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="63788-124">이미지 제안을 얻으려면 Get-AzureRmVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63788-125">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="63788-125">-PublisherName</span></span>
<span data-ttu-id="63788-126">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="63788-127">게시자를 얻으려면 Get-AzureRmVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63788-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="63788-128">-Skus</span></span>
<span data-ttu-id="63788-129">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="63788-130">Sku를 가져오려면 Get-AzureRmVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63788-131">-버전</span><span class="sxs-lookup"><span data-stu-id="63788-131">-Version</span></span>
<span data-ttu-id="63788-132">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="63788-133">최신 버전을 사용 하려면 특정 버전 대신 최신 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63788-134">-VM</span><span class="sxs-lookup"><span data-stu-id="63788-134">-VM</span></span>
<span data-ttu-id="63788-135">구성할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-135">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63788-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63788-136">CommonParameters</span></span>
<span data-ttu-id="63788-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63788-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63788-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63788-139">입력</span><span class="sxs-lookup"><span data-stu-id="63788-139">INPUTS</span></span>

### <span data-ttu-id="63788-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="63788-140">PSVirtualMachine</span></span>
<span data-ttu-id="63788-141">' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="63788-142">출력</span><span class="sxs-lookup"><span data-stu-id="63788-142">OUTPUTS</span></span>

### <span data-ttu-id="63788-143">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="63788-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="63788-144">상속자</span><span class="sxs-lookup"><span data-stu-id="63788-144">NOTES</span></span>

## <span data-ttu-id="63788-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63788-145">RELATED LINKS</span></span>

[<span data-ttu-id="63788-146">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="63788-146">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="63788-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="63788-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="63788-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="63788-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="63788-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="63788-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="63788-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="63788-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="63788-151">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="63788-151">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


