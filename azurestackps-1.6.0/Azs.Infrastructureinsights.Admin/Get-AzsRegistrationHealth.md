---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d73e2db2f09ba504e9c6adbf15a0bbc2629452ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523599"
---
# <span data-ttu-id="e3c32-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="e3c32-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="e3c32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3c32-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c32-103">서비스 아래에 각 리소스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="e3c32-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3c32-104">SYNTAX</span></span>

### <span data-ttu-id="e3c32-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e3c32-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e3c32-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="e3c32-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="e3c32-107">리소스</span><span class="sxs-lookup"><span data-stu-id="e3c32-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="e3c32-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e3c32-108">DESCRIPTION</span></span>
<span data-ttu-id="e3c32-109">서비스 아래에 각 리소스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="e3c32-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e3c32-110">EXAMPLES</span></span>

### <span data-ttu-id="e3c32-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e3c32-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="e3c32-112">서비스 아래에 각 리소스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="e3c32-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e3c32-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="e3c32-114">관리자의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="e3c32-115">변수</span><span class="sxs-lookup"><span data-stu-id="e3c32-115">PARAMETERS</span></span>

### <span data-ttu-id="e3c32-116">-필터</span><span class="sxs-lookup"><span data-stu-id="e3c32-116">-Filter</span></span>
<span data-ttu-id="e3c32-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e3c32-118">-위치</span><span class="sxs-lookup"><span data-stu-id="e3c32-118">-Location</span></span>
<span data-ttu-id="e3c32-119">지역 이름</span><span class="sxs-lookup"><span data-stu-id="e3c32-119">Name of the region</span></span>

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

### <span data-ttu-id="e3c32-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e3c32-120">-Name</span></span>
<span data-ttu-id="e3c32-121">리소스 등록 id에 해당 하는 상태 개체의 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-121">The resource name of the health object which corresponds to the resource registration id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c32-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c32-122">-ResourceGroupName</span></span>
<span data-ttu-id="e3c32-123">리소스가 있는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="e3c32-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3c32-124">-ResourceId</span></span>
<span data-ttu-id="e3c32-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-125">The resource id.</span></span>

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

### <span data-ttu-id="e3c32-126">-ServiceRegistrationName</span><span class="sxs-lookup"><span data-stu-id="e3c32-126">-ServiceRegistrationName</span></span>
<span data-ttu-id="e3c32-127">서비스 등록 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-127">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ServiceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c32-128">-생략</span><span class="sxs-lookup"><span data-stu-id="e3c32-128">-Skip</span></span>
<span data-ttu-id="e3c32-129">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e3c32-130">-위쪽</span><span class="sxs-lookup"><span data-stu-id="e3c32-130">-Top</span></span>
<span data-ttu-id="e3c32-131">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e3c32-132">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e3c32-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c32-133">CommonParameters</span></span>
<span data-ttu-id="e3c32-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c32-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c32-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3c32-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c32-136">입력</span><span class="sxs-lookup"><span data-stu-id="e3c32-136">INPUTS</span></span>

## <span data-ttu-id="e3c32-137">출력</span><span class="sxs-lookup"><span data-stu-id="e3c32-137">OUTPUTS</span></span>

### <span data-ttu-id="e3c32-138">InfrastructureInsights의. m a 관리/체력</span><span class="sxs-lookup"><span data-stu-id="e3c32-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="e3c32-139">상속자</span><span class="sxs-lookup"><span data-stu-id="e3c32-139">NOTES</span></span>

## <span data-ttu-id="e3c32-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3c32-140">RELATED LINKS</span></span>

