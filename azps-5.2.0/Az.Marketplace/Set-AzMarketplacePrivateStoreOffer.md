---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329906"
---
# <span data-ttu-id="2dde0-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="2dde0-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="2dde0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dde0-102">SYNOPSIS</span></span>
<span data-ttu-id="2dde0-103">개인 저장소에 대한 제안을 업데이트하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="2dde0-104">구문</span><span class="sxs-lookup"><span data-stu-id="2dde0-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dde0-105">설명</span><span class="sxs-lookup"><span data-stu-id="2dde0-105">DESCRIPTION</span></span>
<span data-ttu-id="2dde0-106">테넌트 범위에서 만든 개인 저장소에 대한 제안을 업데이트하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="2dde0-107">예제</span><span class="sxs-lookup"><span data-stu-id="2dde0-107">EXAMPLES</span></span>

### <span data-ttu-id="2dde0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2dde0-108">Example 1</span></span>
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

<span data-ttu-id="2dde0-109">테넌트 범위에서 만든 개인 저장소에 대한 개인 + 공용 계획을 통해 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="2dde0-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="2dde0-110">Example 2</span></span>
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

<span data-ttu-id="2dde0-111">구독 범위에서 만든 개인 저장소에 대한 전용 계획으로만 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="2dde0-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="2dde0-112">Example 3</span></span>
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

<span data-ttu-id="2dde0-113">테넌트 범위에서 만든 개인 저장소에 대한 개인 + 공용 계획으로 제안을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="2dde0-114">Etag가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-114">Etag is needed.</span></span>

### <span data-ttu-id="2dde0-115">예제 4</span><span class="sxs-lookup"><span data-stu-id="2dde0-115">Example 4</span></span>
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

<span data-ttu-id="2dde0-116">구독 범위에서 만든 개인 계획만 있는 개인 저장소에 대한 제안을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="2dde0-117">Etag가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-117">Etag is needed.</span></span>


## <span data-ttu-id="2dde0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dde0-118">PARAMETERS</span></span>

### <span data-ttu-id="2dde0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dde0-119">-DefaultProfile</span></span>
<span data-ttu-id="2dde0-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dde0-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="2dde0-121">-ETag</span></span>
<span data-ttu-id="2dde0-122">Azure Marketplace privateStore 제안의 업데이트용 eTag</span><span class="sxs-lookup"><span data-stu-id="2dde0-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="2dde0-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="2dde0-123">-OfferId</span></span>
<span data-ttu-id="2dde0-124">필수 Azure Marketplace privateStore 제품</span><span class="sxs-lookup"><span data-stu-id="2dde0-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="2dde0-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="2dde0-125">-PrivateStoreId</span></span>
<span data-ttu-id="2dde0-126">필수 Azure Marketplace privateStore 제안</span><span class="sxs-lookup"><span data-stu-id="2dde0-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="2dde0-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="2dde0-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="2dde0-128">필수 Azure Marketplace privateStore 제안의 특정 계획 ID 제한</span><span class="sxs-lookup"><span data-stu-id="2dde0-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

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

### <span data-ttu-id="2dde0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2dde0-129">-Confirm</span></span>
<span data-ttu-id="2dde0-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dde0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dde0-131">-WhatIf</span></span>
<span data-ttu-id="2dde0-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2dde0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dde0-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dde0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dde0-134">CommonParameters</span></span>
<span data-ttu-id="2dde0-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2dde0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dde0-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2dde0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dde0-137">입력</span><span class="sxs-lookup"><span data-stu-id="2dde0-137">INPUTS</span></span>

### <span data-ttu-id="2dde0-138">없음</span><span class="sxs-lookup"><span data-stu-id="2dde0-138">None</span></span>

## <span data-ttu-id="2dde0-139">출력</span><span class="sxs-lookup"><span data-stu-id="2dde0-139">OUTPUTS</span></span>

### <span data-ttu-id="2dde0-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="2dde0-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="2dde0-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2dde0-141">NOTES</span></span>

## <span data-ttu-id="2dde0-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2dde0-142">RELATED LINKS</span></span>
