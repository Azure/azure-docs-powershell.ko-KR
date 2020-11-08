---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4285a7423390f5d9b5384faa63f95c4206840d71
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047109"
---
# <span data-ttu-id="d0246-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="d0246-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="d0246-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0246-102">SYNOPSIS</span></span>
<span data-ttu-id="d0246-103">서비스 아래에 각 리소스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="d0246-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0246-104">SYNTAX</span></span>

### <span data-ttu-id="d0246-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d0246-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d0246-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d0246-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> -ResourceRegistrationId <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="d0246-107">리소스</span><span class="sxs-lookup"><span data-stu-id="d0246-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="d0246-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d0246-108">DESCRIPTION</span></span>
<span data-ttu-id="d0246-109">서비스 아래에 각 리소스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="d0246-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d0246-110">EXAMPLES</span></span>

### <span data-ttu-id="d0246-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d0246-111">EXAMPLE 1</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="d0246-112">서비스 아래에 각 리소스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="d0246-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d0246-113">EXAMPLE 2</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationId $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="d0246-114">관리자의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="d0246-115">변수</span><span class="sxs-lookup"><span data-stu-id="d0246-115">PARAMETERS</span></span>

### <span data-ttu-id="d0246-116">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="d0246-116">-ServiceRegistrationId</span></span>
<span data-ttu-id="d0246-117">서비스 등록 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-117">Service registration id.</span></span>

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

### <span data-ttu-id="d0246-118">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="d0246-118">-ResourceRegistrationId</span></span>


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

### <span data-ttu-id="d0246-119">-위치</span><span class="sxs-lookup"><span data-stu-id="d0246-119">-Location</span></span>
<span data-ttu-id="d0246-120">지역 이름</span><span class="sxs-lookup"><span data-stu-id="d0246-120">Name of the region</span></span>

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

### <span data-ttu-id="d0246-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0246-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0246-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="d0246-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0246-123">-ResourceId</span></span>
<span data-ttu-id="d0246-124">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-124">The resource id.</span></span>

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

### <span data-ttu-id="d0246-125">-필터</span><span class="sxs-lookup"><span data-stu-id="d0246-125">-Filter</span></span>
<span data-ttu-id="d0246-126">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-126">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0246-127">-위쪽</span><span class="sxs-lookup"><span data-stu-id="d0246-127">-Top</span></span>
<span data-ttu-id="d0246-128">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d0246-129">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d0246-130">-생략</span><span class="sxs-lookup"><span data-stu-id="d0246-130">-Skip</span></span>
<span data-ttu-id="d0246-131">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d0246-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0246-132">CommonParameters</span></span>
<span data-ttu-id="d0246-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0246-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0246-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0246-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0246-135">입력</span><span class="sxs-lookup"><span data-stu-id="d0246-135">INPUTS</span></span>

## <span data-ttu-id="d0246-136">출력</span><span class="sxs-lookup"><span data-stu-id="d0246-136">OUTPUTS</span></span>

### <span data-ttu-id="d0246-137">InfrastructureInsights의. m a 관리/체력</span><span class="sxs-lookup"><span data-stu-id="d0246-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="d0246-138">상속자</span><span class="sxs-lookup"><span data-stu-id="d0246-138">NOTES</span></span>

## <span data-ttu-id="d0246-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0246-139">RELATED LINKS</span></span>
