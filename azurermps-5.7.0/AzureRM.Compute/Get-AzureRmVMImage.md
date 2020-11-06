---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526963"
---
# <span data-ttu-id="4373f-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4373f-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="4373f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4373f-102">SYNOPSIS</span></span>
<span data-ttu-id="4373f-103">모든 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4373f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4373f-104">SYNTAX</span></span>

### <span data-ttu-id="4373f-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="4373f-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### <span data-ttu-id="4373f-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="4373f-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## <span data-ttu-id="4373f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4373f-107">DESCRIPTION</span></span>
<span data-ttu-id="4373f-108">**AzureRmVMImage** Cmdlet은 VMImage의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="4373f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4373f-109">EXAMPLES</span></span>

### <span data-ttu-id="4373f-110">예제 1: VMImage 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="4373f-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="4373f-111">이 명령은 지정 된 값과 일치 하는 모든 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="4373f-112">변수</span><span class="sxs-lookup"><span data-stu-id="4373f-112">PARAMETERS</span></span>

### <span data-ttu-id="4373f-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="4373f-113">-FilterExpression</span></span>
<span data-ttu-id="4373f-114">필터 식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4373f-115">-위치</span><span class="sxs-lookup"><span data-stu-id="4373f-115">-Location</span></span>
<span data-ttu-id="4373f-116">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-116">Specifies the location of a VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4373f-117">-제공</span><span class="sxs-lookup"><span data-stu-id="4373f-117">-Offer</span></span>
<span data-ttu-id="4373f-118">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-118">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="4373f-119">이미지 제안을 얻으려면 Get-AzureRmVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-119">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4373f-120">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="4373f-120">-PublisherName</span></span>
<span data-ttu-id="4373f-121">VMImage의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-121">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="4373f-122">이미지 게시자를 얻으려면 Get-AzureRmVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-122">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4373f-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="4373f-123">-Skus</span></span>
<span data-ttu-id="4373f-124">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-124">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="4373f-125">SKU를 얻으려면 Get-AzureRmVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-125">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4373f-126">-버전</span><span class="sxs-lookup"><span data-stu-id="4373f-126">-Version</span></span>
<span data-ttu-id="4373f-127">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-127">Specifies the version of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4373f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4373f-128">CommonParameters</span></span>
<span data-ttu-id="4373f-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4373f-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4373f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4373f-131">입력</span><span class="sxs-lookup"><span data-stu-id="4373f-131">INPUTS</span></span>

### <span data-ttu-id="4373f-132">않아야</span><span class="sxs-lookup"><span data-stu-id="4373f-132">None</span></span>
<span data-ttu-id="4373f-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4373f-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4373f-134">출력</span><span class="sxs-lookup"><span data-stu-id="4373f-134">OUTPUTS</span></span>

## <span data-ttu-id="4373f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="4373f-135">NOTES</span></span>

## <span data-ttu-id="4373f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4373f-136">RELATED LINKS</span></span>

[<span data-ttu-id="4373f-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4373f-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="4373f-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4373f-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4373f-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4373f-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="4373f-140">저장-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4373f-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


