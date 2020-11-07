---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 5bdce17c963cc2529fab3f328b9ab64cc549e1d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711915"
---
# <span data-ttu-id="e7fce-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e7fce-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="e7fce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7fce-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fce-103">VMImage Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7fce-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7fce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7fce-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7fce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e7fce-105">DESCRIPTION</span></span>
<span data-ttu-id="e7fce-106">**Get-AzureRmVMImageSku** Cmdlet은 VMImage sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7fce-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="e7fce-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e7fce-107">EXAMPLES</span></span>

### <span data-ttu-id="e7fce-108">예제 1: VMImage Sku 가져오기</span><span class="sxs-lookup"><span data-stu-id="e7fce-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="e7fce-109">이 명령은 지정 된 게시자 및 제안에 대 한 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7fce-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="e7fce-110">변수</span><span class="sxs-lookup"><span data-stu-id="e7fce-110">PARAMETERS</span></span>

### <span data-ttu-id="e7fce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7fce-111">-DefaultProfile</span></span>
<span data-ttu-id="e7fce-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7fce-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7fce-113">-위치</span><span class="sxs-lookup"><span data-stu-id="e7fce-113">-Location</span></span>
<span data-ttu-id="e7fce-114">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7fce-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="e7fce-115">-제공</span><span class="sxs-lookup"><span data-stu-id="e7fce-115">-Offer</span></span>
<span data-ttu-id="e7fce-116">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7fce-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="e7fce-117">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="e7fce-117">-PublisherName</span></span>
<span data-ttu-id="e7fce-118">VMImage의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7fce-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="e7fce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fce-119">CommonParameters</span></span>
<span data-ttu-id="e7fce-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7fce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fce-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7fce-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fce-122">입력</span><span class="sxs-lookup"><span data-stu-id="e7fce-122">INPUTS</span></span>

## <span data-ttu-id="e7fce-123">출력</span><span class="sxs-lookup"><span data-stu-id="e7fce-123">OUTPUTS</span></span>

## <span data-ttu-id="e7fce-124">상속자</span><span class="sxs-lookup"><span data-stu-id="e7fce-124">NOTES</span></span>

## <span data-ttu-id="e7fce-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7fce-125">RELATED LINKS</span></span>

[<span data-ttu-id="e7fce-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e7fce-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="e7fce-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e7fce-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="e7fce-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e7fce-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="e7fce-129">저장-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e7fce-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


