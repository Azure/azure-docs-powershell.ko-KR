---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3a64a045d988d59c2b1aefa650aa695ba09486f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874748"
---
# <span data-ttu-id="d2eb3-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="d2eb3-101">Get-AzsAlert</span></span>

## <span data-ttu-id="d2eb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="d2eb3-103">지정 된 위치에 있는 모든 알림 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="d2eb3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2eb3-104">SYNTAX</span></span>

### <span data-ttu-id="d2eb3-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d2eb3-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d2eb3-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d2eb3-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d2eb3-107">리소스</span><span class="sxs-lookup"><span data-stu-id="d2eb3-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d2eb3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d2eb3-108">DESCRIPTION</span></span>
<span data-ttu-id="d2eb3-109">지정 된 위치에 있는 모든 알림 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="d2eb3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d2eb3-110">EXAMPLES</span></span>

### <span data-ttu-id="d2eb3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d2eb3-111">EXAMPLE 1</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="d2eb3-112">이름으로 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-112">Get an alert by Name.</span></span>

### <span data-ttu-id="d2eb3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d2eb3-113">EXAMPLE 2</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="d2eb3-114">모든 활성 알림을 받고 해당 오류 및 직함을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="d2eb3-115">변수</span><span class="sxs-lookup"><span data-stu-id="d2eb3-115">PARAMETERS</span></span>

### <span data-ttu-id="d2eb3-116">-이름</span><span class="sxs-lookup"><span data-stu-id="d2eb3-116">-Name</span></span>
<span data-ttu-id="d2eb3-117">경고 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-117">The alert identifier.</span></span>

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

### <span data-ttu-id="d2eb3-118">-위치</span><span class="sxs-lookup"><span data-stu-id="d2eb3-118">-Location</span></span>
<span data-ttu-id="d2eb3-119">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-119">Name of the location.</span></span>

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

### <span data-ttu-id="d2eb3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2eb3-120">-ResourceGroupName</span></span>
<span data-ttu-id="d2eb3-121">경고의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="d2eb3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2eb3-122">-ResourceId</span></span>
<span data-ttu-id="d2eb3-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-123">The resource id.</span></span>

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

### <span data-ttu-id="d2eb3-124">-필터</span><span class="sxs-lookup"><span data-stu-id="d2eb3-124">-Filter</span></span>
<span data-ttu-id="d2eb3-125">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="d2eb3-126">-위쪽</span><span class="sxs-lookup"><span data-stu-id="d2eb3-126">-Top</span></span>
<span data-ttu-id="d2eb3-127">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d2eb3-128">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d2eb3-129">-생략</span><span class="sxs-lookup"><span data-stu-id="d2eb3-129">-Skip</span></span>
<span data-ttu-id="d2eb3-130">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-130">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d2eb3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2eb3-131">CommonParameters</span></span>
<span data-ttu-id="d2eb3-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2eb3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2eb3-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2eb3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2eb3-134">입력</span><span class="sxs-lookup"><span data-stu-id="d2eb3-134">INPUTS</span></span>

## <span data-ttu-id="d2eb3-135">출력</span><span class="sxs-lookup"><span data-stu-id="d2eb3-135">OUTPUTS</span></span>

### <span data-ttu-id="d2eb3-136">InfrastructureInsights. Alert (관리자 용)</span><span class="sxs-lookup"><span data-stu-id="d2eb3-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="d2eb3-137">상속자</span><span class="sxs-lookup"><span data-stu-id="d2eb3-137">NOTES</span></span>

## <span data-ttu-id="d2eb3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2eb3-138">RELATED LINKS</span></span>
