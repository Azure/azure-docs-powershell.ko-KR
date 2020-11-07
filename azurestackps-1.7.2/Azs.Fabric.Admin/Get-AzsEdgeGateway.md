---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a81fcf688e1c269aabd64250e9b0694730edc8f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874404"
---
# <span data-ttu-id="9591e-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="9591e-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="9591e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9591e-102">SYNOPSIS</span></span>
<span data-ttu-id="9591e-103">특정 위치에 있는 모든 edge 게이트웨이의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="9591e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9591e-104">SYNTAX</span></span>

### <span data-ttu-id="9591e-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9591e-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9591e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="9591e-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9591e-107">리소스</span><span class="sxs-lookup"><span data-stu-id="9591e-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9591e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9591e-108">DESCRIPTION</span></span>
<span data-ttu-id="9591e-109">특정 위치에 있는 모든 edge 게이트웨이의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="9591e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9591e-110">EXAMPLES</span></span>

### <span data-ttu-id="9591e-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9591e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="9591e-112">모든 edge 게이트웨이의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="9591e-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9591e-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="9591e-114">특정 edge 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="9591e-115">변수</span><span class="sxs-lookup"><span data-stu-id="9591e-115">PARAMETERS</span></span>

### <span data-ttu-id="9591e-116">-필터</span><span class="sxs-lookup"><span data-stu-id="9591e-116">-Filter</span></span>
<span data-ttu-id="9591e-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="9591e-118">-위치</span><span class="sxs-lookup"><span data-stu-id="9591e-118">-Location</span></span>
<span data-ttu-id="9591e-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-119">Location of the resource.</span></span>

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

### <span data-ttu-id="9591e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="9591e-120">-Name</span></span>
<span data-ttu-id="9591e-121">Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-121">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="9591e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9591e-122">-ResourceGroupName</span></span>
<span data-ttu-id="9591e-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="9591e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9591e-124">-ResourceId</span></span>
<span data-ttu-id="9591e-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-125">The resource id.</span></span>

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

### <span data-ttu-id="9591e-126">-생략</span><span class="sxs-lookup"><span data-stu-id="9591e-126">-Skip</span></span>
<span data-ttu-id="9591e-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9591e-128">-위쪽</span><span class="sxs-lookup"><span data-stu-id="9591e-128">-Top</span></span>
<span data-ttu-id="9591e-129">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9591e-130">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9591e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9591e-131">CommonParameters</span></span>
<span data-ttu-id="9591e-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9591e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9591e-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9591e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9591e-134">입력</span><span class="sxs-lookup"><span data-stu-id="9591e-134">INPUTS</span></span>

## <span data-ttu-id="9591e-135">출력</span><span class="sxs-lookup"><span data-stu-id="9591e-135">OUTPUTS</span></span>

### <span data-ttu-id="9591e-136">EdgeGateway. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="9591e-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="9591e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="9591e-137">NOTES</span></span>

## <span data-ttu-id="9591e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9591e-138">RELATED LINKS</span></span>

