---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6713b912f962a7a85627ca2280d6195cc5c5d88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874485"
---
# <span data-ttu-id="35afc-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="35afc-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="35afc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35afc-102">SYNOPSIS</span></span>
<span data-ttu-id="35afc-103">영역의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35afc-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="35afc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35afc-104">SYNTAX</span></span>

### <span data-ttu-id="35afc-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="35afc-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="35afc-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="35afc-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="35afc-107">리소스</span><span class="sxs-lookup"><span data-stu-id="35afc-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="35afc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="35afc-108">DESCRIPTION</span></span>
<span data-ttu-id="35afc-109">영역의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35afc-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="35afc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="35afc-110">EXAMPLES</span></span>

### <span data-ttu-id="35afc-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="35afc-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="35afc-112">영역의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35afc-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="35afc-113">변수</span><span class="sxs-lookup"><span data-stu-id="35afc-113">PARAMETERS</span></span>

### <span data-ttu-id="35afc-114">-필터</span><span class="sxs-lookup"><span data-stu-id="35afc-114">-Filter</span></span>
<span data-ttu-id="35afc-115">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="35afc-115">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35afc-116">-위치</span><span class="sxs-lookup"><span data-stu-id="35afc-116">-Location</span></span>
<span data-ttu-id="35afc-117">지역 이름</span><span class="sxs-lookup"><span data-stu-id="35afc-117">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35afc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35afc-118">-ResourceGroupName</span></span>
<span data-ttu-id="35afc-119">리소스가 있는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35afc-119">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35afc-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35afc-120">-ResourceId</span></span>
<span data-ttu-id="35afc-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="35afc-121">The resource id.</span></span>

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

### <span data-ttu-id="35afc-122">-생략</span><span class="sxs-lookup"><span data-stu-id="35afc-122">-Skip</span></span>
<span data-ttu-id="35afc-123">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="35afc-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35afc-124">-위쪽</span><span class="sxs-lookup"><span data-stu-id="35afc-124">-Top</span></span>
<span data-ttu-id="35afc-125">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35afc-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="35afc-126">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35afc-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35afc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35afc-127">CommonParameters</span></span>
<span data-ttu-id="35afc-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35afc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35afc-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35afc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35afc-130">입력</span><span class="sxs-lookup"><span data-stu-id="35afc-130">INPUTS</span></span>

## <span data-ttu-id="35afc-131">출력</span><span class="sxs-lookup"><span data-stu-id="35afc-131">OUTPUTS</span></span>

### <span data-ttu-id="35afc-132">InfrastructureInsights. 지역 건강 관리 모델. 지역/국가</span><span class="sxs-lookup"><span data-stu-id="35afc-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="35afc-133">상속자</span><span class="sxs-lookup"><span data-stu-id="35afc-133">NOTES</span></span>

## <span data-ttu-id="35afc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35afc-134">RELATED LINKS</span></span>

