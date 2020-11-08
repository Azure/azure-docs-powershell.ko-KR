---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8fc33149fa47c6c70207bebfe87e554fe7eb60cf
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047138"
---
# <span data-ttu-id="fa883-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="fa883-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="fa883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa883-102">SYNOPSIS</span></span>
<span data-ttu-id="fa883-103">특정 갤러리 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa883-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="fa883-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa883-104">SYNTAX</span></span>

### <span data-ttu-id="fa883-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fa883-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa883-106">리소스</span><span class="sxs-lookup"><span data-stu-id="fa883-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa883-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fa883-107">DESCRIPTION</span></span>
<span data-ttu-id="fa883-108">특정 갤러리 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa883-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="fa883-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fa883-109">EXAMPLES</span></span>

### <span data-ttu-id="fa883-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fa883-110">EXAMPLE 1</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="fa883-111">갤러리 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa883-111">Delete a gallery item.</span></span>

## <span data-ttu-id="fa883-112">변수</span><span class="sxs-lookup"><span data-stu-id="fa883-112">PARAMETERS</span></span>

### <span data-ttu-id="fa883-113">-이름</span><span class="sxs-lookup"><span data-stu-id="fa883-113">-Name</span></span>
<span data-ttu-id="fa883-114">갤러리 항목의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="fa883-114">Identity of the gallery item.</span></span>
<span data-ttu-id="fa883-115">Publisher 이름, 항목 이름 등을 포함 하며 기간으로 구분 된 버전을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa883-115">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa883-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa883-116">-ResourceId</span></span>
<span data-ttu-id="fa883-117">정규화 된 Azure 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fa883-117">Fully qualified Azure resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa883-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fa883-118">-Force</span></span>
<span data-ttu-id="fa883-119">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa883-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fa883-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa883-120">-WhatIf</span></span>
<span data-ttu-id="fa883-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa883-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa883-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa883-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa883-123">-확인</span><span class="sxs-lookup"><span data-stu-id="fa883-123">-Confirm</span></span>
<span data-ttu-id="fa883-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa883-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa883-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa883-125">CommonParameters</span></span>
<span data-ttu-id="fa883-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa883-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa883-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa883-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa883-128">입력</span><span class="sxs-lookup"><span data-stu-id="fa883-128">INPUTS</span></span>

## <span data-ttu-id="fa883-129">출력</span><span class="sxs-lookup"><span data-stu-id="fa883-129">OUTPUTS</span></span>

## <span data-ttu-id="fa883-130">상속자</span><span class="sxs-lookup"><span data-stu-id="fa883-130">NOTES</span></span>

## <span data-ttu-id="fa883-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa883-131">RELATED LINKS</span></span>
