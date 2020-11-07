---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 7c4b59f97a6cd74da791f090b1c90be72f43a2c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711198"
---
# <span data-ttu-id="928d3-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="928d3-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="928d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="928d3-102">SYNOPSIS</span></span>
<span data-ttu-id="928d3-103">VMImage Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="928d3-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="928d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="928d3-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String> [<CommonParameters>]
```

## <span data-ttu-id="928d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="928d3-105">DESCRIPTION</span></span>
<span data-ttu-id="928d3-106">**Get-AzureRmVMImageSku** Cmdlet은 VMImage sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="928d3-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="928d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="928d3-107">EXAMPLES</span></span>

### <span data-ttu-id="928d3-108">예제 1: VMImage Sku 가져오기</span><span class="sxs-lookup"><span data-stu-id="928d3-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="928d3-109">이 명령은 지정 된 게시자 및 제안에 대 한 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="928d3-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="928d3-110">변수</span><span class="sxs-lookup"><span data-stu-id="928d3-110">PARAMETERS</span></span>

### <span data-ttu-id="928d3-111">-위치</span><span class="sxs-lookup"><span data-stu-id="928d3-111">-Location</span></span>
<span data-ttu-id="928d3-112">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="928d3-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="928d3-113">-제공</span><span class="sxs-lookup"><span data-stu-id="928d3-113">-Offer</span></span>
<span data-ttu-id="928d3-114">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="928d3-114">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="928d3-115">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="928d3-115">-PublisherName</span></span>
<span data-ttu-id="928d3-116">VMImage의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="928d3-116">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="928d3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928d3-117">CommonParameters</span></span>
<span data-ttu-id="928d3-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="928d3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928d3-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928d3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928d3-120">입력</span><span class="sxs-lookup"><span data-stu-id="928d3-120">INPUTS</span></span>

### <span data-ttu-id="928d3-121">않아야</span><span class="sxs-lookup"><span data-stu-id="928d3-121">None</span></span>
<span data-ttu-id="928d3-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="928d3-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="928d3-123">출력</span><span class="sxs-lookup"><span data-stu-id="928d3-123">OUTPUTS</span></span>

## <span data-ttu-id="928d3-124">상속자</span><span class="sxs-lookup"><span data-stu-id="928d3-124">NOTES</span></span>

## <span data-ttu-id="928d3-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="928d3-125">RELATED LINKS</span></span>

[<span data-ttu-id="928d3-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="928d3-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="928d3-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="928d3-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="928d3-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="928d3-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="928d3-129">저장-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="928d3-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


