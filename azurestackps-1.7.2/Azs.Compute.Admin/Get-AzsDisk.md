---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4c464d2d0e822b745acc2a7c6daecf329449105
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873965"
---
# <span data-ttu-id="45276-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="45276-101">Get-AzsDisk</span></span>

## <span data-ttu-id="45276-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45276-102">SYNOPSIS</span></span>
<span data-ttu-id="45276-103">지정 된 공유에서 마이그레이션될 수 있는 관리 디스크의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="45276-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="45276-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45276-104">SYNTAX</span></span>

### <span data-ttu-id="45276-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="45276-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="45276-106">리소스</span><span class="sxs-lookup"><span data-stu-id="45276-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="45276-107">가져오기</span><span class="sxs-lookup"><span data-stu-id="45276-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="45276-108">설명은</span><span class="sxs-lookup"><span data-stu-id="45276-108">DESCRIPTION</span></span>
<span data-ttu-id="45276-109">디스크 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="45276-109">Returns a list of disks.</span></span>

## <span data-ttu-id="45276-110">예제의</span><span class="sxs-lookup"><span data-stu-id="45276-110">EXAMPLES</span></span>

### <span data-ttu-id="45276-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="45276-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="45276-112">로컬 위치에 있는 관리 디스크의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="45276-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="45276-113">기본적으로 첫 번째 100 디스크를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="45276-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="45276-114">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="45276-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="45276-115">특정 관리 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45276-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="45276-116">변수</span><span class="sxs-lookup"><span data-stu-id="45276-116">PARAMETERS</span></span>

### <span data-ttu-id="45276-117">-카운트</span><span class="sxs-lookup"><span data-stu-id="45276-117">-Count</span></span>
<span data-ttu-id="45276-118">반환할 최대 디스크 수입니다.</span><span class="sxs-lookup"><span data-stu-id="45276-118">The maximum number of disks to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45276-119">-위치</span><span class="sxs-lookup"><span data-stu-id="45276-119">-Location</span></span>
<span data-ttu-id="45276-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="45276-120">Location of the resource.</span></span>

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

### <span data-ttu-id="45276-121">-이름</span><span class="sxs-lookup"><span data-stu-id="45276-121">-Name</span></span>
<span data-ttu-id="45276-122">Id 인 디스크 guid입니다.</span><span class="sxs-lookup"><span data-stu-id="45276-122">The disk guid as identity.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45276-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45276-123">-ResourceId</span></span>
<span data-ttu-id="45276-124">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="45276-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45276-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="45276-125">-SharePath</span></span>
<span data-ttu-id="45276-126">리소스가 속한 원본 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="45276-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="45276-127">-시작</span><span class="sxs-lookup"><span data-stu-id="45276-127">-Start</span></span>
<span data-ttu-id="45276-128">Query의 디스크 시작 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="45276-128">The start index of disks in query.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45276-129">-상태</span><span class="sxs-lookup"><span data-stu-id="45276-129">-Status</span></span>
<span data-ttu-id="45276-130">디스크 상태의 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="45276-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="45276-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45276-131">-UserSubscriptionId</span></span>
<span data-ttu-id="45276-132">리소스가 속한 테 넌 트 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="45276-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="45276-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45276-133">CommonParameters</span></span>
<span data-ttu-id="45276-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45276-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45276-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45276-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45276-136">입력</span><span class="sxs-lookup"><span data-stu-id="45276-136">INPUTS</span></span>

## <span data-ttu-id="45276-137">출력</span><span class="sxs-lookup"><span data-stu-id="45276-137">OUTPUTS</span></span>

### <span data-ttu-id="45276-138">Microsoft AzureStack. 관리자. m a. 관리.</span><span class="sxs-lookup"><span data-stu-id="45276-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="45276-139">상속자</span><span class="sxs-lookup"><span data-stu-id="45276-139">NOTES</span></span>

## <span data-ttu-id="45276-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45276-140">RELATED LINKS</span></span>

