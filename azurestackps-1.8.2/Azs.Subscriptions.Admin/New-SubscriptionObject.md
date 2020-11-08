---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047163"
---
# <span data-ttu-id="5cc00-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="5cc00-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="5cc00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cc00-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc00-103">지원 되는 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-103">List of supported operations.</span></span>

## <span data-ttu-id="5cc00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5cc00-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="5cc00-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5cc00-105">DESCRIPTION</span></span>
<span data-ttu-id="5cc00-106">지원 되는 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-106">List of supported operations.</span></span>

## <span data-ttu-id="5cc00-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5cc00-107">EXAMPLES</span></span>

### <span data-ttu-id="5cc00-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5cc00-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="5cc00-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="5cc00-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="5cc00-110">변수</span><span class="sxs-lookup"><span data-stu-id="5cc00-110">PARAMETERS</span></span>

### <span data-ttu-id="5cc00-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cc00-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="5cc00-112">부모 DelegatedProvider 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc00-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5cc00-113">-DisplayName</span></span>
<span data-ttu-id="5cc00-114">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-114">Subscription name.</span></span>

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

### <span data-ttu-id="5cc00-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="5cc00-115">-ExternalReferenceId</span></span>
<span data-ttu-id="5cc00-116">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-116">External reference identifier.</span></span>

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

### <span data-ttu-id="5cc00-117">-Id</span><span class="sxs-lookup"><span data-stu-id="5cc00-117">-Id</span></span>
<span data-ttu-id="5cc00-118">정규화 된 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-118">Fully qualified identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc00-119">-이름</span><span class="sxs-lookup"><span data-stu-id="5cc00-119">-Name</span></span>
<span data-ttu-id="5cc00-120">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-120">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc00-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="5cc00-121">-OfferId</span></span>
<span data-ttu-id="5cc00-122">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-122">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc00-123">-소유자</span><span class="sxs-lookup"><span data-stu-id="5cc00-123">-Owner</span></span>
<span data-ttu-id="5cc00-124">구독 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-124">Subscription owner.</span></span>

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

### <span data-ttu-id="5cc00-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="5cc00-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="5cc00-126">라우팅 리소스 관리자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-126">Routing resource manager type.</span></span>

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

### <span data-ttu-id="5cc00-127">-상태</span><span class="sxs-lookup"><span data-stu-id="5cc00-127">-State</span></span>
<span data-ttu-id="5cc00-128">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-128">Subscription state.</span></span>

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

### <span data-ttu-id="5cc00-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cc00-129">-SubscriptionId</span></span>
<span data-ttu-id="5cc00-130">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="5cc00-131">-TenantId</span><span class="sxs-lookup"><span data-stu-id="5cc00-131">-TenantId</span></span>
<span data-ttu-id="5cc00-132">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="5cc00-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc00-133">CommonParameters</span></span>
<span data-ttu-id="5cc00-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cc00-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc00-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cc00-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc00-136">입력</span><span class="sxs-lookup"><span data-stu-id="5cc00-136">INPUTS</span></span>

## <span data-ttu-id="5cc00-137">출력</span><span class="sxs-lookup"><span data-stu-id="5cc00-137">OUTPUTS</span></span>

## <span data-ttu-id="5cc00-138">상속자</span><span class="sxs-lookup"><span data-stu-id="5cc00-138">NOTES</span></span>

## <span data-ttu-id="5cc00-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5cc00-139">RELATED LINKS</span></span>

