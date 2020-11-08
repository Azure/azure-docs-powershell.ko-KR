---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046646"
---
# <span data-ttu-id="ab692-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="ab692-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="ab692-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab692-102">SYNOPSIS</span></span>
<span data-ttu-id="ab692-103">모든 패브릭 위치의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab692-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="ab692-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab692-104">SYNTAX</span></span>

### <span data-ttu-id="ab692-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ab692-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab692-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="ab692-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ab692-107">리소스</span><span class="sxs-lookup"><span data-stu-id="ab692-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ab692-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ab692-108">DESCRIPTION</span></span>
<span data-ttu-id="ab692-109">모든 패브릭 위치의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab692-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="ab692-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ab692-110">EXAMPLES</span></span>

### <span data-ttu-id="ab692-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab692-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="ab692-112">모든 패브릭 위치 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab692-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="ab692-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="ab692-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="ab692-114">이름을 기준으로 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab692-114">Return a location based on the name.</span></span>

## <span data-ttu-id="ab692-115">변수</span><span class="sxs-lookup"><span data-stu-id="ab692-115">PARAMETERS</span></span>

### <span data-ttu-id="ab692-116">-위치</span><span class="sxs-lookup"><span data-stu-id="ab692-116">-Location</span></span>
<span data-ttu-id="ab692-117">패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="ab692-117">Fabric location.</span></span>

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

### <span data-ttu-id="ab692-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab692-118">-ResourceGroupName</span></span>
<span data-ttu-id="ab692-119">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="ab692-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ab692-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab692-120">-ResourceId</span></span>
<span data-ttu-id="ab692-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ab692-121">The resource id.</span></span>

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

### <span data-ttu-id="ab692-122">-필터</span><span class="sxs-lookup"><span data-stu-id="ab692-122">-Filter</span></span>
<span data-ttu-id="ab692-123">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab692-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="ab692-124">-생략</span><span class="sxs-lookup"><span data-stu-id="ab692-124">-Skip</span></span>
<span data-ttu-id="ab692-125">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="ab692-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ab692-126">-위쪽</span><span class="sxs-lookup"><span data-stu-id="ab692-126">-Top</span></span>
<span data-ttu-id="ab692-127">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab692-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ab692-128">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab692-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ab692-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab692-129">CommonParameters</span></span>
<span data-ttu-id="ab692-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab692-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab692-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab692-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab692-132">입력</span><span class="sxs-lookup"><span data-stu-id="ab692-132">INPUTS</span></span>

## <span data-ttu-id="ab692-133">출력</span><span class="sxs-lookup"><span data-stu-id="ab692-133">OUTPUTS</span></span>

### <span data-ttu-id="ab692-134">FabricLocation. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="ab692-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="ab692-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ab692-135">NOTES</span></span>

## <span data-ttu-id="ab692-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab692-136">RELATED LINKS</span></span>
