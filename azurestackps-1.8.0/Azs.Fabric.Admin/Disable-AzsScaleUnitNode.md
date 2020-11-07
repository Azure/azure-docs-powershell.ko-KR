---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874690"
---
# <span data-ttu-id="37cb1-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="37cb1-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="37cb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="37cb1-103">확장 단위 노드의 유지 관리 모드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="37cb1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37cb1-104">SYNTAX</span></span>

### <span data-ttu-id="37cb1-105">사용 안 함 (기본값)</span><span class="sxs-lookup"><span data-stu-id="37cb1-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37cb1-106">리소스</span><span class="sxs-lookup"><span data-stu-id="37cb1-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37cb1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="37cb1-107">DESCRIPTION</span></span>
<span data-ttu-id="37cb1-108">확장 단위 노드의 유지 관리 모드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="37cb1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="37cb1-109">EXAMPLES</span></span>

### <span data-ttu-id="37cb1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="37cb1-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="37cb1-111">배율 단위 노드에 대 한 유지 관리 모드를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="37cb1-112">변수</span><span class="sxs-lookup"><span data-stu-id="37cb1-112">PARAMETERS</span></span>

### <span data-ttu-id="37cb1-113">-이름</span><span class="sxs-lookup"><span data-stu-id="37cb1-113">-Name</span></span>
<span data-ttu-id="37cb1-114">배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cb1-115">-위치</span><span class="sxs-lookup"><span data-stu-id="37cb1-115">-Location</span></span>
<span data-ttu-id="37cb1-116">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cb1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37cb1-117">-ResourceGroupName</span></span>
<span data-ttu-id="37cb1-118">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cb1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37cb1-119">-ResourceId</span></span>
<span data-ttu-id="37cb1-120">배율 단위 노드 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="37cb1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37cb1-121">-AsJob</span></span>
<span data-ttu-id="37cb1-122">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="37cb1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="37cb1-123">-Force</span></span>
<span data-ttu-id="37cb1-124">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="37cb1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37cb1-125">-WhatIf</span></span>
<span data-ttu-id="37cb1-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37cb1-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37cb1-128">-확인</span><span class="sxs-lookup"><span data-stu-id="37cb1-128">-Confirm</span></span>
<span data-ttu-id="37cb1-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37cb1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cb1-130">CommonParameters</span></span>
<span data-ttu-id="37cb1-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cb1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cb1-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37cb1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cb1-133">입력</span><span class="sxs-lookup"><span data-stu-id="37cb1-133">INPUTS</span></span>

## <span data-ttu-id="37cb1-134">출력</span><span class="sxs-lookup"><span data-stu-id="37cb1-134">OUTPUTS</span></span>

## <span data-ttu-id="37cb1-135">상속자</span><span class="sxs-lookup"><span data-stu-id="37cb1-135">NOTES</span></span>

## <span data-ttu-id="37cb1-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37cb1-136">RELATED LINKS</span></span>
