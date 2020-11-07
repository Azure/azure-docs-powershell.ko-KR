---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azbgpservicecommunity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
ms.openlocfilehash: 6f57c03ab6501501745e66c7e49a986e8ece8dc0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700617"
---
# <span data-ttu-id="1531a-101">Get-AzBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="1531a-101">Get-AzBgpServiceCommunity</span></span>

## <span data-ttu-id="1531a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1531a-102">SYNOPSIS</span></span>
<span data-ttu-id="1531a-103">모든 서비스/지역, BGP 커뮤니티 및 연결 된 접두사 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1531a-103">Provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="1531a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1531a-104">SYNTAX</span></span>

```
Get-AzBgpServiceCommunity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1531a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1531a-105">DESCRIPTION</span></span>
<span data-ttu-id="1531a-106">이 cmdlet은 모든 서비스/지역, BGP 커뮤니티 및 연결 된 접두사의 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1531a-106">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="1531a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1531a-107">EXAMPLES</span></span>

### <span data-ttu-id="1531a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1531a-108">Example 1</span></span>
```
Get-AzBgpServiceCommunity

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

<span data-ttu-id="1531a-109">이 cmdlet은 모든 서비스/지역, BGP 커뮤니티 및 연결 된 접두사의 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1531a-109">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="1531a-110">변수</span><span class="sxs-lookup"><span data-stu-id="1531a-110">PARAMETERS</span></span>

### <span data-ttu-id="1531a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1531a-111">-DefaultProfile</span></span>
<span data-ttu-id="1531a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1531a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1531a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1531a-113">CommonParameters</span></span>
<span data-ttu-id="1531a-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1531a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1531a-115">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1531a-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1531a-116">입력</span><span class="sxs-lookup"><span data-stu-id="1531a-116">INPUTS</span></span>

### <span data-ttu-id="1531a-117">않아야</span><span class="sxs-lookup"><span data-stu-id="1531a-117">None</span></span>

## <span data-ttu-id="1531a-118">출력</span><span class="sxs-lookup"><span data-stu-id="1531a-118">OUTPUTS</span></span>

### <span data-ttu-id="1531a-119">PSBgpServiceCommunity에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1531a-119">Microsoft.Azure.Commands.Network.Models.PSBgpServiceCommunity</span></span>

## <span data-ttu-id="1531a-120">상속자</span><span class="sxs-lookup"><span data-stu-id="1531a-120">NOTES</span></span>

## <span data-ttu-id="1531a-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1531a-121">RELATED LINKS</span></span>

[<span data-ttu-id="1531a-122">이동-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1531a-122">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="1531a-123">새로운 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1531a-123">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="1531a-124">제거-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1531a-124">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="1531a-125">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1531a-125">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="1531a-126">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1531a-126">Get-AzRouteFilter</span></span>](Get-AzRouteFilter.md)

[<span data-ttu-id="1531a-127">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1531a-127">Get-AzRouteFilterRuleConfig</span></span>](Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1531a-128">제거-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1531a-128">Remove-AzRouteFilter</span></span>](Remove-AzRouteFilter.md)

[<span data-ttu-id="1531a-129">제거-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1531a-129">Remove-AzRouteFilterRuleConfig</span></span>](Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1531a-130">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1531a-130">Set-AzRouteFilter</span></span>](Set-AzRouteFilter.md)

[<span data-ttu-id="1531a-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1531a-131">Set-AzRouteFilterRuleConfig</span></span>](Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1531a-132">새로운 AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1531a-132">New-AzRouteFilter</span></span>](New-AzRouteFilter.md)

[<span data-ttu-id="1531a-133">새로운 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1531a-133">New-AzRouteFilterRuleConfig</span></span>](New-AzRouteFilterRuleConfig.md)
