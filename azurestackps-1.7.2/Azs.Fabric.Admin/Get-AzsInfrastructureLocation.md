---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcd5d112fea0ec68e372a5ad282b3d661f9481ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689089"
---
# <span data-ttu-id="d8a02-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="d8a02-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="d8a02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8a02-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a02-103">모든 패브릭 위치의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a02-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="d8a02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8a02-104">SYNTAX</span></span>

### <span data-ttu-id="d8a02-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d8a02-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8a02-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d8a02-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d8a02-107">리소스</span><span class="sxs-lookup"><span data-stu-id="d8a02-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d8a02-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d8a02-108">DESCRIPTION</span></span>
<span data-ttu-id="d8a02-109">모든 패브릭 위치의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a02-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="d8a02-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d8a02-110">EXAMPLES</span></span>

### <span data-ttu-id="d8a02-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8a02-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="d8a02-112">모든 패브릭 위치 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a02-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="d8a02-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8a02-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="d8a02-114">이름을 기준으로 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a02-114">Return a location based on the name.</span></span>

## <span data-ttu-id="d8a02-115">변수</span><span class="sxs-lookup"><span data-stu-id="d8a02-115">PARAMETERS</span></span>

### <span data-ttu-id="d8a02-116">-필터</span><span class="sxs-lookup"><span data-stu-id="d8a02-116">-Filter</span></span>
<span data-ttu-id="d8a02-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8a02-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="d8a02-118">-위치</span><span class="sxs-lookup"><span data-stu-id="d8a02-118">-Location</span></span>
<span data-ttu-id="d8a02-119">패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="d8a02-119">Fabric location.</span></span>

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

### <span data-ttu-id="d8a02-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8a02-120">-ResourceGroupName</span></span>
<span data-ttu-id="d8a02-121">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="d8a02-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d8a02-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8a02-122">-ResourceId</span></span>
<span data-ttu-id="d8a02-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d8a02-123">The resource id.</span></span>

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

### <span data-ttu-id="d8a02-124">-생략</span><span class="sxs-lookup"><span data-stu-id="d8a02-124">-Skip</span></span>
<span data-ttu-id="d8a02-125">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="d8a02-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d8a02-126">-위쪽</span><span class="sxs-lookup"><span data-stu-id="d8a02-126">-Top</span></span>
<span data-ttu-id="d8a02-127">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a02-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d8a02-128">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8a02-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d8a02-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a02-129">CommonParameters</span></span>
<span data-ttu-id="d8a02-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a02-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a02-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a02-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a02-132">입력</span><span class="sxs-lookup"><span data-stu-id="d8a02-132">INPUTS</span></span>

## <span data-ttu-id="d8a02-133">출력</span><span class="sxs-lookup"><span data-stu-id="d8a02-133">OUTPUTS</span></span>

### <span data-ttu-id="d8a02-134">FabricLocation. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="d8a02-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="d8a02-135">상속자</span><span class="sxs-lookup"><span data-stu-id="d8a02-135">NOTES</span></span>

## <span data-ttu-id="d8a02-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8a02-136">RELATED LINKS</span></span>

