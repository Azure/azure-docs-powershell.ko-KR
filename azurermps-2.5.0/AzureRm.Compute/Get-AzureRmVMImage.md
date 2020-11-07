---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: c69474929fa91b2e4ae1c7f4e50d5961a9322f66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881610"
---
# <span data-ttu-id="e75ea-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e75ea-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="e75ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e75ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e75ea-103">모든 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e75ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e75ea-104">SYNTAX</span></span>

### <span data-ttu-id="e75ea-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="e75ea-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e75ea-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="e75ea-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e75ea-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e75ea-107">DESCRIPTION</span></span>
<span data-ttu-id="e75ea-108">**AzureRmVMImage** Cmdlet은 VMImage의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="e75ea-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e75ea-109">EXAMPLES</span></span>

### <span data-ttu-id="e75ea-110">예제 1: VMImage 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="e75ea-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="e75ea-111">이 명령은 지정 된 값과 일치 하는 모든 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="e75ea-112">변수</span><span class="sxs-lookup"><span data-stu-id="e75ea-112">PARAMETERS</span></span>

### <span data-ttu-id="e75ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e75ea-113">-DefaultProfile</span></span>
<span data-ttu-id="e75ea-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e75ea-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="e75ea-115">-FilterExpression</span></span>
<span data-ttu-id="e75ea-116">필터 식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="e75ea-117">-위치</span><span class="sxs-lookup"><span data-stu-id="e75ea-117">-Location</span></span>
<span data-ttu-id="e75ea-118">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="e75ea-119">-제공</span><span class="sxs-lookup"><span data-stu-id="e75ea-119">-Offer</span></span>
<span data-ttu-id="e75ea-120">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="e75ea-121">이미지 제안을 얻으려면 Get-AzureRmVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="e75ea-122">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="e75ea-122">-PublisherName</span></span>
<span data-ttu-id="e75ea-123">VMImage의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="e75ea-124">이미지 게시자를 얻으려면 Get-AzureRmVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="e75ea-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="e75ea-125">-Skus</span></span>
<span data-ttu-id="e75ea-126">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="e75ea-127">SKU를 얻으려면 Get-AzureRmVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="e75ea-128">-버전</span><span class="sxs-lookup"><span data-stu-id="e75ea-128">-Version</span></span>
<span data-ttu-id="e75ea-129">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="e75ea-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e75ea-130">CommonParameters</span></span>
<span data-ttu-id="e75ea-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e75ea-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e75ea-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e75ea-133">입력</span><span class="sxs-lookup"><span data-stu-id="e75ea-133">INPUTS</span></span>

### <span data-ttu-id="e75ea-134">않아야</span><span class="sxs-lookup"><span data-stu-id="e75ea-134">None</span></span>
<span data-ttu-id="e75ea-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e75ea-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e75ea-136">출력</span><span class="sxs-lookup"><span data-stu-id="e75ea-136">OUTPUTS</span></span>

### <span data-ttu-id="e75ea-137">Microsoft. a \* PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="e75ea-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="e75ea-138">Microsoft. a g m. a g m.</span><span class="sxs-lookup"><span data-stu-id="e75ea-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="e75ea-139">상속자</span><span class="sxs-lookup"><span data-stu-id="e75ea-139">NOTES</span></span>

## <span data-ttu-id="e75ea-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e75ea-140">RELATED LINKS</span></span>

[<span data-ttu-id="e75ea-141">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e75ea-141">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="e75ea-142">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e75ea-142">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="e75ea-143">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e75ea-143">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="e75ea-144">저장-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e75ea-144">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


