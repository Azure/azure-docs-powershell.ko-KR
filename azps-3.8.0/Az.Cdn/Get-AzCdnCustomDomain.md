---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034265"
---
# <span data-ttu-id="666d8-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="666d8-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="666d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="666d8-102">SYNOPSIS</span></span>
<span data-ttu-id="666d8-103">CDN 사용자 지정 도메인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="666d8-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="666d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="666d8-104">SYNTAX</span></span>

### <span data-ttu-id="666d8-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="666d8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="666d8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="666d8-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="666d8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="666d8-107">DESCRIPTION</span></span>
<span data-ttu-id="666d8-108">**AzCdnCustomDomain** CMDLET은 CDN (Azure Content Delivery Network) 사용자 지정 도메인 및 관련 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="666d8-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="666d8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="666d8-109">EXAMPLES</span></span>

## <span data-ttu-id="666d8-110">변수</span><span class="sxs-lookup"><span data-stu-id="666d8-110">PARAMETERS</span></span>

### <span data-ttu-id="666d8-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="666d8-111">-CdnEndpoint</span></span>
<span data-ttu-id="666d8-112">사용자 지정 도메인이 멤버인 CDN 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="666d8-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="666d8-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="666d8-113">-CustomDomainName</span></span>
<span data-ttu-id="666d8-114">사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="666d8-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="666d8-115">사용자 지정 도메인의 이름이 사용자 지정 도메인의 호스트 이름과 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="666d8-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="666d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666d8-116">-DefaultProfile</span></span>
<span data-ttu-id="666d8-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="666d8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="666d8-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="666d8-118">-EndpointName</span></span>
<span data-ttu-id="666d8-119">사용자 지정 도메인이 속한 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="666d8-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="666d8-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="666d8-120">-ProfileName</span></span>
<span data-ttu-id="666d8-121">사용자 지정 도메인이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="666d8-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="666d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="666d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="666d8-123">사용자 지정 도메인이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="666d8-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="666d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666d8-124">CommonParameters</span></span>
<span data-ttu-id="666d8-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="666d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666d8-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="666d8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666d8-127">입력</span><span class="sxs-lookup"><span data-stu-id="666d8-127">INPUTS</span></span>

### <span data-ttu-id="666d8-128">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="666d8-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="666d8-129">출력</span><span class="sxs-lookup"><span data-stu-id="666d8-129">OUTPUTS</span></span>

### <span data-ttu-id="666d8-130">PSCustomDomain (.). c.</span><span class="sxs-lookup"><span data-stu-id="666d8-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="666d8-131">상속자</span><span class="sxs-lookup"><span data-stu-id="666d8-131">NOTES</span></span>

## <span data-ttu-id="666d8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="666d8-132">RELATED LINKS</span></span>

[<span data-ttu-id="666d8-133">새로운 AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="666d8-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="666d8-134">제거-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="666d8-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


