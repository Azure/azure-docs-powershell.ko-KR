---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 7b7a61c6d3043fcb4687d75ac49400b88361b81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877058"
---
# <span data-ttu-id="8a58b-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8a58b-101">Get-AzVMImage</span></span>

## <span data-ttu-id="8a58b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a58b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a58b-103">모든 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="8a58b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a58b-104">SYNTAX</span></span>

### <span data-ttu-id="8a58b-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="8a58b-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a58b-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="8a58b-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a58b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8a58b-107">DESCRIPTION</span></span>
<span data-ttu-id="8a58b-108">**AzVMImage** Cmdlet은 VMImage의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="8a58b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8a58b-109">EXAMPLES</span></span>

### <span data-ttu-id="8a58b-110">예제 1: VMImage 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="8a58b-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="8a58b-111">이 명령은 지정 된 값과 일치 하는 모든 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="8a58b-112">변수</span><span class="sxs-lookup"><span data-stu-id="8a58b-112">PARAMETERS</span></span>

### <span data-ttu-id="8a58b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a58b-113">-DefaultProfile</span></span>
<span data-ttu-id="8a58b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a58b-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="8a58b-115">-FilterExpression</span></span>
<span data-ttu-id="8a58b-116">필터 식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="8a58b-117">-위치</span><span class="sxs-lookup"><span data-stu-id="8a58b-117">-Location</span></span>
<span data-ttu-id="8a58b-118">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="8a58b-119">-제공</span><span class="sxs-lookup"><span data-stu-id="8a58b-119">-Offer</span></span>
<span data-ttu-id="8a58b-120">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="8a58b-121">이미지 제안을 얻으려면 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-121">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="8a58b-122">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="8a58b-122">-PublisherName</span></span>
<span data-ttu-id="8a58b-123">VMImage의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="8a58b-124">이미지 게시자를 얻으려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-124">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="8a58b-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="8a58b-125">-Skus</span></span>
<span data-ttu-id="8a58b-126">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="8a58b-127">SKU를 얻으려면 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-127">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="8a58b-128">-버전</span><span class="sxs-lookup"><span data-stu-id="8a58b-128">-Version</span></span>
<span data-ttu-id="8a58b-129">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="8a58b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a58b-130">CommonParameters</span></span>
<span data-ttu-id="8a58b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a58b-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a58b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a58b-133">입력</span><span class="sxs-lookup"><span data-stu-id="8a58b-133">INPUTS</span></span>

### <span data-ttu-id="8a58b-134">않아야</span><span class="sxs-lookup"><span data-stu-id="8a58b-134">None</span></span>
<span data-ttu-id="8a58b-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a58b-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a58b-136">출력</span><span class="sxs-lookup"><span data-stu-id="8a58b-136">OUTPUTS</span></span>

### <span data-ttu-id="8a58b-137">Microsoft. a \* PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="8a58b-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="8a58b-138">Microsoft. a g m. a g m.</span><span class="sxs-lookup"><span data-stu-id="8a58b-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="8a58b-139">상속자</span><span class="sxs-lookup"><span data-stu-id="8a58b-139">NOTES</span></span>

## <span data-ttu-id="8a58b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a58b-140">RELATED LINKS</span></span>

[<span data-ttu-id="8a58b-141">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8a58b-141">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="8a58b-142">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8a58b-142">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="8a58b-143">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8a58b-143">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="8a58b-144">저장-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8a58b-144">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


