---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874698"
---
# <span data-ttu-id="99efb-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="99efb-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="99efb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99efb-102">SYNOPSIS</span></span>
<span data-ttu-id="99efb-103">플랫폼 이미지 리포지토리에서 가상 컴퓨터 이미지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="99efb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99efb-104">SYNTAX</span></span>

### <span data-ttu-id="99efb-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="99efb-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99efb-106">리소스</span><span class="sxs-lookup"><span data-stu-id="99efb-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99efb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="99efb-107">DESCRIPTION</span></span>
<span data-ttu-id="99efb-108">플랫폼 이미지 삭제</span><span class="sxs-lookup"><span data-stu-id="99efb-108">Delete a platform image</span></span>

## <span data-ttu-id="99efb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="99efb-109">EXAMPLES</span></span>

### <span data-ttu-id="99efb-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="99efb-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="99efb-111">기존 플랫폼 이미지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="99efb-112">변수</span><span class="sxs-lookup"><span data-stu-id="99efb-112">PARAMETERS</span></span>

### <span data-ttu-id="99efb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="99efb-113">-Force</span></span>
<span data-ttu-id="99efb-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="99efb-115">-위치</span><span class="sxs-lookup"><span data-stu-id="99efb-115">-Location</span></span>
<span data-ttu-id="99efb-116">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99efb-117">-제공</span><span class="sxs-lookup"><span data-stu-id="99efb-117">-Offer</span></span>
<span data-ttu-id="99efb-118">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-118">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99efb-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="99efb-119">-Publisher</span></span>
<span data-ttu-id="99efb-120">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-120">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99efb-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99efb-121">-ResourceId</span></span>
<span data-ttu-id="99efb-122">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-122">The resource id.</span></span>

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

### <span data-ttu-id="99efb-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="99efb-123">-Sku</span></span>
<span data-ttu-id="99efb-124">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-124">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99efb-125">-버전</span><span class="sxs-lookup"><span data-stu-id="99efb-125">-Version</span></span>
<span data-ttu-id="99efb-126">가상 컴퓨터 이미지의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-126">The version of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99efb-127">-확인</span><span class="sxs-lookup"><span data-stu-id="99efb-127">-Confirm</span></span>
<span data-ttu-id="99efb-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99efb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99efb-129">-WhatIf</span></span>
<span data-ttu-id="99efb-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99efb-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99efb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99efb-132">CommonParameters</span></span>
<span data-ttu-id="99efb-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99efb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99efb-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99efb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99efb-135">입력</span><span class="sxs-lookup"><span data-stu-id="99efb-135">INPUTS</span></span>

## <span data-ttu-id="99efb-136">출력</span><span class="sxs-lookup"><span data-stu-id="99efb-136">OUTPUTS</span></span>

## <span data-ttu-id="99efb-137">상속자</span><span class="sxs-lookup"><span data-stu-id="99efb-137">NOTES</span></span>

## <span data-ttu-id="99efb-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99efb-138">RELATED LINKS</span></span>

