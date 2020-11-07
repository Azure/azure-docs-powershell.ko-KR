---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 148cfa9db340b4a10e02b0870fc2edb5efb20a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701757"
---
# <span data-ttu-id="3b081-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="3b081-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="3b081-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b081-102">SYNOPSIS</span></span>
<span data-ttu-id="3b081-103">특정 갤러리 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b081-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="3b081-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b081-104">SYNTAX</span></span>

### <span data-ttu-id="3b081-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3b081-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b081-106">리소스</span><span class="sxs-lookup"><span data-stu-id="3b081-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b081-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3b081-107">DESCRIPTION</span></span>
<span data-ttu-id="3b081-108">특정 갤러리 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b081-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="3b081-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3b081-109">EXAMPLES</span></span>

### <span data-ttu-id="3b081-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3b081-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="3b081-111">갤러리 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b081-111">Delete a gallery item.</span></span>

## <span data-ttu-id="3b081-112">변수</span><span class="sxs-lookup"><span data-stu-id="3b081-112">PARAMETERS</span></span>

### <span data-ttu-id="3b081-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3b081-113">-Force</span></span>
<span data-ttu-id="3b081-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b081-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3b081-115">-이름</span><span class="sxs-lookup"><span data-stu-id="3b081-115">-Name</span></span>
<span data-ttu-id="3b081-116">갤러리 항목의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="3b081-116">Identity of the gallery item.</span></span>
<span data-ttu-id="3b081-117">Publisher 이름, 항목 이름 등을 포함 하며 기간으로 구분 된 버전을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b081-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="3b081-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b081-118">-ResourceId</span></span>
<span data-ttu-id="3b081-119">정규화 된 Azure 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3b081-119">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="3b081-120">-확인</span><span class="sxs-lookup"><span data-stu-id="3b081-120">-Confirm</span></span>
<span data-ttu-id="3b081-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b081-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b081-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b081-122">-WhatIf</span></span>
<span data-ttu-id="3b081-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3b081-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b081-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b081-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b081-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b081-125">CommonParameters</span></span>
<span data-ttu-id="3b081-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b081-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b081-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b081-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b081-128">입력</span><span class="sxs-lookup"><span data-stu-id="3b081-128">INPUTS</span></span>

## <span data-ttu-id="3b081-129">출력</span><span class="sxs-lookup"><span data-stu-id="3b081-129">OUTPUTS</span></span>

## <span data-ttu-id="3b081-130">상속자</span><span class="sxs-lookup"><span data-stu-id="3b081-130">NOTES</span></span>

## <span data-ttu-id="3b081-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b081-131">RELATED LINKS</span></span>

