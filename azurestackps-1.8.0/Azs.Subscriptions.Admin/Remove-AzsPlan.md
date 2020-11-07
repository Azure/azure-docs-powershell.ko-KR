---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75010b9591b4211f32c5665aa969bae28d69aaea
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874617"
---
# <span data-ttu-id="b796f-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="b796f-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="b796f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b796f-102">SYNOPSIS</span></span>
<span data-ttu-id="b796f-103">지정 된 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b796f-103">Removes the specified plan</span></span>

## <span data-ttu-id="b796f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b796f-104">SYNTAX</span></span>

### <span data-ttu-id="b796f-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b796f-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b796f-106">리소스</span><span class="sxs-lookup"><span data-stu-id="b796f-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b796f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b796f-107">DESCRIPTION</span></span>
<span data-ttu-id="b796f-108">지정 된 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b796f-108">Removes the specified plan</span></span>

## <span data-ttu-id="b796f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b796f-109">EXAMPLES</span></span>

### <span data-ttu-id="b796f-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b796f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="b796f-111">지정 된 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b796f-111">Removes the specified plan</span></span>

## <span data-ttu-id="b796f-112">변수</span><span class="sxs-lookup"><span data-stu-id="b796f-112">PARAMETERS</span></span>

### <span data-ttu-id="b796f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b796f-113">-Force</span></span>
<span data-ttu-id="b796f-114">확인 하지 않고 항목을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="b796f-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="b796f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b796f-115">-Name</span></span>
<span data-ttu-id="b796f-116">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b796f-116">Name of the plan.</span></span>

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

### <span data-ttu-id="b796f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b796f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b796f-118">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b796f-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="b796f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b796f-119">-ResourceId</span></span>
<span data-ttu-id="b796f-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b796f-120">The resource id.</span></span>

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

### <span data-ttu-id="b796f-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b796f-121">-Confirm</span></span>
<span data-ttu-id="b796f-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b796f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b796f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b796f-123">-WhatIf</span></span>
<span data-ttu-id="b796f-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b796f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b796f-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b796f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b796f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b796f-126">CommonParameters</span></span>
<span data-ttu-id="b796f-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b796f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b796f-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b796f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b796f-129">입력</span><span class="sxs-lookup"><span data-stu-id="b796f-129">INPUTS</span></span>

## <span data-ttu-id="b796f-130">출력</span><span class="sxs-lookup"><span data-stu-id="b796f-130">OUTPUTS</span></span>

## <span data-ttu-id="b796f-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b796f-131">NOTES</span></span>

## <span data-ttu-id="b796f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b796f-132">RELATED LINKS</span></span>

