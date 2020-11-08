---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213515"
---
# <span data-ttu-id="eedca-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="eedca-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="eedca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eedca-102">SYNOPSIS</span></span>
<span data-ttu-id="eedca-103">개인 저장소에 대 한 제안을 업데이트 하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="eedca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eedca-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eedca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eedca-105">DESCRIPTION</span></span>
<span data-ttu-id="eedca-106">테 넌 트 범위 아래에서 만들어진 개인 저장소에 대 한 제안을 업데이트 하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="eedca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eedca-107">EXAMPLES</span></span>

### <span data-ttu-id="eedca-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="eedca-108">Example 1</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73, PublisherEnterpriseLinux73-ARM, PublisherEnterpriseLinux73-ARM-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="eedca-109">테 넌 트 범위 아래에 만들어진 개인 저장소에 대해 전용 + 공용 요금제를 사용 하 여 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="eedca-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="eedca-110">Example 2</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-ARM-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="eedca-111">구독 범위 아래에서 만든 개인 저장소에 대해서만 비공개 요금제를 사용 하 여 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="eedca-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="eedca-112">Example 3</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="eedca-113">테 넌 트 범위 아래에 만들어진 개인 저장소에 대 한 전용 및 공개 요금제를 사용 하 여 업데이트를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="eedca-114">Etag가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-114">Etag is needed.</span></span>

### <span data-ttu-id="eedca-115">예제 4</span><span class="sxs-lookup"><span data-stu-id="eedca-115">Example 4</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux73-pr") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="eedca-116">구독 범위 아래에서 만들어진 비공개 요금제를 사용 하 여 개인 저장소에 대 한 업데이트를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="eedca-117">Etag가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-117">Etag is needed.</span></span>


## <span data-ttu-id="eedca-118">변수</span><span class="sxs-lookup"><span data-stu-id="eedca-118">PARAMETERS</span></span>

### <span data-ttu-id="eedca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eedca-119">-DefaultProfile</span></span>
<span data-ttu-id="eedca-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eedca-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="eedca-121">-ETag</span></span>
<span data-ttu-id="eedca-122">Azure Marketplace privateStore 제공 업데이트의 eTag</span><span class="sxs-lookup"><span data-stu-id="eedca-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="eedca-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="eedca-123">-OfferId</span></span>
<span data-ttu-id="eedca-124">필수 Azure 마켓플레이스 privateStore 제공</span><span class="sxs-lookup"><span data-stu-id="eedca-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="eedca-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="eedca-125">-PrivateStoreId</span></span>
<span data-ttu-id="eedca-126">필수 Azure 마켓플레이스 privateStore 제공</span><span class="sxs-lookup"><span data-stu-id="eedca-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="eedca-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="eedca-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="eedca-128">필수 Azure Marketplace privateStore 제공의 특정 계획 id 제한 사항</span><span class="sxs-lookup"><span data-stu-id="eedca-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedca-129">-확인</span><span class="sxs-lookup"><span data-stu-id="eedca-129">-Confirm</span></span>
<span data-ttu-id="eedca-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedca-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eedca-131">-WhatIf</span></span>
<span data-ttu-id="eedca-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eedca-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eedca-134">CommonParameters</span></span>
<span data-ttu-id="eedca-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eedca-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eedca-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eedca-137">입력</span><span class="sxs-lookup"><span data-stu-id="eedca-137">INPUTS</span></span>

### <span data-ttu-id="eedca-138">않아야</span><span class="sxs-lookup"><span data-stu-id="eedca-138">None</span></span>

## <span data-ttu-id="eedca-139">출력</span><span class="sxs-lookup"><span data-stu-id="eedca-139">OUTPUTS</span></span>

### <span data-ttu-id="eedca-140">PrivateStore. PSPrivateStoreOffer에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="eedca-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="eedca-141">상속자</span><span class="sxs-lookup"><span data-stu-id="eedca-141">NOTES</span></span>

## <span data-ttu-id="eedca-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eedca-142">RELATED LINKS</span></span>
