---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a04836e2d361f4c9686fa5dfe62babfa57ade189
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047085"
---
# <span data-ttu-id="d0107-101">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="d0107-101">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="d0107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0107-102">SYNOPSIS</span></span>
<span data-ttu-id="d0107-103">위임 된 공급자 제공 간에 사용자 구독을 이동할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0107-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="d0107-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0107-104">SYNTAX</span></span>

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="d0107-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d0107-105">DESCRIPTION</span></span>
<span data-ttu-id="d0107-106">위임 된 공급자 제공 간에 사용자 구독을 이동할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0107-106">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="d0107-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d0107-107">EXAMPLES</span></span>

### <span data-ttu-id="d0107-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0107-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test that user subscriptions can be moved to a delegated provider offer.
```

<span data-ttu-id="d0107-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="d0107-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="d0107-110">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0107-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

<span data-ttu-id="d0107-111">$resourceIds = Get-AzsUserSubscription-필터 "offerName eq ' o1 '" | 선택-ExpandProperty Id Test-MoveSubscription-ResoruceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="d0107-111">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | Select -ExpandProperty Id Test-MoveSubscription -ResoruceId $resourceIds</span></span>

## <span data-ttu-id="d0107-112">변수</span><span class="sxs-lookup"><span data-stu-id="d0107-112">PARAMETERS</span></span>

### <span data-ttu-id="d0107-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0107-113">-AsJob</span></span>
<span data-ttu-id="d0107-114">이동 작업을 작업으로 실행할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0107-114">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="d0107-115">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="d0107-115">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="d0107-116">이 cmdlet이 구독을 이동할 정식 위임 된 공급자 제안을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0107-116">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="d0107-117">구독이 기본 공급자로 다시 이동 되는 경우 NULL입니다.</span><span class="sxs-lookup"><span data-stu-id="d0107-117">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="d0107-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0107-118">-ResourceId</span></span>
<span data-ttu-id="d0107-119">이 cmdlet이 이동 하는 정규화 된 구독 리소스 식별자 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0107-119">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

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

### <span data-ttu-id="d0107-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0107-120">CommonParameters</span></span>
<span data-ttu-id="d0107-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0107-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0107-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0107-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0107-123">입력</span><span class="sxs-lookup"><span data-stu-id="d0107-123">INPUTS</span></span>

## <span data-ttu-id="d0107-124">출력</span><span class="sxs-lookup"><span data-stu-id="d0107-124">OUTPUTS</span></span>

## <span data-ttu-id="d0107-125">상속자</span><span class="sxs-lookup"><span data-stu-id="d0107-125">NOTES</span></span>

## <span data-ttu-id="d0107-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0107-126">RELATED LINKS</span></span>

