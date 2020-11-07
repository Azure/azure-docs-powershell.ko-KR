---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 987793101e89a7f628f575bf7353994756edaeae
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874806"
---
# <span data-ttu-id="156dd-101">Move-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="156dd-101">Move-AzsSubscription</span></span>

## <span data-ttu-id="156dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="156dd-102">SYNOPSIS</span></span>
<span data-ttu-id="156dd-103">위임 된 공급자 제공 간에 구독을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="156dd-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="156dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="156dd-104">SYNTAX</span></span>

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="156dd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="156dd-105">DESCRIPTION</span></span>
<span data-ttu-id="156dd-106">위임 된 공급자 제공 간에 구독을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="156dd-106">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="156dd-107">이 프로세스는 다시 브랜드를 수행 하며, 구독에 대 한 기본 제공, 계획, 할당량은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="156dd-107">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="156dd-108">예제의</span><span class="sxs-lookup"><span data-stu-id="156dd-108">EXAMPLES</span></span>

### <span data-ttu-id="156dd-109">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="156dd-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Move user subscriptions to a delegated provider offer.
```

<span data-ttu-id="156dd-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="156dd-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="156dd-111">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="156dd-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Move user subscriptions from a delegated provider to the Default Provider.
```

<span data-ttu-id="156dd-112">$resourceIds = Get-AzsUserSubscription-필터 "offerName eq ' o1 '" | 여기서 {$ _. DelegatedProviderSubscriptionId-eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | 선택-ExpandProperty Id Move-AzsSubscription-ResourceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="156dd-112">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id Move-AzsSubscription -ResourceId $resourceIds</span></span>

## <span data-ttu-id="156dd-113">변수</span><span class="sxs-lookup"><span data-stu-id="156dd-113">PARAMETERS</span></span>

### <span data-ttu-id="156dd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="156dd-114">-AsJob</span></span>
<span data-ttu-id="156dd-115">이동 작업을 작업으로 실행할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="156dd-115">Specifies whether the move operation is to be executed as a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="156dd-116">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="156dd-116">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="156dd-117">이 cmdlet이 구독을 이동할 정식 위임 된 공급자 제안을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="156dd-117">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="156dd-118">구독이 기본 공급자로 다시 이동 되는 경우 NULL입니다.</span><span class="sxs-lookup"><span data-stu-id="156dd-118">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="156dd-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="156dd-119">-ResourceId</span></span>
<span data-ttu-id="156dd-120">이 cmdlet이 이동 하는 정규화 된 구독 리소스 식별자 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="156dd-120">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="156dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156dd-121">CommonParameters</span></span>
<span data-ttu-id="156dd-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="156dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156dd-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="156dd-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156dd-124">입력</span><span class="sxs-lookup"><span data-stu-id="156dd-124">INPUTS</span></span>

## <span data-ttu-id="156dd-125">출력</span><span class="sxs-lookup"><span data-stu-id="156dd-125">OUTPUTS</span></span>

## <span data-ttu-id="156dd-126">상속자</span><span class="sxs-lookup"><span data-stu-id="156dd-126">NOTES</span></span>

## <span data-ttu-id="156dd-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="156dd-127">RELATED LINKS</span></span>

