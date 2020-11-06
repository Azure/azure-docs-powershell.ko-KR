---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermbgpservicecommunity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmBgpServiceCommunity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmBgpServiceCommunity.md
ms.openlocfilehash: f951aab0ab655d073c830d08e2665533c961960a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533359"
---
# <span data-ttu-id="c97cb-101">Get-AzureRmBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="c97cb-101">Get-AzureRmBgpServiceCommunity</span></span>

## <span data-ttu-id="c97cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c97cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c97cb-103">모든 서비스/지역, BGP 커뮤니티 및 연결 된 접두사 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c97cb-103">Provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c97cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c97cb-104">SYNTAX</span></span>

```
Get-AzureRmBgpServiceCommunity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c97cb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c97cb-105">DESCRIPTION</span></span>
<span data-ttu-id="c97cb-106">이 cmdlet은 모든 서비스/지역, BGP 커뮤니티 및 연결 된 접두사의 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c97cb-106">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="c97cb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c97cb-107">EXAMPLES</span></span>

### <span data-ttu-id="c97cb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c97cb-108">Example 1</span></span>
```
Get-AzureRmBgpServiceCommunity

...

Name           : AzureCentralIndia
Id             : /subscriptions//resourceGroups//providers/Microsoft.Network/bgpServiceCommunities/AzureCentralIndia
Type           : Microsoft.Network/bgpServiceCommunities
BgpCommunities : [
                   {
                     "ServiceSupportedRegion": "Global",
                     "CommunityName": "Azure Central India",
                     "CommunityValue": "12076:51017",
                     "CommunityPrefixes": [
                       "13.71.0.0/18",
                       "20.190.146.0/25",
                       "40.79.214.0/24",
                       "40.81.224.0/19",
                       "40.87.224.0/22",
                       "40.112.39.0/25",
                       "40.112.39.128/26",
                       "40.126.18.0/25",
                       "52.136.24.0/24",
                       "52.140.64.0/18",
                       "52.159.64.0/19",
                       "52.172.128.0/17",
                       "52.239.135.64/26",
                       "52.239.202.0/24",
                       "52.245.96.0/22",
                       "52.253.168.0/22",
                       "104.47.210.0/23",
                       "104.211.64.0/20",
                       "104.211.81.0/24",
                       "104.211.82.0/23",
                       "104.211.84.0/22",
                       "104.211.88.0/21",
                       "104.211.96.0/19"
                     ],
                     "IsAuthorizedToUse": true,
                     "ServiceGroup": "Azure"
                   }
                 ]
...
```

<span data-ttu-id="c97cb-109">이 cmdlet은 모든 서비스/지역, BGP 커뮤니티 및 연결 된 접두사의 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c97cb-109">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="c97cb-110">변수</span><span class="sxs-lookup"><span data-stu-id="c97cb-110">PARAMETERS</span></span>

### <span data-ttu-id="c97cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97cb-111">-DefaultProfile</span></span>
<span data-ttu-id="c97cb-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c97cb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c97cb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97cb-113">CommonParameters</span></span>
<span data-ttu-id="c97cb-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c97cb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97cb-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c97cb-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97cb-116">입력</span><span class="sxs-lookup"><span data-stu-id="c97cb-116">INPUTS</span></span>

### <span data-ttu-id="c97cb-117">않아야</span><span class="sxs-lookup"><span data-stu-id="c97cb-117">None</span></span>

## <span data-ttu-id="c97cb-118">출력</span><span class="sxs-lookup"><span data-stu-id="c97cb-118">OUTPUTS</span></span>

### <span data-ttu-id="c97cb-119">PSBgpServiceCommunity에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c97cb-119">Microsoft.Azure.Commands.Network.Models.PSBgpServiceCommunity</span></span>

## <span data-ttu-id="c97cb-120">상속자</span><span class="sxs-lookup"><span data-stu-id="c97cb-120">NOTES</span></span>

## <span data-ttu-id="c97cb-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c97cb-121">RELATED LINKS</span></span>

[<span data-ttu-id="c97cb-122">이동-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c97cb-122">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c97cb-123">새로운 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c97cb-123">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c97cb-124">제거-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c97cb-124">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c97cb-125">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c97cb-125">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c97cb-126">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c97cb-126">Get-AzureRmRouteFilter</span></span>](Get-AzureRmRouteFilter.md)

[<span data-ttu-id="c97cb-127">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c97cb-127">Get-AzureRmRouteFilterRuleConfig</span></span>](Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="c97cb-128">제거-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c97cb-128">Remove-AzureRmRouteFilter</span></span>](Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="c97cb-129">제거-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c97cb-129">Remove-AzureRmRouteFilterRuleConfig</span></span>](Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="c97cb-130">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c97cb-130">Set-AzureRmRouteFilter</span></span>](Set-AzureRmRouteFilter.md)

[<span data-ttu-id="c97cb-131">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c97cb-131">Set-AzureRmRouteFilterRuleConfig</span></span>](Set-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="c97cb-132">새로운 AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c97cb-132">New-AzureRmRouteFilter</span></span>](New-AzureRmRouteFilter.md)

[<span data-ttu-id="c97cb-133">새로운 AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c97cb-133">New-AzureRmRouteFilterRuleConfig</span></span>](New-AzureRmRouteFilterRuleConfig.md)
