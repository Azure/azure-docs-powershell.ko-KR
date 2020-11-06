---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef5db457846f6fdf0dcd0a0a32b37cab96a557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523980"
---
# <span data-ttu-id="80352-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="80352-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="80352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80352-102">SYNOPSIS</span></span>
<span data-ttu-id="80352-103">모든 논리 서브넷의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="80352-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="80352-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80352-104">SYNTAX</span></span>

### <span data-ttu-id="80352-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="80352-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="80352-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="80352-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="80352-107">리소스</span><span class="sxs-lookup"><span data-stu-id="80352-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="80352-108">설명은</span><span class="sxs-lookup"><span data-stu-id="80352-108">DESCRIPTION</span></span>
<span data-ttu-id="80352-109">모든 논리 서브넷의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="80352-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="80352-110">예제의</span><span class="sxs-lookup"><span data-stu-id="80352-110">EXAMPLES</span></span>

### <span data-ttu-id="80352-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="80352-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="80352-112">지정 된 논리 네트워크 및 위치에 대 한 모든 논리 서브넷 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="80352-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="80352-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="80352-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="80352-114">지정 된 논리 네트워크 및 이름에 따라 위치에 대 한 특정 논리 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="80352-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="80352-115">변수</span><span class="sxs-lookup"><span data-stu-id="80352-115">PARAMETERS</span></span>

### <span data-ttu-id="80352-116">-필터</span><span class="sxs-lookup"><span data-stu-id="80352-116">-Filter</span></span>
<span data-ttu-id="80352-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="80352-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="80352-118">-위치</span><span class="sxs-lookup"><span data-stu-id="80352-118">-Location</span></span>
<span data-ttu-id="80352-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="80352-119">Location of the resource.</span></span>

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

### <span data-ttu-id="80352-120">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="80352-120">-LogicalNetwork</span></span>
<span data-ttu-id="80352-121">논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80352-121">Name of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80352-122">-이름</span><span class="sxs-lookup"><span data-stu-id="80352-122">-Name</span></span>
<span data-ttu-id="80352-123">논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80352-123">Name of the logical subnet.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80352-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80352-124">-ResourceGroupName</span></span>
<span data-ttu-id="80352-125">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="80352-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="80352-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80352-126">-ResourceId</span></span>
<span data-ttu-id="80352-127">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="80352-127">The resource id.</span></span>

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

### <span data-ttu-id="80352-128">-생략</span><span class="sxs-lookup"><span data-stu-id="80352-128">-Skip</span></span>
<span data-ttu-id="80352-129">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="80352-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="80352-130">-위쪽</span><span class="sxs-lookup"><span data-stu-id="80352-130">-Top</span></span>
<span data-ttu-id="80352-131">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="80352-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="80352-132">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80352-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="80352-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80352-133">CommonParameters</span></span>
<span data-ttu-id="80352-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80352-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80352-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80352-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80352-136">입력</span><span class="sxs-lookup"><span data-stu-id="80352-136">INPUTS</span></span>

## <span data-ttu-id="80352-137">출력</span><span class="sxs-lookup"><span data-stu-id="80352-137">OUTPUTS</span></span>

### <span data-ttu-id="80352-138">Microsoft AzureStack. 관리. a. 관리자. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="80352-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="80352-139">상속자</span><span class="sxs-lookup"><span data-stu-id="80352-139">NOTES</span></span>

## <span data-ttu-id="80352-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80352-140">RELATED LINKS</span></span>

