---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 3c7356768db35ce2c21499db0a94402f040b5162
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003776"
---
# <span data-ttu-id="8a597-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="8a597-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="8a597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a597-102">SYNOPSIS</span></span>
<span data-ttu-id="8a597-103">하나 이상의 개인 저장소의 제안을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a597-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="8a597-104">구문</span><span class="sxs-lookup"><span data-stu-id="8a597-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a597-105">설명</span><span class="sxs-lookup"><span data-stu-id="8a597-105">DESCRIPTION</span></span>
<span data-ttu-id="8a597-106">테넌트 범위에 따라 추가된 공용 + 개인 요금제로 하나 이상의 개인 저장소의 제안을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a597-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="8a597-107">구독 ID가 있는 경우 구독 범위에서만 개인 요금제가 있는 하나 이상의 사설 저장소의 제안을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a597-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="8a597-108">예제</span><span class="sxs-lookup"><span data-stu-id="8a597-108">EXAMPLES</span></span>

### <span data-ttu-id="8a597-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="8a597-109">Example 1</span></span>
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

<span data-ttu-id="8a597-110">테넌트 범위에 추가된 개인 + 공용 요금제로 개인 저장소의 제안을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a597-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="8a597-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="8a597-111">Example 2</span></span>
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

<span data-ttu-id="8a597-112">구독 범위에서 추가된 개인 요금제로 개인 저장소의 제안을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a597-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="8a597-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="8a597-113">Example 3</span></span>
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

<span data-ttu-id="8a597-114">테넌트 범위에 추가된 개인 + 공용 요금제로 개인 저장소의 제안을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a597-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="8a597-115">예제 4</span><span class="sxs-lookup"><span data-stu-id="8a597-115">Example 4</span></span>
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

<span data-ttu-id="8a597-116">테넌트 범위에서 추가된 개인 요금제로 개인 저장소의 제안을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a597-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="8a597-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8a597-117">PARAMETERS</span></span>

### <span data-ttu-id="8a597-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a597-118">-DefaultProfile</span></span>
<span data-ttu-id="8a597-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a597-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a597-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="8a597-120">-OfferId</span></span>
<span data-ttu-id="8a597-121">필수 Azure Marketplace privateStore 제품</span><span class="sxs-lookup"><span data-stu-id="8a597-121">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="8a597-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="8a597-122">-PrivateStoreId</span></span>
<span data-ttu-id="8a597-123">필수 Azure Marketplace privateStore 제안</span><span class="sxs-lookup"><span data-stu-id="8a597-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="8a597-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a597-124">-SubscriptionId</span></span>
<span data-ttu-id="8a597-125">Azure Marketplace 구독 ID</span><span class="sxs-lookup"><span data-stu-id="8a597-125">Azure Marketplace subscription id</span></span>

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

### <span data-ttu-id="8a597-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a597-126">CommonParameters</span></span>
<span data-ttu-id="8a597-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8a597-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a597-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a597-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a597-129">입력</span><span class="sxs-lookup"><span data-stu-id="8a597-129">INPUTS</span></span>

### <span data-ttu-id="8a597-130">없음</span><span class="sxs-lookup"><span data-stu-id="8a597-130">None</span></span>

## <span data-ttu-id="8a597-131">출력</span><span class="sxs-lookup"><span data-stu-id="8a597-131">OUTPUTS</span></span>

### <span data-ttu-id="8a597-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="8a597-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="8a597-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8a597-133">NOTES</span></span>

## <span data-ttu-id="8a597-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a597-134">RELATED LINKS</span></span>
