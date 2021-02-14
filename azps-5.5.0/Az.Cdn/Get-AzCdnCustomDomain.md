---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195172"
---
# <span data-ttu-id="83496-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83496-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="83496-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83496-102">SYNOPSIS</span></span>
<span data-ttu-id="83496-103">CDN 사용자 지정 도메인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83496-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="83496-104">구문</span><span class="sxs-lookup"><span data-stu-id="83496-104">SYNTAX</span></span>

### <span data-ttu-id="83496-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="83496-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83496-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83496-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83496-107">설명</span><span class="sxs-lookup"><span data-stu-id="83496-107">DESCRIPTION</span></span>
<span data-ttu-id="83496-108">**Get-AzCdnCustomDomain** cmdlet은 Azure CDN(Content Delivery Network) 사용자 지정 도메인 및 관련 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83496-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="83496-109">예제</span><span class="sxs-lookup"><span data-stu-id="83496-109">EXAMPLES</span></span>

## <span data-ttu-id="83496-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83496-110">PARAMETERS</span></span>

### <span data-ttu-id="83496-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="83496-111">-CdnEndpoint</span></span>
<span data-ttu-id="83496-112">사용자 지정 도메인이 구성원인 CDN 엔드포인트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83496-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="83496-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="83496-113">-CustomDomainName</span></span>
<span data-ttu-id="83496-114">사용자 지정 도메인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83496-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="83496-115">사용자 지정 도메인의 이름은 사용자 지정 도메인의 호스트 이름과 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="83496-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="83496-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83496-116">-DefaultProfile</span></span>
<span data-ttu-id="83496-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="83496-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83496-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="83496-118">-EndpointName</span></span>
<span data-ttu-id="83496-119">사용자 지정 도메인이 속한 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83496-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="83496-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="83496-120">-ProfileName</span></span>
<span data-ttu-id="83496-121">사용자 지정 도메인이 속한 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83496-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="83496-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83496-122">-ResourceGroupName</span></span>
<span data-ttu-id="83496-123">사용자 지정 도메인이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83496-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="83496-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83496-124">CommonParameters</span></span>
<span data-ttu-id="83496-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83496-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83496-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83496-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83496-127">입력</span><span class="sxs-lookup"><span data-stu-id="83496-127">INPUTS</span></span>

### <span data-ttu-id="83496-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="83496-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="83496-129">출력</span><span class="sxs-lookup"><span data-stu-id="83496-129">OUTPUTS</span></span>

### <span data-ttu-id="83496-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83496-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="83496-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83496-131">NOTES</span></span>

## <span data-ttu-id="83496-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83496-132">RELATED LINKS</span></span>

[<span data-ttu-id="83496-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83496-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="83496-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83496-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


