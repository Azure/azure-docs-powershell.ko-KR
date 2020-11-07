---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6de990526330cdd192cd99707aacc1e06ad49c5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874500"
---
# <span data-ttu-id="65588-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="65588-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="65588-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65588-102">SYNOPSIS</span></span>
<span data-ttu-id="65588-103">배율 단위 노드의 전원을 끕니다.</span><span class="sxs-lookup"><span data-stu-id="65588-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="65588-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65588-104">SYNTAX</span></span>

### <span data-ttu-id="65588-105">중지 (기본값)</span><span class="sxs-lookup"><span data-stu-id="65588-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65588-106">리소스</span><span class="sxs-lookup"><span data-stu-id="65588-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65588-107">설명은</span><span class="sxs-lookup"><span data-stu-id="65588-107">DESCRIPTION</span></span>
<span data-ttu-id="65588-108">배율 단위 노드의 전원을 끕니다.</span><span class="sxs-lookup"><span data-stu-id="65588-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="65588-109">예제의</span><span class="sxs-lookup"><span data-stu-id="65588-109">EXAMPLES</span></span>

### <span data-ttu-id="65588-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="65588-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="65588-111">배율 단위 노드를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="65588-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="65588-112">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="65588-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="65588-113">배율 단위 노드 전원을 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="65588-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="65588-114">변수</span><span class="sxs-lookup"><span data-stu-id="65588-114">PARAMETERS</span></span>

### <span data-ttu-id="65588-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65588-115">-AsJob</span></span>
<span data-ttu-id="65588-116">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65588-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="65588-117">-Force</span><span class="sxs-lookup"><span data-stu-id="65588-117">-Force</span></span>
<span data-ttu-id="65588-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65588-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="65588-119">-위치</span><span class="sxs-lookup"><span data-stu-id="65588-119">-Location</span></span>
<span data-ttu-id="65588-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="65588-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65588-121">-이름</span><span class="sxs-lookup"><span data-stu-id="65588-121">-Name</span></span>
<span data-ttu-id="65588-122">배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65588-122">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65588-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65588-123">-ResourceGroupName</span></span>
<span data-ttu-id="65588-124">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="65588-124">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65588-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65588-125">-ResourceId</span></span>
<span data-ttu-id="65588-126">배율 단위 노드 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="65588-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="65588-127">-종료</span><span class="sxs-lookup"><span data-stu-id="65588-127">-Shutdown</span></span>
<span data-ttu-id="65588-128">설정 된 경우 배율 단위 노드가 적절 하 게 종료 됩니다. 그렇지 않으면 배율 단위 노드의 전원이 꺼집니다.</span><span class="sxs-lookup"><span data-stu-id="65588-128">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="65588-129">-확인</span><span class="sxs-lookup"><span data-stu-id="65588-129">-Confirm</span></span>
<span data-ttu-id="65588-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65588-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65588-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65588-131">-WhatIf</span></span>
<span data-ttu-id="65588-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="65588-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65588-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65588-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65588-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65588-134">CommonParameters</span></span>
<span data-ttu-id="65588-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65588-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65588-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65588-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65588-137">입력</span><span class="sxs-lookup"><span data-stu-id="65588-137">INPUTS</span></span>

## <span data-ttu-id="65588-138">출력</span><span class="sxs-lookup"><span data-stu-id="65588-138">OUTPUTS</span></span>

## <span data-ttu-id="65588-139">상속자</span><span class="sxs-lookup"><span data-stu-id="65588-139">NOTES</span></span>

## <span data-ttu-id="65588-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65588-140">RELATED LINKS</span></span>

