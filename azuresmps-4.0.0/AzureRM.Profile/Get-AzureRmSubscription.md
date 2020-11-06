---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523399"
---
# <span data-ttu-id="8feb3-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="8feb3-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="8feb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8feb3-102">SYNOPSIS</span></span>
<span data-ttu-id="8feb3-103">현재 계정이 액세스할 수 있는 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8feb3-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="8feb3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8feb3-104">SYNTAX</span></span>

### <span data-ttu-id="8feb3-105">ListByIdInTenant (기본값)</span><span class="sxs-lookup"><span data-stu-id="8feb3-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### <span data-ttu-id="8feb3-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="8feb3-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## <span data-ttu-id="8feb3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8feb3-107">DESCRIPTION</span></span>
<span data-ttu-id="8feb3-108">Get-AzureRmSubscription cmdlet은 현재 계정이 액세스할 수 있는 구독에 대 한 구독 ID, 구독 이름 및 홈 테 넌 트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8feb3-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="8feb3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8feb3-109">EXAMPLES</span></span>

### <span data-ttu-id="8feb3-110">예제 1: 모든 테 넌 트의 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="8feb3-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="8feb3-111">이 명령은 현재 계정에 대해 권한이 있는 모든 테 넌 트의 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8feb3-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="8feb3-112">예제 2: 특정 테 넌 트에 대 한 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="8feb3-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="8feb3-113">지정 된 테 넌 트에서 현재 계정에 대해 권한이 있는 모든 구독을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8feb3-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="8feb3-114">예제 3: 현재 테 넌 트의 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="8feb3-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="8feb3-115">이 명령은 현재 테 넌 트에서 현재 사용자에 대해 권한이 부여 된 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8feb3-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="8feb3-116">예제 4: 특정 구독을 사용 하도록 현재 컨텍스트 변경</span><span class="sxs-lookup"><span data-stu-id="8feb3-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="8feb3-117">이 명령은 지정 된 구독을 가져온 다음 현재 컨텍스트를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8feb3-117">This command gets the specified subscription, and then sets the current context to use it.</span></span>
<span data-ttu-id="8feb3-118">이 세션의 모든 후속 cmdlet은 기본적으로 새 구독 (Contoso 구독 1)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8feb3-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="8feb3-119">변수</span><span class="sxs-lookup"><span data-stu-id="8feb3-119">PARAMETERS</span></span>

### <span data-ttu-id="8feb3-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8feb3-120">-SubscriptionId</span></span>
<span data-ttu-id="8feb3-121">가져올 구독의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8feb3-121">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8feb3-122">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8feb3-122">-SubscriptionName</span></span>
<span data-ttu-id="8feb3-123">가져올 구독의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8feb3-123">Specifies the name of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8feb3-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="8feb3-124">-TenantId</span></span>
<span data-ttu-id="8feb3-125">가져올 구독이 포함 된 테 넌 트의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8feb3-125">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8feb3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8feb3-126">CommonParameters</span></span>
<span data-ttu-id="8feb3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8feb3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8feb3-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8feb3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8feb3-129">입력</span><span class="sxs-lookup"><span data-stu-id="8feb3-129">INPUTS</span></span>

## <span data-ttu-id="8feb3-130">출력</span><span class="sxs-lookup"><span data-stu-id="8feb3-130">OUTPUTS</span></span>

### <span data-ttu-id="8feb3-131">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="8feb3-131">PSAzureSubscription</span></span>

## <span data-ttu-id="8feb3-132">상속자</span><span class="sxs-lookup"><span data-stu-id="8feb3-132">NOTES</span></span>

## <span data-ttu-id="8feb3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8feb3-133">RELATED LINKS</span></span>

