---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb535146787c4c33a57ad406f05544f18ba74eb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875007"
---
# <span data-ttu-id="6f65b-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="6f65b-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="6f65b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f65b-102">SYNOPSIS</span></span>
<span data-ttu-id="6f65b-103">모든 논리 서브넷의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="6f65b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f65b-104">SYNTAX</span></span>

### <span data-ttu-id="6f65b-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6f65b-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6f65b-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6f65b-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f65b-107">리소스</span><span class="sxs-lookup"><span data-stu-id="6f65b-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6f65b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6f65b-108">DESCRIPTION</span></span>
<span data-ttu-id="6f65b-109">모든 논리 서브넷의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="6f65b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6f65b-110">EXAMPLES</span></span>

### <span data-ttu-id="6f65b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f65b-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="6f65b-112">지정 된 논리 네트워크 및 위치에 대 한 모든 논리 서브넷 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="6f65b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6f65b-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="6f65b-114">지정 된 논리 네트워크 및 이름에 따라 위치에 대 한 특정 논리 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="6f65b-115">변수</span><span class="sxs-lookup"><span data-stu-id="6f65b-115">PARAMETERS</span></span>

### <span data-ttu-id="6f65b-116">-이름</span><span class="sxs-lookup"><span data-stu-id="6f65b-116">-Name</span></span>
<span data-ttu-id="6f65b-117">논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-117">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="6f65b-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="6f65b-118">-LogicalNetwork</span></span>
<span data-ttu-id="6f65b-119">논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-119">Name of the logical network.</span></span>

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

### <span data-ttu-id="6f65b-120">-위치</span><span class="sxs-lookup"><span data-stu-id="6f65b-120">-Location</span></span>
<span data-ttu-id="6f65b-121">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-121">Location of the resource.</span></span>

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

### <span data-ttu-id="6f65b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f65b-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f65b-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6f65b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f65b-124">-ResourceId</span></span>
<span data-ttu-id="6f65b-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-125">The resource id.</span></span>

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

### <span data-ttu-id="6f65b-126">-필터</span><span class="sxs-lookup"><span data-stu-id="6f65b-126">-Filter</span></span>
<span data-ttu-id="6f65b-127">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="6f65b-128">-생략</span><span class="sxs-lookup"><span data-stu-id="6f65b-128">-Skip</span></span>
<span data-ttu-id="6f65b-129">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6f65b-130">-위쪽</span><span class="sxs-lookup"><span data-stu-id="6f65b-130">-Top</span></span>
<span data-ttu-id="6f65b-131">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6f65b-132">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6f65b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f65b-133">CommonParameters</span></span>
<span data-ttu-id="6f65b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f65b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f65b-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f65b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f65b-136">입력</span><span class="sxs-lookup"><span data-stu-id="6f65b-136">INPUTS</span></span>

## <span data-ttu-id="6f65b-137">출력</span><span class="sxs-lookup"><span data-stu-id="6f65b-137">OUTPUTS</span></span>

### <span data-ttu-id="6f65b-138">Microsoft AzureStack. 관리. a. 관리자. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="6f65b-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="6f65b-139">상속자</span><span class="sxs-lookup"><span data-stu-id="6f65b-139">NOTES</span></span>

## <span data-ttu-id="6f65b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f65b-140">RELATED LINKS</span></span>
