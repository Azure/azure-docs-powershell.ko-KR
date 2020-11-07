---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa4bd73f9300daf8ca17e3a11d884e06e9852234
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701722"
---
# <span data-ttu-id="daa7c-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="daa7c-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="daa7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daa7c-102">SYNOPSIS</span></span>
<span data-ttu-id="daa7c-103">지정 된 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa7c-103">Removes the specified plan</span></span>

## <span data-ttu-id="daa7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="daa7c-104">SYNTAX</span></span>

### <span data-ttu-id="daa7c-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="daa7c-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daa7c-106">리소스</span><span class="sxs-lookup"><span data-stu-id="daa7c-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daa7c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="daa7c-107">DESCRIPTION</span></span>
<span data-ttu-id="daa7c-108">지정 된 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa7c-108">Removes the specified plan</span></span>

## <span data-ttu-id="daa7c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="daa7c-109">EXAMPLES</span></span>

### <span data-ttu-id="daa7c-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="daa7c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="daa7c-111">지정 된 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa7c-111">Removes the specified plan</span></span>

## <span data-ttu-id="daa7c-112">변수</span><span class="sxs-lookup"><span data-stu-id="daa7c-112">PARAMETERS</span></span>

### <span data-ttu-id="daa7c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="daa7c-113">-Force</span></span>
<span data-ttu-id="daa7c-114">확인 하지 않고 항목을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="daa7c-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="daa7c-115">-이름</span><span class="sxs-lookup"><span data-stu-id="daa7c-115">-Name</span></span>
<span data-ttu-id="daa7c-116">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="daa7c-116">Name of the plan.</span></span>

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

### <span data-ttu-id="daa7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="daa7c-118">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="daa7c-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="daa7c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daa7c-119">-ResourceId</span></span>
<span data-ttu-id="daa7c-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="daa7c-120">The resource id.</span></span>

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

### <span data-ttu-id="daa7c-121">-확인</span><span class="sxs-lookup"><span data-stu-id="daa7c-121">-Confirm</span></span>
<span data-ttu-id="daa7c-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa7c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daa7c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa7c-123">-WhatIf</span></span>
<span data-ttu-id="daa7c-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="daa7c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daa7c-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="daa7c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daa7c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa7c-126">CommonParameters</span></span>
<span data-ttu-id="daa7c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa7c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa7c-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daa7c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa7c-129">입력</span><span class="sxs-lookup"><span data-stu-id="daa7c-129">INPUTS</span></span>

## <span data-ttu-id="daa7c-130">출력</span><span class="sxs-lookup"><span data-stu-id="daa7c-130">OUTPUTS</span></span>

## <span data-ttu-id="daa7c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="daa7c-131">NOTES</span></span>

## <span data-ttu-id="daa7c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="daa7c-132">RELATED LINKS</span></span>

