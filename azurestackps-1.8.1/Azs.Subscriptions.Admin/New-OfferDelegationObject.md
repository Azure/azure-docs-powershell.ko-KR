---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874946"
---
# <span data-ttu-id="286be-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="286be-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="286be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286be-102">SYNOPSIS</span></span>
<span data-ttu-id="286be-103">위임을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="286be-103">Offer delegation.</span></span>

## <span data-ttu-id="286be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="286be-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="286be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="286be-105">DESCRIPTION</span></span>
<span data-ttu-id="286be-106">위임을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="286be-106">Offer delegation.</span></span>

## <span data-ttu-id="286be-107">예제의</span><span class="sxs-lookup"><span data-stu-id="286be-107">EXAMPLES</span></span>

### <span data-ttu-id="286be-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="286be-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="286be-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="286be-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="286be-110">변수</span><span class="sxs-lookup"><span data-stu-id="286be-110">PARAMETERS</span></span>

### <span data-ttu-id="286be-111">-Id</span><span class="sxs-lookup"><span data-stu-id="286be-111">-Id</span></span>
<span data-ttu-id="286be-112">리소스의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="286be-112">URI of the resource.</span></span>

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

### <span data-ttu-id="286be-113">-위치</span><span class="sxs-lookup"><span data-stu-id="286be-113">-Location</span></span>
<span data-ttu-id="286be-114">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="286be-114">Location of the resource.</span></span>

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

### <span data-ttu-id="286be-115">-이름</span><span class="sxs-lookup"><span data-stu-id="286be-115">-Name</span></span>
<span data-ttu-id="286be-116">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="286be-116">Name of the resource.</span></span>

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

### <span data-ttu-id="286be-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="286be-117">-SubscriptionId</span></span>
<span data-ttu-id="286be-118">위임 된 제안을 받는 구독의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="286be-118">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="286be-119">태그</span><span class="sxs-lookup"><span data-stu-id="286be-119">-Tags</span></span>
<span data-ttu-id="286be-120">키-값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="286be-120">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286be-121">-Type</span><span class="sxs-lookup"><span data-stu-id="286be-121">-Type</span></span>
<span data-ttu-id="286be-122">리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="286be-122">Type of resource.</span></span>

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

### <span data-ttu-id="286be-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286be-123">CommonParameters</span></span>
<span data-ttu-id="286be-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="286be-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286be-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="286be-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286be-126">입력</span><span class="sxs-lookup"><span data-stu-id="286be-126">INPUTS</span></span>

## <span data-ttu-id="286be-127">출력</span><span class="sxs-lookup"><span data-stu-id="286be-127">OUTPUTS</span></span>

## <span data-ttu-id="286be-128">상속자</span><span class="sxs-lookup"><span data-stu-id="286be-128">NOTES</span></span>

## <span data-ttu-id="286be-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="286be-129">RELATED LINKS</span></span>

