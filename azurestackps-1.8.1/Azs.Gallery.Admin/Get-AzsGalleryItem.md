---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875201"
---
# <span data-ttu-id="8b6a5-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="8b6a5-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="8b6a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b6a5-102">SYNOPSIS</span></span>
<span data-ttu-id="8b6a5-103">갤러리 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a5-103">Lists gallery items.</span></span>

## <span data-ttu-id="8b6a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b6a5-104">SYNTAX</span></span>

### <span data-ttu-id="8b6a5-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8b6a5-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="8b6a5-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="8b6a5-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="8b6a5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8b6a5-107">DESCRIPTION</span></span>
<span data-ttu-id="8b6a5-108">Azure Stack Marketplace에서 사용할 수 있는 갤러리 항목 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="8b6a5-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="8b6a5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8b6a5-109">EXAMPLES</span></span>

### <span data-ttu-id="8b6a5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b6a5-110">EXAMPLE 1</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="8b6a5-111">갤러리 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a5-111">List gallery items.</span></span>

### <span data-ttu-id="8b6a5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="8b6a5-112">EXAMPLE 2</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="8b6a5-113">이름으로 갤러리 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a5-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="8b6a5-114">변수</span><span class="sxs-lookup"><span data-stu-id="8b6a5-114">PARAMETERS</span></span>

### <span data-ttu-id="8b6a5-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8b6a5-115">-Name</span></span>
<span data-ttu-id="8b6a5-116">갤러리 항목의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a5-116">Identity of the gallery item.</span></span>
<span data-ttu-id="8b6a5-117">Publisher 이름, 항목 이름 등을 포함 하며 기간으로 구분 된 버전을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a5-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6a5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b6a5-118">CommonParameters</span></span>
<span data-ttu-id="8b6a5-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b6a5-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b6a5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b6a5-121">입력</span><span class="sxs-lookup"><span data-stu-id="8b6a5-121">INPUTS</span></span>

## <span data-ttu-id="8b6a5-122">출력</span><span class="sxs-lookup"><span data-stu-id="8b6a5-122">OUTPUTS</span></span>

### <span data-ttu-id="8b6a5-123">Microsoft AzureStack. 관리자. 모델. m m a 관리</span><span class="sxs-lookup"><span data-stu-id="8b6a5-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="8b6a5-124">상속자</span><span class="sxs-lookup"><span data-stu-id="8b6a5-124">NOTES</span></span>

## <span data-ttu-id="8b6a5-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b6a5-125">RELATED LINKS</span></span>
