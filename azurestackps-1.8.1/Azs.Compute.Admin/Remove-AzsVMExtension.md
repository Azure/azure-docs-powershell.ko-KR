---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0aa30655a7fa73b6cb53de12f8906ebb59ea5a17
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875031"
---
# <span data-ttu-id="78c08-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="78c08-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="78c08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78c08-102">SYNOPSIS</span></span>
<span data-ttu-id="78c08-103">가상 컴퓨터 확장 이미지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="78c08-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78c08-104">SYNTAX</span></span>

### <span data-ttu-id="78c08-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="78c08-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78c08-106">리소스</span><span class="sxs-lookup"><span data-stu-id="78c08-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78c08-107">설명은</span><span class="sxs-lookup"><span data-stu-id="78c08-107">DESCRIPTION</span></span>
<span data-ttu-id="78c08-108">지정 된 가상 컴퓨터 확장 이미지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="78c08-109">예제의</span><span class="sxs-lookup"><span data-stu-id="78c08-109">EXAMPLES</span></span>

### <span data-ttu-id="78c08-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="78c08-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="78c08-111">플랫폼 이미지 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="78c08-112">변수</span><span class="sxs-lookup"><span data-stu-id="78c08-112">PARAMETERS</span></span>

### <span data-ttu-id="78c08-113">-Force</span><span class="sxs-lookup"><span data-stu-id="78c08-113">-Force</span></span>
<span data-ttu-id="78c08-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="78c08-115">-위치</span><span class="sxs-lookup"><span data-stu-id="78c08-115">-Location</span></span>
<span data-ttu-id="78c08-116">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-116">Location of the resource.</span></span>

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

### <span data-ttu-id="78c08-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="78c08-117">-Publisher</span></span>
<span data-ttu-id="78c08-118">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="78c08-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78c08-119">-ResourceId</span></span>
<span data-ttu-id="78c08-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-120">The resource id.</span></span>

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

### <span data-ttu-id="78c08-121">-Type</span><span class="sxs-lookup"><span data-stu-id="78c08-121">-Type</span></span>
<span data-ttu-id="78c08-122">확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-122">Type of extension.</span></span>

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

### <span data-ttu-id="78c08-123">-버전</span><span class="sxs-lookup"><span data-stu-id="78c08-123">-Version</span></span>
<span data-ttu-id="78c08-124">가상 컴퓨터 확장 이미지의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="78c08-125">-확인</span><span class="sxs-lookup"><span data-stu-id="78c08-125">-Confirm</span></span>
<span data-ttu-id="78c08-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78c08-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78c08-127">-WhatIf</span></span>
<span data-ttu-id="78c08-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78c08-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78c08-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c08-130">CommonParameters</span></span>
<span data-ttu-id="78c08-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c08-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c08-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c08-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c08-133">입력</span><span class="sxs-lookup"><span data-stu-id="78c08-133">INPUTS</span></span>

## <span data-ttu-id="78c08-134">출력</span><span class="sxs-lookup"><span data-stu-id="78c08-134">OUTPUTS</span></span>

## <span data-ttu-id="78c08-135">상속자</span><span class="sxs-lookup"><span data-stu-id="78c08-135">NOTES</span></span>

## <span data-ttu-id="78c08-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78c08-136">RELATED LINKS</span></span>

