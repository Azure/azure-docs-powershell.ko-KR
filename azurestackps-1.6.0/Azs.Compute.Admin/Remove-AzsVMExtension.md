---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f87690c20357cbff7f85a405dd6d3fae3a72dc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522968"
---
# <span data-ttu-id="14db7-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="14db7-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="14db7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14db7-102">SYNOPSIS</span></span>
<span data-ttu-id="14db7-103">가상 컴퓨터 확장 이미지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="14db7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14db7-104">SYNTAX</span></span>

### <span data-ttu-id="14db7-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="14db7-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14db7-106">리소스</span><span class="sxs-lookup"><span data-stu-id="14db7-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14db7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="14db7-107">DESCRIPTION</span></span>
<span data-ttu-id="14db7-108">지정 된 가상 컴퓨터 확장 이미지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="14db7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="14db7-109">EXAMPLES</span></span>

### <span data-ttu-id="14db7-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="14db7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="14db7-111">플랫폼 이미지 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="14db7-112">변수</span><span class="sxs-lookup"><span data-stu-id="14db7-112">PARAMETERS</span></span>

### <span data-ttu-id="14db7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="14db7-113">-Force</span></span>
<span data-ttu-id="14db7-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="14db7-115">-위치</span><span class="sxs-lookup"><span data-stu-id="14db7-115">-Location</span></span>
<span data-ttu-id="14db7-116">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-116">Location of the resource.</span></span>

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

### <span data-ttu-id="14db7-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="14db7-117">-Publisher</span></span>
<span data-ttu-id="14db7-118">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="14db7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14db7-119">-ResourceId</span></span>
<span data-ttu-id="14db7-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-120">The resource id.</span></span>

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

### <span data-ttu-id="14db7-121">-Type</span><span class="sxs-lookup"><span data-stu-id="14db7-121">-Type</span></span>
<span data-ttu-id="14db7-122">확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-122">Type of extension.</span></span>

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

### <span data-ttu-id="14db7-123">-버전</span><span class="sxs-lookup"><span data-stu-id="14db7-123">-Version</span></span>
<span data-ttu-id="14db7-124">가상 컴퓨터 확장 이미지의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="14db7-125">-확인</span><span class="sxs-lookup"><span data-stu-id="14db7-125">-Confirm</span></span>
<span data-ttu-id="14db7-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14db7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14db7-127">-WhatIf</span></span>
<span data-ttu-id="14db7-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14db7-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14db7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14db7-130">CommonParameters</span></span>
<span data-ttu-id="14db7-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14db7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14db7-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14db7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14db7-133">입력</span><span class="sxs-lookup"><span data-stu-id="14db7-133">INPUTS</span></span>

## <span data-ttu-id="14db7-134">출력</span><span class="sxs-lookup"><span data-stu-id="14db7-134">OUTPUTS</span></span>

## <span data-ttu-id="14db7-135">상속자</span><span class="sxs-lookup"><span data-stu-id="14db7-135">NOTES</span></span>

## <span data-ttu-id="14db7-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14db7-136">RELATED LINKS</span></span>

