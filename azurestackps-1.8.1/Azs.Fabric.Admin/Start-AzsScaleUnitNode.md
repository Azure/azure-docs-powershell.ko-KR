---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875215"
---
# <span data-ttu-id="6d60e-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="6d60e-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="6d60e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d60e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d60e-103">배율 단위 노드의 전원을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="6d60e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d60e-104">SYNTAX</span></span>

### <span data-ttu-id="6d60e-105">PowerOn (기본값)</span><span class="sxs-lookup"><span data-stu-id="6d60e-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d60e-106">리소스</span><span class="sxs-lookup"><span data-stu-id="6d60e-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d60e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6d60e-107">DESCRIPTION</span></span>
<span data-ttu-id="6d60e-108">배율 단위 노드의 전원을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="6d60e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6d60e-109">EXAMPLES</span></span>

### <span data-ttu-id="6d60e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d60e-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="6d60e-111">ProvisioningState: 성공</span><span class="sxs-lookup"><span data-stu-id="6d60e-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="6d60e-112">배율 단위 노드의 전원을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="6d60e-113">변수</span><span class="sxs-lookup"><span data-stu-id="6d60e-113">PARAMETERS</span></span>

### <span data-ttu-id="6d60e-114">-이름</span><span class="sxs-lookup"><span data-stu-id="6d60e-114">-Name</span></span>
<span data-ttu-id="6d60e-115">배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-115">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d60e-116">-위치</span><span class="sxs-lookup"><span data-stu-id="6d60e-116">-Location</span></span>
<span data-ttu-id="6d60e-117">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d60e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d60e-118">-ResourceGroupName</span></span>
<span data-ttu-id="6d60e-119">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d60e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d60e-120">-ResourceId</span></span>
<span data-ttu-id="6d60e-121">배율 단위 노드 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="6d60e-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d60e-122">-AsJob</span></span>
<span data-ttu-id="6d60e-123">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6d60e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6d60e-124">-Force</span></span>
<span data-ttu-id="6d60e-125">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6d60e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d60e-126">-WhatIf</span></span>
<span data-ttu-id="6d60e-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d60e-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d60e-129">-확인</span><span class="sxs-lookup"><span data-stu-id="6d60e-129">-Confirm</span></span>
<span data-ttu-id="6d60e-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d60e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d60e-131">CommonParameters</span></span>
<span data-ttu-id="6d60e-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d60e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d60e-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d60e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d60e-134">입력</span><span class="sxs-lookup"><span data-stu-id="6d60e-134">INPUTS</span></span>

## <span data-ttu-id="6d60e-135">출력</span><span class="sxs-lookup"><span data-stu-id="6d60e-135">OUTPUTS</span></span>

## <span data-ttu-id="6d60e-136">상속자</span><span class="sxs-lookup"><span data-stu-id="6d60e-136">NOTES</span></span>

## <span data-ttu-id="6d60e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d60e-137">RELATED LINKS</span></span>
