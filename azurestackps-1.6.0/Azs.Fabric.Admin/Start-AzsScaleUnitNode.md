---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c5de84b66283d683d121c99c0cf2e0ea27a4a66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523631"
---
# <span data-ttu-id="41e1d-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="41e1d-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="41e1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="41e1d-103">배율 단위 노드의 전원을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="41e1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41e1d-104">SYNTAX</span></span>

### <span data-ttu-id="41e1d-105">PowerOn (기본값)</span><span class="sxs-lookup"><span data-stu-id="41e1d-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41e1d-106">리소스</span><span class="sxs-lookup"><span data-stu-id="41e1d-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41e1d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="41e1d-107">DESCRIPTION</span></span>
<span data-ttu-id="41e1d-108">배율 단위 노드의 전원을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="41e1d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="41e1d-109">EXAMPLES</span></span>

### <span data-ttu-id="41e1d-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="41e1d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="41e1d-111">ProvisioningState: 성공</span><span class="sxs-lookup"><span data-stu-id="41e1d-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="41e1d-112">배율 단위 노드의 전원을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="41e1d-113">변수</span><span class="sxs-lookup"><span data-stu-id="41e1d-113">PARAMETERS</span></span>

### <span data-ttu-id="41e1d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41e1d-114">-AsJob</span></span>
<span data-ttu-id="41e1d-115">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="41e1d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="41e1d-116">-Force</span></span>
<span data-ttu-id="41e1d-117">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="41e1d-118">-위치</span><span class="sxs-lookup"><span data-stu-id="41e1d-118">-Location</span></span>
<span data-ttu-id="41e1d-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-119">Location of the resource.</span></span>

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

### <span data-ttu-id="41e1d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="41e1d-120">-Name</span></span>
<span data-ttu-id="41e1d-121">배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="41e1d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e1d-122">-ResourceGroupName</span></span>
<span data-ttu-id="41e1d-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="41e1d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41e1d-124">-ResourceId</span></span>
<span data-ttu-id="41e1d-125">배율 단위 노드 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-125">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="41e1d-126">-확인</span><span class="sxs-lookup"><span data-stu-id="41e1d-126">-Confirm</span></span>
<span data-ttu-id="41e1d-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41e1d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41e1d-128">-WhatIf</span></span>
<span data-ttu-id="41e1d-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41e1d-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41e1d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e1d-131">CommonParameters</span></span>
<span data-ttu-id="41e1d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e1d-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41e1d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e1d-134">입력</span><span class="sxs-lookup"><span data-stu-id="41e1d-134">INPUTS</span></span>

## <span data-ttu-id="41e1d-135">출력</span><span class="sxs-lookup"><span data-stu-id="41e1d-135">OUTPUTS</span></span>

## <span data-ttu-id="41e1d-136">상속자</span><span class="sxs-lookup"><span data-stu-id="41e1d-136">NOTES</span></span>

## <span data-ttu-id="41e1d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41e1d-137">RELATED LINKS</span></span>

