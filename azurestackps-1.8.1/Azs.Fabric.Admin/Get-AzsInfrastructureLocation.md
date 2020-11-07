---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875022"
---
# <span data-ttu-id="95413-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="95413-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="95413-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95413-102">SYNOPSIS</span></span>
<span data-ttu-id="95413-103">모든 패브릭 위치의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="95413-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="95413-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95413-104">SYNTAX</span></span>

### <span data-ttu-id="95413-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="95413-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="95413-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="95413-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="95413-107">리소스</span><span class="sxs-lookup"><span data-stu-id="95413-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="95413-108">설명은</span><span class="sxs-lookup"><span data-stu-id="95413-108">DESCRIPTION</span></span>
<span data-ttu-id="95413-109">모든 패브릭 위치의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="95413-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="95413-110">예제의</span><span class="sxs-lookup"><span data-stu-id="95413-110">EXAMPLES</span></span>

### <span data-ttu-id="95413-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="95413-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="95413-112">모든 패브릭 위치 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="95413-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="95413-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="95413-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="95413-114">이름을 기준으로 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="95413-114">Return a location based on the name.</span></span>

## <span data-ttu-id="95413-115">변수</span><span class="sxs-lookup"><span data-stu-id="95413-115">PARAMETERS</span></span>

### <span data-ttu-id="95413-116">-위치</span><span class="sxs-lookup"><span data-stu-id="95413-116">-Location</span></span>
<span data-ttu-id="95413-117">패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="95413-117">Fabric location.</span></span>

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

### <span data-ttu-id="95413-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95413-118">-ResourceGroupName</span></span>
<span data-ttu-id="95413-119">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="95413-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="95413-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95413-120">-ResourceId</span></span>
<span data-ttu-id="95413-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="95413-121">The resource id.</span></span>

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

### <span data-ttu-id="95413-122">-필터</span><span class="sxs-lookup"><span data-stu-id="95413-122">-Filter</span></span>
<span data-ttu-id="95413-123">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="95413-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="95413-124">-생략</span><span class="sxs-lookup"><span data-stu-id="95413-124">-Skip</span></span>
<span data-ttu-id="95413-125">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="95413-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="95413-126">-위쪽</span><span class="sxs-lookup"><span data-stu-id="95413-126">-Top</span></span>
<span data-ttu-id="95413-127">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="95413-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="95413-128">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95413-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="95413-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95413-129">CommonParameters</span></span>
<span data-ttu-id="95413-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95413-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95413-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95413-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95413-132">입력</span><span class="sxs-lookup"><span data-stu-id="95413-132">INPUTS</span></span>

## <span data-ttu-id="95413-133">출력</span><span class="sxs-lookup"><span data-stu-id="95413-133">OUTPUTS</span></span>

### <span data-ttu-id="95413-134">FabricLocation. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="95413-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="95413-135">상속자</span><span class="sxs-lookup"><span data-stu-id="95413-135">NOTES</span></span>

## <span data-ttu-id="95413-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95413-136">RELATED LINKS</span></span>
