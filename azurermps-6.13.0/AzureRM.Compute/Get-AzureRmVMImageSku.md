---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 5131a9ea24ea14114c9a4d5f5600bbe190499f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530992"
---
# <span data-ttu-id="72c49-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="72c49-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="72c49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72c49-102">SYNOPSIS</span></span>
<span data-ttu-id="72c49-103">VMImage Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="72c49-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72c49-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72c49-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72c49-105">설명은</span><span class="sxs-lookup"><span data-stu-id="72c49-105">DESCRIPTION</span></span>
<span data-ttu-id="72c49-106">**Get-AzureRmVMImageSku** Cmdlet은 VMImage sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="72c49-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="72c49-107">예제의</span><span class="sxs-lookup"><span data-stu-id="72c49-107">EXAMPLES</span></span>

### <span data-ttu-id="72c49-108">예제 1: VMImage Sku 가져오기</span><span class="sxs-lookup"><span data-stu-id="72c49-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="72c49-109">이 명령은 지정 된 게시자 및 제안에 대 한 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="72c49-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="72c49-110">변수</span><span class="sxs-lookup"><span data-stu-id="72c49-110">PARAMETERS</span></span>

### <span data-ttu-id="72c49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c49-111">-DefaultProfile</span></span>
<span data-ttu-id="72c49-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="72c49-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72c49-113">-위치</span><span class="sxs-lookup"><span data-stu-id="72c49-113">-Location</span></span>
<span data-ttu-id="72c49-114">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72c49-114">Specifies the location of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c49-115">-제공</span><span class="sxs-lookup"><span data-stu-id="72c49-115">-Offer</span></span>
<span data-ttu-id="72c49-116">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72c49-116">Specifies the type of VMImage offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c49-117">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="72c49-117">-PublisherName</span></span>
<span data-ttu-id="72c49-118">VMImage의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72c49-118">Specifies the publisher of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c49-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c49-119">CommonParameters</span></span>
<span data-ttu-id="72c49-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72c49-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c49-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72c49-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c49-122">입력</span><span class="sxs-lookup"><span data-stu-id="72c49-122">INPUTS</span></span>

### <span data-ttu-id="72c49-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="72c49-123">System.String</span></span>

## <span data-ttu-id="72c49-124">출력</span><span class="sxs-lookup"><span data-stu-id="72c49-124">OUTPUTS</span></span>

### <span data-ttu-id="72c49-125">PSVirtualMachineImageSku를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="72c49-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="72c49-126">상속자</span><span class="sxs-lookup"><span data-stu-id="72c49-126">NOTES</span></span>

## <span data-ttu-id="72c49-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72c49-127">RELATED LINKS</span></span>

[<span data-ttu-id="72c49-128">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="72c49-128">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="72c49-129">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="72c49-129">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="72c49-130">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="72c49-130">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="72c49-131">저장-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="72c49-131">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


