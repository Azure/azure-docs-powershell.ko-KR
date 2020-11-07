---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874944"
---
# <span data-ttu-id="4663f-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="4663f-101">New-PlanObject</span></span>

## <span data-ttu-id="4663f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4663f-102">SYNOPSIS</span></span>
<span data-ttu-id="4663f-103">계획은 테 넌 트를 제공 하는 할당량 및 용량 패키지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="4663f-104">테 넌 트가 기본 클라우드 서비스에 대 한 액세스를 업그레이드 하는 제안을 통해이 요금제를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="4663f-105">구문과</span><span class="sxs-lookup"><span data-stu-id="4663f-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="4663f-106">설명은</span><span class="sxs-lookup"><span data-stu-id="4663f-106">DESCRIPTION</span></span>
<span data-ttu-id="4663f-107">계획은 테 넌 트를 제공 하는 할당량 및 용량 패키지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="4663f-108">테 넌 트가 기본 클라우드 서비스에 대 한 액세스를 업그레이드 하는 제안을 통해이 요금제를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="4663f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4663f-109">EXAMPLES</span></span>

### <span data-ttu-id="4663f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4663f-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4663f-111">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="4663f-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="4663f-112">변수</span><span class="sxs-lookup"><span data-stu-id="4663f-112">PARAMETERS</span></span>

### <span data-ttu-id="4663f-113">-설명</span><span class="sxs-lookup"><span data-stu-id="4663f-113">-Description</span></span>
<span data-ttu-id="4663f-114">계획에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-114">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4663f-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4663f-115">-DisplayName</span></span>
<span data-ttu-id="4663f-116">표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-116">Display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4663f-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="4663f-117">-ExternalReferenceId</span></span>
<span data-ttu-id="4663f-118">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-118">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4663f-119">-Id</span><span class="sxs-lookup"><span data-stu-id="4663f-119">-Id</span></span>
<span data-ttu-id="4663f-120">리소스의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-120">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4663f-121">-위치</span><span class="sxs-lookup"><span data-stu-id="4663f-121">-Location</span></span>
<span data-ttu-id="4663f-122">리소스가 위치 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-122">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4663f-123">-이름</span><span class="sxs-lookup"><span data-stu-id="4663f-123">-Name</span></span>
<span data-ttu-id="4663f-124">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-124">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4663f-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="4663f-125">-QuotaIds</span></span>
<span data-ttu-id="4663f-126">계획 아래에 할당량 식별자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-126">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4663f-127">-(\) Uid</span><span class="sxs-lookup"><span data-stu-id="4663f-127">-SkuIds</span></span>
<span data-ttu-id="4663f-128">SKU 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-128">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4663f-129">-구독 카운트</span><span class="sxs-lookup"><span data-stu-id="4663f-129">-SubscriptionCount</span></span>
<span data-ttu-id="4663f-130">구독 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-130">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4663f-131">태그</span><span class="sxs-lookup"><span data-stu-id="4663f-131">-Tags</span></span>
<span data-ttu-id="4663f-132">키-값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-132">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4663f-133">-Type</span><span class="sxs-lookup"><span data-stu-id="4663f-133">-Type</span></span>
<span data-ttu-id="4663f-134">리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-134">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4663f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4663f-135">CommonParameters</span></span>
<span data-ttu-id="4663f-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4663f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4663f-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4663f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4663f-138">입력</span><span class="sxs-lookup"><span data-stu-id="4663f-138">INPUTS</span></span>

## <span data-ttu-id="4663f-139">출력</span><span class="sxs-lookup"><span data-stu-id="4663f-139">OUTPUTS</span></span>

## <span data-ttu-id="4663f-140">상속자</span><span class="sxs-lookup"><span data-stu-id="4663f-140">NOTES</span></span>

## <span data-ttu-id="4663f-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4663f-141">RELATED LINKS</span></span>

