---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875218"
---
# <span data-ttu-id="2a192-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="2a192-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="2a192-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a192-102">SYNOPSIS</span></span>
<span data-ttu-id="2a192-103">새 배율 단위를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-103">Add a new scale unit.</span></span>

## <span data-ttu-id="2a192-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a192-104">SYNTAX</span></span>

### <span data-ttu-id="2a192-105">ScaleOut (기본값)</span><span class="sxs-lookup"><span data-stu-id="2a192-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a192-106">리소스</span><span class="sxs-lookup"><span data-stu-id="2a192-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a192-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2a192-107">DESCRIPTION</span></span>
<span data-ttu-id="2a192-108">새 배율 단위를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-108">Add a new scale unit.</span></span>

## <span data-ttu-id="2a192-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2a192-109">EXAMPLES</span></span>

### <span data-ttu-id="2a192-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2a192-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="2a192-111">새 배율 단위 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="2a192-112">변수</span><span class="sxs-lookup"><span data-stu-id="2a192-112">PARAMETERS</span></span>

### <span data-ttu-id="2a192-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a192-113">-AsJob</span></span>
<span data-ttu-id="2a192-114">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2a192-115">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="2a192-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="2a192-116">플래그는 작업이 반환 되기 전에 저장소가 수렴 될 때까지 대기 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="2a192-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2a192-117">-Force</span></span>
<span data-ttu-id="2a192-118">확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="2a192-118">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="2a192-119">-위치</span><span class="sxs-lookup"><span data-stu-id="2a192-119">-Location</span></span>
<span data-ttu-id="2a192-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a192-121">-이름</span><span class="sxs-lookup"><span data-stu-id="2a192-121">-Name</span></span>
<span data-ttu-id="2a192-122">{{Fill Name Description}}</span><span class="sxs-lookup"><span data-stu-id="2a192-122">{{Fill Name Description}}</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a192-123">-NodeList</span><span class="sxs-lookup"><span data-stu-id="2a192-123">-NodeList</span></span>
<span data-ttu-id="2a192-124">배율 단위 노드의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-124">List of nodes in the scale unit.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a192-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a192-125">-ResourceGroupName</span></span>
<span data-ttu-id="2a192-126">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-126">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a192-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a192-127">-ResourceId</span></span>
<span data-ttu-id="2a192-128">배율 단위 노드 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-128">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="2a192-129">-확인</span><span class="sxs-lookup"><span data-stu-id="2a192-129">-Confirm</span></span>
<span data-ttu-id="2a192-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a192-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a192-131">-WhatIf</span></span>
<span data-ttu-id="2a192-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a192-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a192-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a192-134">CommonParameters</span></span>
<span data-ttu-id="2a192-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a192-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a192-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a192-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a192-137">입력</span><span class="sxs-lookup"><span data-stu-id="2a192-137">INPUTS</span></span>

## <span data-ttu-id="2a192-138">출력</span><span class="sxs-lookup"><span data-stu-id="2a192-138">OUTPUTS</span></span>

## <span data-ttu-id="2a192-139">상속자</span><span class="sxs-lookup"><span data-stu-id="2a192-139">NOTES</span></span>

## <span data-ttu-id="2a192-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a192-140">RELATED LINKS</span></span>

