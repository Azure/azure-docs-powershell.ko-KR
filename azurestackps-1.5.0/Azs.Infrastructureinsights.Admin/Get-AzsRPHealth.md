---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e42278eb4ed402d561399dbd1077f819ef3d2cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523356"
---
# <span data-ttu-id="ea2ea-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="ea2ea-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="ea2ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2ea-103">각 서비스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="ea2ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea2ea-104">SYNTAX</span></span>

### <span data-ttu-id="ea2ea-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea2ea-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ea2ea-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="ea2ea-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ea2ea-107">리소스</span><span class="sxs-lookup"><span data-stu-id="ea2ea-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ea2ea-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ea2ea-108">DESCRIPTION</span></span>
<span data-ttu-id="ea2ea-109">각 서비스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-109">Returns a list of each service's health.</span></span> <span data-ttu-id="ea2ea-110">AlertSummary 속성에는 경고/오류 개수에 대 한 세부 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="ea2ea-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ea2ea-111">EXAMPLES</span></span>

### <span data-ttu-id="ea2ea-112">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ea2ea-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="ea2ea-113">각 서비스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="ea2ea-114">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ea2ea-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="ea2ea-115">서비스의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-115">Returns a service's health.</span></span>

## <span data-ttu-id="ea2ea-116">변수</span><span class="sxs-lookup"><span data-stu-id="ea2ea-116">PARAMETERS</span></span>

### <span data-ttu-id="ea2ea-117">-필터</span><span class="sxs-lookup"><span data-stu-id="ea2ea-117">-Filter</span></span>
<span data-ttu-id="ea2ea-118">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="ea2ea-119">-위치</span><span class="sxs-lookup"><span data-stu-id="ea2ea-119">-Location</span></span>
<span data-ttu-id="ea2ea-120">지역 이름</span><span class="sxs-lookup"><span data-stu-id="ea2ea-120">Name of the region</span></span>

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

### <span data-ttu-id="ea2ea-121">-이름</span><span class="sxs-lookup"><span data-stu-id="ea2ea-121">-Name</span></span>
<span data-ttu-id="ea2ea-122">서비스 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-122">Service Health name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea2ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea2ea-124">리소스가 있는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-124">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="ea2ea-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea2ea-125">-ResourceId</span></span>
<span data-ttu-id="ea2ea-126">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-126">The resource id.</span></span>

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

### <span data-ttu-id="ea2ea-127">-생략</span><span class="sxs-lookup"><span data-stu-id="ea2ea-127">-Skip</span></span>
<span data-ttu-id="ea2ea-128">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ea2ea-129">-위쪽</span><span class="sxs-lookup"><span data-stu-id="ea2ea-129">-Top</span></span>
<span data-ttu-id="ea2ea-130">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ea2ea-131">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ea2ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2ea-132">CommonParameters</span></span>
<span data-ttu-id="ea2ea-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2ea-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea2ea-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2ea-135">입력</span><span class="sxs-lookup"><span data-stu-id="ea2ea-135">INPUTS</span></span>

## <span data-ttu-id="ea2ea-136">출력</span><span class="sxs-lookup"><span data-stu-id="ea2ea-136">OUTPUTS</span></span>

### <span data-ttu-id="ea2ea-137">InfrastructureInsights. w i m. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="ea2ea-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="ea2ea-138">상속자</span><span class="sxs-lookup"><span data-stu-id="ea2ea-138">NOTES</span></span>

## <span data-ttu-id="ea2ea-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea2ea-139">RELATED LINKS</span></span>

