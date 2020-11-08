---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047110"
---
# <span data-ttu-id="0f424-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="0f424-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="0f424-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f424-102">SYNOPSIS</span></span>
<span data-ttu-id="0f424-103">영역의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f424-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="0f424-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f424-104">SYNTAX</span></span>

### <span data-ttu-id="0f424-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0f424-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f424-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="0f424-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f424-107">리소스</span><span class="sxs-lookup"><span data-stu-id="0f424-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0f424-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0f424-108">DESCRIPTION</span></span>
<span data-ttu-id="0f424-109">영역의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f424-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="0f424-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0f424-110">EXAMPLES</span></span>

### <span data-ttu-id="0f424-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0f424-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="0f424-112">영역의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f424-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="0f424-113">변수</span><span class="sxs-lookup"><span data-stu-id="0f424-113">PARAMETERS</span></span>

### <span data-ttu-id="0f424-114">-위치</span><span class="sxs-lookup"><span data-stu-id="0f424-114">-Location</span></span>
<span data-ttu-id="0f424-115">지역 이름</span><span class="sxs-lookup"><span data-stu-id="0f424-115">Name of the region</span></span>

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

### <span data-ttu-id="0f424-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f424-116">-ResourceGroupName</span></span>
<span data-ttu-id="0f424-117">리소스 그룹 이름, 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0f424-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="0f424-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f424-118">-ResourceId</span></span>
<span data-ttu-id="0f424-119">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0f424-119">The resource id.</span></span>

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

### <span data-ttu-id="0f424-120">-필터</span><span class="sxs-lookup"><span data-stu-id="0f424-120">-Filter</span></span>
<span data-ttu-id="0f424-121">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="0f424-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="0f424-122">-위쪽</span><span class="sxs-lookup"><span data-stu-id="0f424-122">-Top</span></span>
<span data-ttu-id="0f424-123">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f424-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0f424-124">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f424-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0f424-125">-생략</span><span class="sxs-lookup"><span data-stu-id="0f424-125">-Skip</span></span>
<span data-ttu-id="0f424-126">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="0f424-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0f424-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f424-127">CommonParameters</span></span>
<span data-ttu-id="0f424-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f424-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f424-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f424-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f424-130">입력</span><span class="sxs-lookup"><span data-stu-id="0f424-130">INPUTS</span></span>

## <span data-ttu-id="0f424-131">출력</span><span class="sxs-lookup"><span data-stu-id="0f424-131">OUTPUTS</span></span>

### <span data-ttu-id="0f424-132">InfrastructureInsights. 지역 건강 관리 모델. 지역/국가</span><span class="sxs-lookup"><span data-stu-id="0f424-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="0f424-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0f424-133">NOTES</span></span>

## <span data-ttu-id="0f424-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f424-134">RELATED LINKS</span></span>
