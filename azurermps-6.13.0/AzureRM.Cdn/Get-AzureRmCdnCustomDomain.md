---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e0c1d2e49cce4798499506352811d1e341bf47e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536731"
---
# <span data-ttu-id="a89ed-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a89ed-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="a89ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a89ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a89ed-103">CDN 사용자 지정 도메인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a89ed-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a89ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a89ed-104">SYNTAX</span></span>

### <span data-ttu-id="a89ed-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a89ed-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a89ed-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89ed-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a89ed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a89ed-107">DESCRIPTION</span></span>
<span data-ttu-id="a89ed-108">**AzureRmCdnCustomDomain** CMDLET은 CDN (Azure Content Delivery Network) 사용자 지정 도메인 및 관련 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a89ed-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="a89ed-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a89ed-109">EXAMPLES</span></span>

## <span data-ttu-id="a89ed-110">변수</span><span class="sxs-lookup"><span data-stu-id="a89ed-110">PARAMETERS</span></span>

### <span data-ttu-id="a89ed-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a89ed-111">-CdnEndpoint</span></span>
<span data-ttu-id="a89ed-112">사용자 지정 도메인이 멤버인 CDN 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a89ed-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="a89ed-113">-CustomDomainName</span></span>
<span data-ttu-id="a89ed-114">사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a89ed-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="a89ed-115">사용자 지정 도메인의 이름이 사용자 지정 도메인의 호스트 이름과 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="a89ed-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="a89ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89ed-116">-DefaultProfile</span></span>
<span data-ttu-id="a89ed-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a89ed-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a89ed-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a89ed-118">-EndpointName</span></span>
<span data-ttu-id="a89ed-119">사용자 지정 도메인이 속한 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a89ed-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="a89ed-120">-ProfileName</span></span>
<span data-ttu-id="a89ed-121">사용자 지정 도메인이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a89ed-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a89ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="a89ed-123">사용자 지정 도메인이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a89ed-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89ed-124">CommonParameters</span></span>
<span data-ttu-id="a89ed-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a89ed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89ed-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a89ed-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89ed-127">입력</span><span class="sxs-lookup"><span data-stu-id="a89ed-127">INPUTS</span></span>

### <span data-ttu-id="a89ed-128">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a89ed-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="a89ed-129">매개 변수: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a89ed-129">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="a89ed-130">출력</span><span class="sxs-lookup"><span data-stu-id="a89ed-130">OUTPUTS</span></span>

### <span data-ttu-id="a89ed-131">PSCustomDomain (.). c.</span><span class="sxs-lookup"><span data-stu-id="a89ed-131">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="a89ed-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a89ed-132">NOTES</span></span>

## <span data-ttu-id="a89ed-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a89ed-133">RELATED LINKS</span></span>

[<span data-ttu-id="a89ed-134">새로운 AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a89ed-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="a89ed-135">제거-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a89ed-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


