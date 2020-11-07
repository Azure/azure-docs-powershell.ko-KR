---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875217"
---
# <span data-ttu-id="78b0b-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="78b0b-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="78b0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="78b0b-103">확장 단위 노드의 유지 관리 모드를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="78b0b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78b0b-104">SYNTAX</span></span>

### <span data-ttu-id="78b0b-105">사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="78b0b-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78b0b-106">리소스</span><span class="sxs-lookup"><span data-stu-id="78b0b-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78b0b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="78b0b-107">DESCRIPTION</span></span>
<span data-ttu-id="78b0b-108">확장 단위 노드의 유지 관리 모드를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="78b0b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="78b0b-109">EXAMPLES</span></span>

### <span data-ttu-id="78b0b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="78b0b-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="78b0b-111">확장 단위 노드에서 유지 관리 모드를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="78b0b-112">변수</span><span class="sxs-lookup"><span data-stu-id="78b0b-112">PARAMETERS</span></span>

### <span data-ttu-id="78b0b-113">-이름</span><span class="sxs-lookup"><span data-stu-id="78b0b-113">-Name</span></span>
<span data-ttu-id="78b0b-114">배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b0b-115">-위치</span><span class="sxs-lookup"><span data-stu-id="78b0b-115">-Location</span></span>
<span data-ttu-id="78b0b-116">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b0b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78b0b-117">-ResourceGroupName</span></span>
<span data-ttu-id="78b0b-118">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b0b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78b0b-119">-ResourceId</span></span>
<span data-ttu-id="78b0b-120">배율 단위 노드 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="78b0b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78b0b-121">-AsJob</span></span>
<span data-ttu-id="78b0b-122">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="78b0b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="78b0b-123">-Force</span></span>
<span data-ttu-id="78b0b-124">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="78b0b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78b0b-125">-WhatIf</span></span>
<span data-ttu-id="78b0b-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78b0b-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78b0b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="78b0b-128">-Confirm</span></span>
<span data-ttu-id="78b0b-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78b0b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b0b-130">CommonParameters</span></span>
<span data-ttu-id="78b0b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b0b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b0b-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78b0b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b0b-133">입력</span><span class="sxs-lookup"><span data-stu-id="78b0b-133">INPUTS</span></span>

## <span data-ttu-id="78b0b-134">출력</span><span class="sxs-lookup"><span data-stu-id="78b0b-134">OUTPUTS</span></span>

## <span data-ttu-id="78b0b-135">상속자</span><span class="sxs-lookup"><span data-stu-id="78b0b-135">NOTES</span></span>

## <span data-ttu-id="78b0b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78b0b-136">RELATED LINKS</span></span>
