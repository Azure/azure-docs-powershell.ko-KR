---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056670"
---
# <span data-ttu-id="5f8f2-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="5f8f2-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="5f8f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8f2-103">하나 이상의 개인 저장소 제안을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="5f8f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f8f2-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f8f2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5f8f2-105">DESCRIPTION</span></span>
<span data-ttu-id="5f8f2-106">테 넌 트 범위 아래에 추가 된 공개 + 전용 요금제를 사용 하 여 하나 이상의 개인 저장소 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="5f8f2-107">구독 id가 표시 되는 경우 구독 범위 아래에 있는 비공개 요금제를 사용 하 여 하나 이상의 개인 저장소 제안을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="5f8f2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5f8f2-108">EXAMPLES</span></span>

### <span data-ttu-id="5f8f2-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="5f8f2-109">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional ,azure_managedservices_professional-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="5f8f2-110">테 넌 트 범위 아래에 추가 된 개인 및 공개 요금제를 사용 하 여 개인 저장소의 제안을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="5f8f2-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="5f8f2-111">Example 2</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="5f8f2-112">구독 범위 아래에 추가 된 개인 요금제로 개인 저장소의 제안을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="5f8f2-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="5f8f2-113">Example 3</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="5f8f2-114">테 넌 트 범위 아래에 추가 된 비공개 + 공개 계획이 있는 개인 저장소의 제안을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="5f8f2-115">예제 4</span><span class="sxs-lookup"><span data-stu-id="5f8f2-115">Example 4</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="5f8f2-116">테 넌 트 범위에 추가 된 비공개 요금제를 사용 하 여 개인 저장소의 제안을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="5f8f2-117">변수</span><span class="sxs-lookup"><span data-stu-id="5f8f2-117">PARAMETERS</span></span>

### <span data-ttu-id="5f8f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f8f2-118">-DefaultProfile</span></span>
<span data-ttu-id="5f8f2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f8f2-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="5f8f2-120">-OfferId</span></span>
<span data-ttu-id="5f8f2-121">필수 Azure 마켓플레이스 privateStore 제공</span><span class="sxs-lookup"><span data-stu-id="5f8f2-121">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f8f2-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="5f8f2-122">-PrivateStoreId</span></span>
<span data-ttu-id="5f8f2-123">필수 Azure 마켓플레이스 privateStore 제공</span><span class="sxs-lookup"><span data-stu-id="5f8f2-123">Required Azure Marketplace privateStore offers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f8f2-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f8f2-124">-SubscriptionId</span></span>
<span data-ttu-id="5f8f2-125">Azure Marketplace 구독 id</span><span class="sxs-lookup"><span data-stu-id="5f8f2-125">Azure Marketplace subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f8f2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8f2-126">CommonParameters</span></span>
<span data-ttu-id="5f8f2-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8f2-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8f2-129">입력</span><span class="sxs-lookup"><span data-stu-id="5f8f2-129">INPUTS</span></span>

### <span data-ttu-id="5f8f2-130">않아야</span><span class="sxs-lookup"><span data-stu-id="5f8f2-130">None</span></span>

## <span data-ttu-id="5f8f2-131">출력</span><span class="sxs-lookup"><span data-stu-id="5f8f2-131">OUTPUTS</span></span>

### <span data-ttu-id="5f8f2-132">PrivateStore. PSPrivateStoreOffer에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="5f8f2-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="5f8f2-133">상속자</span><span class="sxs-lookup"><span data-stu-id="5f8f2-133">NOTES</span></span>

## <span data-ttu-id="5f8f2-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f8f2-134">RELATED LINKS</span></span>
