---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fbec7ec2f8bcfc0d7595658f84866cf449d3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874487"
---
# <span data-ttu-id="e24d4-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="e24d4-101">Get-AzsAlert</span></span>

## <span data-ttu-id="e24d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e24d4-102">SYNOPSIS</span></span>
<span data-ttu-id="e24d4-103">지정 된 위치에 있는 모든 알림 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="e24d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e24d4-104">SYNTAX</span></span>

### <span data-ttu-id="e24d4-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e24d4-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e24d4-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="e24d4-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e24d4-107">리소스</span><span class="sxs-lookup"><span data-stu-id="e24d4-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e24d4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e24d4-108">DESCRIPTION</span></span>
<span data-ttu-id="e24d4-109">지정 된 위치에 있는 모든 알림 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="e24d4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e24d4-110">EXAMPLES</span></span>

### <span data-ttu-id="e24d4-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e24d4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="e24d4-112">이름으로 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-112">Get an alert by Name.</span></span>

### <span data-ttu-id="e24d4-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e24d4-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="e24d4-114">모든 활성 알림을 받고 해당 오류 및 직함을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="e24d4-115">변수</span><span class="sxs-lookup"><span data-stu-id="e24d4-115">PARAMETERS</span></span>

### <span data-ttu-id="e24d4-116">-필터</span><span class="sxs-lookup"><span data-stu-id="e24d4-116">-Filter</span></span>
<span data-ttu-id="e24d4-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e24d4-118">-위치</span><span class="sxs-lookup"><span data-stu-id="e24d4-118">-Location</span></span>
<span data-ttu-id="e24d4-119">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-119">Name of the location.</span></span>

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

### <span data-ttu-id="e24d4-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e24d4-120">-Name</span></span>
<span data-ttu-id="e24d4-121">경고 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-121">The alert identifier.</span></span>

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

### <span data-ttu-id="e24d4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e24d4-122">-ResourceGroupName</span></span>
<span data-ttu-id="e24d4-123">리소스가 있는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="e24d4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e24d4-124">-ResourceId</span></span>
<span data-ttu-id="e24d4-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-125">The resource id.</span></span>

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

### <span data-ttu-id="e24d4-126">-생략</span><span class="sxs-lookup"><span data-stu-id="e24d4-126">-Skip</span></span>
<span data-ttu-id="e24d4-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e24d4-128">-위쪽</span><span class="sxs-lookup"><span data-stu-id="e24d4-128">-Top</span></span>
<span data-ttu-id="e24d4-129">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e24d4-130">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e24d4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24d4-131">CommonParameters</span></span>
<span data-ttu-id="e24d4-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24d4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24d4-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e24d4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24d4-134">입력</span><span class="sxs-lookup"><span data-stu-id="e24d4-134">INPUTS</span></span>

## <span data-ttu-id="e24d4-135">출력</span><span class="sxs-lookup"><span data-stu-id="e24d4-135">OUTPUTS</span></span>

### <span data-ttu-id="e24d4-136">InfrastructureInsights. Alert (관리자 용)</span><span class="sxs-lookup"><span data-stu-id="e24d4-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="e24d4-137">상속자</span><span class="sxs-lookup"><span data-stu-id="e24d4-137">NOTES</span></span>

## <span data-ttu-id="e24d4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e24d4-138">RELATED LINKS</span></span>

