---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 793bf4a4b5b9dfb448c5b2a1baf9d74af592a23e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046647"
---
# <span data-ttu-id="26493-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="26493-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="26493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26493-102">SYNOPSIS</span></span>
<span data-ttu-id="26493-103">특정 위치에 있는 모든 edge 게이트웨이의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26493-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="26493-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26493-104">SYNTAX</span></span>

### <span data-ttu-id="26493-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="26493-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="26493-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="26493-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="26493-107">리소스</span><span class="sxs-lookup"><span data-stu-id="26493-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="26493-108">설명은</span><span class="sxs-lookup"><span data-stu-id="26493-108">DESCRIPTION</span></span>
<span data-ttu-id="26493-109">특정 위치에 있는 모든 edge 게이트웨이의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26493-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="26493-110">예제의</span><span class="sxs-lookup"><span data-stu-id="26493-110">EXAMPLES</span></span>

### <span data-ttu-id="26493-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="26493-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="26493-112">모든 edge 게이트웨이의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26493-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="26493-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="26493-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="26493-114">특정 edge 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26493-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="26493-115">변수</span><span class="sxs-lookup"><span data-stu-id="26493-115">PARAMETERS</span></span>

### <span data-ttu-id="26493-116">-이름</span><span class="sxs-lookup"><span data-stu-id="26493-116">-Name</span></span>
<span data-ttu-id="26493-117">Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26493-117">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="26493-118">-위치</span><span class="sxs-lookup"><span data-stu-id="26493-118">-Location</span></span>
<span data-ttu-id="26493-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="26493-119">Location of the resource.</span></span>

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

### <span data-ttu-id="26493-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26493-120">-ResourceGroupName</span></span>
<span data-ttu-id="26493-121">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="26493-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="26493-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26493-122">-ResourceId</span></span>
<span data-ttu-id="26493-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="26493-123">The resource id.</span></span>

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

### <span data-ttu-id="26493-124">-필터</span><span class="sxs-lookup"><span data-stu-id="26493-124">-Filter</span></span>
<span data-ttu-id="26493-125">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="26493-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="26493-126">-생략</span><span class="sxs-lookup"><span data-stu-id="26493-126">-Skip</span></span>
<span data-ttu-id="26493-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="26493-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="26493-128">-위쪽</span><span class="sxs-lookup"><span data-stu-id="26493-128">-Top</span></span>
<span data-ttu-id="26493-129">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26493-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="26493-130">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26493-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="26493-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26493-131">CommonParameters</span></span>
<span data-ttu-id="26493-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26493-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26493-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26493-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26493-134">입력</span><span class="sxs-lookup"><span data-stu-id="26493-134">INPUTS</span></span>

## <span data-ttu-id="26493-135">출력</span><span class="sxs-lookup"><span data-stu-id="26493-135">OUTPUTS</span></span>

### <span data-ttu-id="26493-136">EdgeGateway. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="26493-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="26493-137">상속자</span><span class="sxs-lookup"><span data-stu-id="26493-137">NOTES</span></span>

## <span data-ttu-id="26493-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26493-138">RELATED LINKS</span></span>
