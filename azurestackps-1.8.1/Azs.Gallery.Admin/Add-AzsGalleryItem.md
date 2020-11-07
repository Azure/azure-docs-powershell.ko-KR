---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875203"
---
# <span data-ttu-id="d7b80-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="d7b80-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="d7b80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7b80-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b80-103">저장소에 공급자 갤러리 항목을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b80-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="d7b80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7b80-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7b80-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d7b80-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b80-106">저장소에 공급자 갤러리 항목을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b80-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="d7b80-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d7b80-107">EXAMPLES</span></span>

### <span data-ttu-id="d7b80-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7b80-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="d7b80-109">새 갤러리 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7b80-109">Create a new gallery item.</span></span>

## <span data-ttu-id="d7b80-110">변수</span><span class="sxs-lookup"><span data-stu-id="d7b80-110">PARAMETERS</span></span>

### <span data-ttu-id="d7b80-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="d7b80-111">-GalleryItemUri</span></span>
<span data-ttu-id="d7b80-112">갤러리 항목 JSON 파일에 대 한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="d7b80-112">The URI to the gallery item JSON file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b80-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d7b80-113">-Force</span></span>
<span data-ttu-id="d7b80-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7b80-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b80-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b80-115">-WhatIf</span></span>
<span data-ttu-id="d7b80-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7b80-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7b80-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7b80-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b80-118">-확인</span><span class="sxs-lookup"><span data-stu-id="d7b80-118">-Confirm</span></span>
<span data-ttu-id="d7b80-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b80-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b80-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b80-120">CommonParameters</span></span>
<span data-ttu-id="d7b80-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b80-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b80-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b80-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b80-123">입력</span><span class="sxs-lookup"><span data-stu-id="d7b80-123">INPUTS</span></span>

## <span data-ttu-id="d7b80-124">출력</span><span class="sxs-lookup"><span data-stu-id="d7b80-124">OUTPUTS</span></span>

### <span data-ttu-id="d7b80-125">Microsoft AzureStack. 관리자. 모델. m m a 관리</span><span class="sxs-lookup"><span data-stu-id="d7b80-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="d7b80-126">상속자</span><span class="sxs-lookup"><span data-stu-id="d7b80-126">NOTES</span></span>

## <span data-ttu-id="d7b80-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7b80-127">RELATED LINKS</span></span>
