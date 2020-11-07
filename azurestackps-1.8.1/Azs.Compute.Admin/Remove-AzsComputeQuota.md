---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ebc1ebae40d6d1726ee6c23def6f82ff1efc8517
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875042"
---
# <span data-ttu-id="fa545-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="fa545-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="fa545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa545-102">SYNOPSIS</span></span>
<span data-ttu-id="fa545-103">지정 된 계산 할당량을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="fa545-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa545-104">SYNTAX</span></span>

### <span data-ttu-id="fa545-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fa545-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa545-106">리소스</span><span class="sxs-lookup"><span data-stu-id="fa545-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa545-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fa545-107">DESCRIPTION</span></span>
<span data-ttu-id="fa545-108">기존 할당량을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-108">Delete an existing quota.</span></span>

## <span data-ttu-id="fa545-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fa545-109">EXAMPLES</span></span>

### <span data-ttu-id="fa545-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fa545-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="fa545-111">모든 매개 변수가 지정 된 계산 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="fa545-112">변수</span><span class="sxs-lookup"><span data-stu-id="fa545-112">PARAMETERS</span></span>

### <span data-ttu-id="fa545-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fa545-113">-Force</span></span>
<span data-ttu-id="fa545-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fa545-115">-위치</span><span class="sxs-lookup"><span data-stu-id="fa545-115">-Location</span></span>
<span data-ttu-id="fa545-116">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-116">Location of the resource.</span></span> <span data-ttu-id="fa545-117">지정 하지 않은 경우, tenat의 구독에 바인딩된 위치를 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-117">If not given we default to the location bound to the tenat's subscription.</span></span>

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

### <span data-ttu-id="fa545-118">-이름</span><span class="sxs-lookup"><span data-stu-id="fa545-118">-Name</span></span>
<span data-ttu-id="fa545-119">할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-119">Name of the quota.</span></span>

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

### <span data-ttu-id="fa545-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa545-120">-ResourceId</span></span>
<span data-ttu-id="fa545-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-121">The resource id.</span></span>

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

### <span data-ttu-id="fa545-122">-확인</span><span class="sxs-lookup"><span data-stu-id="fa545-122">-Confirm</span></span>
<span data-ttu-id="fa545-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa545-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa545-124">-WhatIf</span></span>
<span data-ttu-id="fa545-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa545-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa545-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa545-127">CommonParameters</span></span>
<span data-ttu-id="fa545-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa545-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa545-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa545-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa545-130">입력</span><span class="sxs-lookup"><span data-stu-id="fa545-130">INPUTS</span></span>

## <span data-ttu-id="fa545-131">출력</span><span class="sxs-lookup"><span data-stu-id="fa545-131">OUTPUTS</span></span>

## <span data-ttu-id="fa545-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fa545-132">NOTES</span></span>

## <span data-ttu-id="fa545-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa545-133">RELATED LINKS</span></span>

