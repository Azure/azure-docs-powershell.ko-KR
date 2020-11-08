---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042194"
---
# <span data-ttu-id="d5f3b-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5f3b-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="d5f3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f3b-103">CDN 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d5f3b-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="d5f3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5f3b-104">SYNTAX</span></span>

### <span data-ttu-id="d5f3b-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d5f3b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f3b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f3b-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5f3b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d5f3b-107">DESCRIPTION</span></span>
<span data-ttu-id="d5f3b-108">**AzCdnEndpoint** CMDLET은 CDN (Azure Content Delivery Network) 끝점 및 연결 된 구성 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d5f3b-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="d5f3b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d5f3b-109">EXAMPLES</span></span>

## <span data-ttu-id="d5f3b-110">변수</span><span class="sxs-lookup"><span data-stu-id="d5f3b-110">PARAMETERS</span></span>

### <span data-ttu-id="d5f3b-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="d5f3b-111">-CdnProfile</span></span>
<span data-ttu-id="d5f3b-112">끝점이 속한 CDN 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5f3b-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f3b-113">-DefaultProfile</span></span>
<span data-ttu-id="d5f3b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d5f3b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5f3b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d5f3b-115">-EndpointName</span></span>
<span data-ttu-id="d5f3b-116">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5f3b-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="d5f3b-117">끝점의 이름이 끝점의 호스트 이름이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="d5f3b-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="d5f3b-118">-/Profile</span><span class="sxs-lookup"><span data-stu-id="d5f3b-118">-ProfileName</span></span>
<span data-ttu-id="d5f3b-119">종점이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5f3b-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d5f3b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5f3b-120">-ResourceGroupName</span></span>
<span data-ttu-id="d5f3b-121">끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5f3b-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d5f3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f3b-122">CommonParameters</span></span>
<span data-ttu-id="d5f3b-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5f3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f3b-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d5f3b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f3b-125">입력</span><span class="sxs-lookup"><span data-stu-id="d5f3b-125">INPUTS</span></span>

### <span data-ttu-id="d5f3b-126">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="d5f3b-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="d5f3b-127">출력</span><span class="sxs-lookup"><span data-stu-id="d5f3b-127">OUTPUTS</span></span>

### <span data-ttu-id="d5f3b-128">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5f3b-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="d5f3b-129">상속자</span><span class="sxs-lookup"><span data-stu-id="d5f3b-129">NOTES</span></span>

## <span data-ttu-id="d5f3b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5f3b-130">RELATED LINKS</span></span>

[<span data-ttu-id="d5f3b-131">새로운 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5f3b-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="d5f3b-132">제거-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5f3b-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="d5f3b-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5f3b-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="d5f3b-134">시작-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5f3b-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="d5f3b-135">중지-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5f3b-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


