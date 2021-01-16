---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347253"
---
# <span data-ttu-id="b7791-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7791-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="b7791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7791-102">SYNOPSIS</span></span>
<span data-ttu-id="b7791-103">CDN 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7791-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="b7791-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7791-104">SYNTAX</span></span>

### <span data-ttu-id="b7791-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b7791-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7791-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7791-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7791-107">설명</span><span class="sxs-lookup"><span data-stu-id="b7791-107">DESCRIPTION</span></span>
<span data-ttu-id="b7791-108">**Get-AzCdnEndpoint** cmdlet은 Azure CDN(Content Delivery Network) 엔드포인트 및 관련 구성 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7791-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="b7791-109">예제</span><span class="sxs-lookup"><span data-stu-id="b7791-109">EXAMPLES</span></span>

## <span data-ttu-id="b7791-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7791-110">PARAMETERS</span></span>

### <span data-ttu-id="b7791-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b7791-111">-CdnProfile</span></span>
<span data-ttu-id="b7791-112">엔드포인트가 속한 CDN 프로필 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7791-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b7791-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7791-113">-DefaultProfile</span></span>
<span data-ttu-id="b7791-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b7791-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7791-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b7791-115">-EndpointName</span></span>
<span data-ttu-id="b7791-116">엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7791-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="b7791-117">엔드포인트의 이름은 엔드포인트의 호스트 이름이 아닌 경우</span><span class="sxs-lookup"><span data-stu-id="b7791-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="b7791-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b7791-118">-ProfileName</span></span>
<span data-ttu-id="b7791-119">엔드포인트가 속한 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7791-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b7791-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7791-120">-ResourceGroupName</span></span>
<span data-ttu-id="b7791-121">엔드포인트가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7791-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b7791-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7791-122">CommonParameters</span></span>
<span data-ttu-id="b7791-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7791-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7791-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7791-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7791-125">입력</span><span class="sxs-lookup"><span data-stu-id="b7791-125">INPUTS</span></span>

### <span data-ttu-id="b7791-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="b7791-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="b7791-127">출력</span><span class="sxs-lookup"><span data-stu-id="b7791-127">OUTPUTS</span></span>

### <span data-ttu-id="b7791-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7791-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="b7791-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7791-129">NOTES</span></span>

## <span data-ttu-id="b7791-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7791-130">RELATED LINKS</span></span>

[<span data-ttu-id="b7791-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7791-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="b7791-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7791-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="b7791-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7791-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="b7791-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7791-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="b7791-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7791-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


