---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a20f0fbc5b059e878f0062569ffba2c16794204
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875023"
---
# <span data-ttu-id="8ef53-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="8ef53-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="8ef53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ef53-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef53-103">위치에 있는 모든 인프라 역할의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="8ef53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ef53-104">SYNTAX</span></span>

### <span data-ttu-id="8ef53-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8ef53-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8ef53-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="8ef53-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ef53-107">리소스</span><span class="sxs-lookup"><span data-stu-id="8ef53-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8ef53-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8ef53-108">DESCRIPTION</span></span>
<span data-ttu-id="8ef53-109">위치에 있는 모든 인프라 역할의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="8ef53-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8ef53-110">EXAMPLES</span></span>

### <span data-ttu-id="8ef53-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ef53-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="8ef53-112">모든 인프라 역할의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="8ef53-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8ef53-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="8ef53-114">이름에 따라 인프라 역할을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="8ef53-115">변수</span><span class="sxs-lookup"><span data-stu-id="8ef53-115">PARAMETERS</span></span>

### <span data-ttu-id="8ef53-116">-이름</span><span class="sxs-lookup"><span data-stu-id="8ef53-116">-Name</span></span>
<span data-ttu-id="8ef53-117">인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-117">Infrastructure role name.</span></span>

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

### <span data-ttu-id="8ef53-118">-위치</span><span class="sxs-lookup"><span data-stu-id="8ef53-118">-Location</span></span>
<span data-ttu-id="8ef53-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-119">Location of the resource.</span></span>

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

### <span data-ttu-id="8ef53-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ef53-120">-ResourceGroupName</span></span>
<span data-ttu-id="8ef53-121">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="8ef53-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ef53-122">-ResourceId</span></span>
<span data-ttu-id="8ef53-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-123">The resource id.</span></span>

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

### <span data-ttu-id="8ef53-124">-필터</span><span class="sxs-lookup"><span data-stu-id="8ef53-124">-Filter</span></span>
<span data-ttu-id="8ef53-125">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="8ef53-126">-생략</span><span class="sxs-lookup"><span data-stu-id="8ef53-126">-Skip</span></span>
<span data-ttu-id="8ef53-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8ef53-128">-위쪽</span><span class="sxs-lookup"><span data-stu-id="8ef53-128">-Top</span></span>
<span data-ttu-id="8ef53-129">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8ef53-130">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8ef53-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef53-131">CommonParameters</span></span>
<span data-ttu-id="8ef53-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef53-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef53-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ef53-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef53-134">입력</span><span class="sxs-lookup"><span data-stu-id="8ef53-134">INPUTS</span></span>

## <span data-ttu-id="8ef53-135">출력</span><span class="sxs-lookup"><span data-stu-id="8ef53-135">OUTPUTS</span></span>

### <span data-ttu-id="8ef53-136">InfraRole. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="8ef53-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="8ef53-137">상속자</span><span class="sxs-lookup"><span data-stu-id="8ef53-137">NOTES</span></span>

## <span data-ttu-id="8ef53-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ef53-138">RELATED LINKS</span></span>
