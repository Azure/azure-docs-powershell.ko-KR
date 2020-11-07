---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
ms.openlocfilehash: 8d2253e20e87a0e6a5d97f2dd0e405412f5a9282
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882389"
---
# <span data-ttu-id="d510e-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d510e-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="d510e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d510e-102">SYNOPSIS</span></span>
<span data-ttu-id="d510e-103">VMImage Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d510e-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d510e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d510e-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d510e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d510e-105">DESCRIPTION</span></span>
<span data-ttu-id="d510e-106">**Get-AzureRmVMImageSku** Cmdlet은 VMImage sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d510e-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="d510e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d510e-107">EXAMPLES</span></span>

### <span data-ttu-id="d510e-108">예제 1: VMImage Sku 가져오기</span><span class="sxs-lookup"><span data-stu-id="d510e-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="d510e-109">이 명령은 지정 된 게시자 및 제안에 대 한 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d510e-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="d510e-110">변수</span><span class="sxs-lookup"><span data-stu-id="d510e-110">PARAMETERS</span></span>

### <span data-ttu-id="d510e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d510e-111">-DefaultProfile</span></span>
<span data-ttu-id="d510e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d510e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d510e-113">-위치</span><span class="sxs-lookup"><span data-stu-id="d510e-113">-Location</span></span>
<span data-ttu-id="d510e-114">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d510e-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="d510e-115">-제공</span><span class="sxs-lookup"><span data-stu-id="d510e-115">-Offer</span></span>
<span data-ttu-id="d510e-116">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d510e-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="d510e-117">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="d510e-117">-PublisherName</span></span>
<span data-ttu-id="d510e-118">VMImage의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d510e-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="d510e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d510e-119">CommonParameters</span></span>
<span data-ttu-id="d510e-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d510e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d510e-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d510e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d510e-122">입력</span><span class="sxs-lookup"><span data-stu-id="d510e-122">INPUTS</span></span>

### <span data-ttu-id="d510e-123">않아야</span><span class="sxs-lookup"><span data-stu-id="d510e-123">None</span></span>
<span data-ttu-id="d510e-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d510e-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d510e-125">출력</span><span class="sxs-lookup"><span data-stu-id="d510e-125">OUTPUTS</span></span>

### <span data-ttu-id="d510e-126">PSVirtualMachineImageSku를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="d510e-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="d510e-127">상속자</span><span class="sxs-lookup"><span data-stu-id="d510e-127">NOTES</span></span>

## <span data-ttu-id="d510e-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d510e-128">RELATED LINKS</span></span>

[<span data-ttu-id="d510e-129">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d510e-129">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="d510e-130">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d510e-130">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="d510e-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d510e-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="d510e-132">저장-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d510e-132">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


