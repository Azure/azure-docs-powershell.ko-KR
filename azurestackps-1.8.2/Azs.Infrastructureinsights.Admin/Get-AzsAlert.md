---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3a64a045d988d59c2b1aefa650aa695ba09486f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046916"
---
# <span data-ttu-id="98af9-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="98af9-101">Get-AzsAlert</span></span>

## <span data-ttu-id="98af9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98af9-102">SYNOPSIS</span></span>
<span data-ttu-id="98af9-103">지정 된 위치에 있는 모든 알림 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="98af9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="98af9-104">SYNTAX</span></span>

### <span data-ttu-id="98af9-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="98af9-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="98af9-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="98af9-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="98af9-107">리소스</span><span class="sxs-lookup"><span data-stu-id="98af9-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="98af9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="98af9-108">DESCRIPTION</span></span>
<span data-ttu-id="98af9-109">지정 된 위치에 있는 모든 알림 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="98af9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="98af9-110">EXAMPLES</span></span>

### <span data-ttu-id="98af9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="98af9-111">EXAMPLE 1</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="98af9-112">이름으로 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-112">Get an alert by Name.</span></span>

### <span data-ttu-id="98af9-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="98af9-113">EXAMPLE 2</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="98af9-114">모든 활성 알림을 받고 해당 오류 및 직함을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="98af9-115">변수</span><span class="sxs-lookup"><span data-stu-id="98af9-115">PARAMETERS</span></span>

### <span data-ttu-id="98af9-116">-이름</span><span class="sxs-lookup"><span data-stu-id="98af9-116">-Name</span></span>
<span data-ttu-id="98af9-117">경고 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-117">The alert identifier.</span></span>

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

### <span data-ttu-id="98af9-118">-위치</span><span class="sxs-lookup"><span data-stu-id="98af9-118">-Location</span></span>
<span data-ttu-id="98af9-119">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-119">Name of the location.</span></span>

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

### <span data-ttu-id="98af9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98af9-120">-ResourceGroupName</span></span>
<span data-ttu-id="98af9-121">경고의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="98af9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98af9-122">-ResourceId</span></span>
<span data-ttu-id="98af9-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-123">The resource id.</span></span>

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

### <span data-ttu-id="98af9-124">-필터</span><span class="sxs-lookup"><span data-stu-id="98af9-124">-Filter</span></span>
<span data-ttu-id="98af9-125">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="98af9-126">-위쪽</span><span class="sxs-lookup"><span data-stu-id="98af9-126">-Top</span></span>
<span data-ttu-id="98af9-127">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="98af9-128">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="98af9-129">-생략</span><span class="sxs-lookup"><span data-stu-id="98af9-129">-Skip</span></span>
<span data-ttu-id="98af9-130">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-130">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="98af9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98af9-131">CommonParameters</span></span>
<span data-ttu-id="98af9-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="98af9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98af9-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98af9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98af9-134">입력</span><span class="sxs-lookup"><span data-stu-id="98af9-134">INPUTS</span></span>

## <span data-ttu-id="98af9-135">출력</span><span class="sxs-lookup"><span data-stu-id="98af9-135">OUTPUTS</span></span>

### <span data-ttu-id="98af9-136">InfrastructureInsights. Alert (관리자 용)</span><span class="sxs-lookup"><span data-stu-id="98af9-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="98af9-137">상속자</span><span class="sxs-lookup"><span data-stu-id="98af9-137">NOTES</span></span>

## <span data-ttu-id="98af9-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98af9-138">RELATED LINKS</span></span>
