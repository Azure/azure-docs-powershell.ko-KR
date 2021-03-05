---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 9a2f5744f5595b7be4a0a59c3181435e4f1d0eb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009616"
---
# <span data-ttu-id="64cd0-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="64cd0-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="64cd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="64cd0-103">개인 저장소에 대한 제안을 업데이트하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="64cd0-104">구문</span><span class="sxs-lookup"><span data-stu-id="64cd0-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64cd0-105">설명</span><span class="sxs-lookup"><span data-stu-id="64cd0-105">DESCRIPTION</span></span>
<span data-ttu-id="64cd0-106">테넌트 범위에서 만든 개인 저장소에 대한 제안을 업데이트하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="64cd0-107">예제</span><span class="sxs-lookup"><span data-stu-id="64cd0-107">EXAMPLES</span></span>

### <span data-ttu-id="64cd0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="64cd0-108">Example 1</span></span>
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

<span data-ttu-id="64cd0-109">테넌트 범위에서 만든 개인 저장소에 대한 개인 + 공용 요금제로 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="64cd0-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="64cd0-110">Example 2</span></span>
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

<span data-ttu-id="64cd0-111">구독 범위에서 만든 개인 저장소에만 개인 요금제가 있는 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="64cd0-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="64cd0-112">Example 3</span></span>
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

<span data-ttu-id="64cd0-113">테넌트 범위에서 만든 개인 저장소에 대한 개인 + 공용 요금제가 있는 업데이트 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="64cd0-114">Etag가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-114">Etag is needed.</span></span>

### <span data-ttu-id="64cd0-115">예제 4</span><span class="sxs-lookup"><span data-stu-id="64cd0-115">Example 4</span></span>
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

<span data-ttu-id="64cd0-116">구독 범위에서 만든 개인 요금제가 있는 개인 저장소에 대한 업데이트 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="64cd0-117">Etag가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-117">Etag is needed.</span></span>


## <span data-ttu-id="64cd0-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="64cd0-118">PARAMETERS</span></span>

### <span data-ttu-id="64cd0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64cd0-119">-DefaultProfile</span></span>
<span data-ttu-id="64cd0-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64cd0-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="64cd0-121">-ETag</span></span>
<span data-ttu-id="64cd0-122">Azure Marketplace privateStore 제품 eTag for update</span><span class="sxs-lookup"><span data-stu-id="64cd0-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="64cd0-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="64cd0-123">-OfferId</span></span>
<span data-ttu-id="64cd0-124">필수 Azure Marketplace privateStore 제품</span><span class="sxs-lookup"><span data-stu-id="64cd0-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="64cd0-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="64cd0-125">-PrivateStoreId</span></span>
<span data-ttu-id="64cd0-126">필수 Azure Marketplace privateStore 제안</span><span class="sxs-lookup"><span data-stu-id="64cd0-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="64cd0-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="64cd0-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="64cd0-128">필수 Azure Marketplace privateStore 제품의 특정 계획 ID 제한</span><span class="sxs-lookup"><span data-stu-id="64cd0-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

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

### <span data-ttu-id="64cd0-129">-확인</span><span class="sxs-lookup"><span data-stu-id="64cd0-129">-Confirm</span></span>
<span data-ttu-id="64cd0-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64cd0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64cd0-131">-WhatIf</span></span>
<span data-ttu-id="64cd0-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64cd0-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64cd0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64cd0-134">CommonParameters</span></span>
<span data-ttu-id="64cd0-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="64cd0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64cd0-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64cd0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64cd0-137">입력</span><span class="sxs-lookup"><span data-stu-id="64cd0-137">INPUTS</span></span>

### <span data-ttu-id="64cd0-138">없음</span><span class="sxs-lookup"><span data-stu-id="64cd0-138">None</span></span>

## <span data-ttu-id="64cd0-139">출력</span><span class="sxs-lookup"><span data-stu-id="64cd0-139">OUTPUTS</span></span>

### <span data-ttu-id="64cd0-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="64cd0-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="64cd0-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="64cd0-141">NOTES</span></span>

## <span data-ttu-id="64cd0-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64cd0-142">RELATED LINKS</span></span>
