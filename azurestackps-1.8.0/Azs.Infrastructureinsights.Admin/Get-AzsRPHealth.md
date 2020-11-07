---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 752bd7f183bf5a5bdad7950e6567024cbe5b8dec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874739"
---
# <span data-ttu-id="c37c0-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="c37c0-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="c37c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c37c0-102">SYNOPSIS</span></span>
<span data-ttu-id="c37c0-103">각 서비스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="c37c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c37c0-104">SYNTAX</span></span>

### <span data-ttu-id="c37c0-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c37c0-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c37c0-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="c37c0-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c37c0-107">리소스</span><span class="sxs-lookup"><span data-stu-id="c37c0-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c37c0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c37c0-108">DESCRIPTION</span></span>
<span data-ttu-id="c37c0-109">각 서비스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-109">Returns a list of each service's health.</span></span> <span data-ttu-id="c37c0-110">AlertSummary 속성에는 경고/오류 개수에 대 한 세부 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="c37c0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c37c0-111">EXAMPLES</span></span>

### <span data-ttu-id="c37c0-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c37c0-112">EXAMPLE 1</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="c37c0-113">각 서비스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="c37c0-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c37c0-114">EXAMPLE 2</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="c37c0-115">서비스의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-115">Returns a service's health.</span></span>

## <span data-ttu-id="c37c0-116">변수</span><span class="sxs-lookup"><span data-stu-id="c37c0-116">PARAMETERS</span></span>

### <span data-ttu-id="c37c0-117">-이름</span><span class="sxs-lookup"><span data-stu-id="c37c0-117">-Name</span></span>
<span data-ttu-id="c37c0-118">서비스 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-118">Service Health name.</span></span>

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

### <span data-ttu-id="c37c0-119">-위치</span><span class="sxs-lookup"><span data-stu-id="c37c0-119">-Location</span></span>
<span data-ttu-id="c37c0-120">지역 이름</span><span class="sxs-lookup"><span data-stu-id="c37c0-120">Name of the region</span></span>

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

### <span data-ttu-id="c37c0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c37c0-121">-ResourceGroupName</span></span>
<span data-ttu-id="c37c0-122">리소스 그룹의 이름, 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-122">Name of the resource group, optional.</span></span>

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

### <span data-ttu-id="c37c0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c37c0-123">-ResourceId</span></span>
<span data-ttu-id="c37c0-124">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-124">The resource id.</span></span>

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

### <span data-ttu-id="c37c0-125">-필터</span><span class="sxs-lookup"><span data-stu-id="c37c0-125">-Filter</span></span>
<span data-ttu-id="c37c0-126">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="c37c0-127">-생략</span><span class="sxs-lookup"><span data-stu-id="c37c0-127">-Skip</span></span>
<span data-ttu-id="c37c0-128">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c37c0-129">-위쪽</span><span class="sxs-lookup"><span data-stu-id="c37c0-129">-Top</span></span>
<span data-ttu-id="c37c0-130">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c37c0-131">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c37c0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37c0-132">CommonParameters</span></span>
<span data-ttu-id="c37c0-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c37c0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37c0-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c37c0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37c0-135">입력</span><span class="sxs-lookup"><span data-stu-id="c37c0-135">INPUTS</span></span>

## <span data-ttu-id="c37c0-136">출력</span><span class="sxs-lookup"><span data-stu-id="c37c0-136">OUTPUTS</span></span>

### <span data-ttu-id="c37c0-137">InfrastructureInsights. w i m. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="c37c0-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="c37c0-138">상속자</span><span class="sxs-lookup"><span data-stu-id="c37c0-138">NOTES</span></span>

## <span data-ttu-id="c37c0-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c37c0-139">RELATED LINKS</span></span>
