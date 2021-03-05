---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: f82882a4975c2f873362ece62f6eac9e6b7a53a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993939"
---
# <span data-ttu-id="4d47c-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d47c-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4d47c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d47c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d47c-103">백던드 서버 풀에 대한 URL 경로 매핑 배열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d47c-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4d47c-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d47c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d47c-105">설명</span><span class="sxs-lookup"><span data-stu-id="4d47c-105">DESCRIPTION</span></span>
<span data-ttu-id="4d47c-106">**Get-AzApplicationGatewayURLPathMapConfig** cmdlet은 백END 서버 풀에 대한 URL 경로 매핑 배열을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="4d47c-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4d47c-107">예제</span><span class="sxs-lookup"><span data-stu-id="4d47c-107">EXAMPLES</span></span>

### <span data-ttu-id="4d47c-108">예제 1: URL 경로 맵 구성을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4d47c-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="4d47c-109">이 명령은 게이트웨이라는 애플리케이션 게이트웨이에 있는 백end 서버에서 URL 경로 맵 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d47c-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="4d47c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4d47c-110">PARAMETERS</span></span>

### <span data-ttu-id="4d47c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d47c-111">-ApplicationGateway</span></span>
<span data-ttu-id="4d47c-112">이 cmdlet에서 URL 경로 맵 구성을 얻을 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d47c-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d47c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d47c-113">-DefaultProfile</span></span>
<span data-ttu-id="4d47c-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d47c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d47c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4d47c-115">-Name</span></span>
<span data-ttu-id="4d47c-116">이 cmdlet에서 경로 맵 구성을 얻을 URL 경로 맵 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d47c-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="4d47c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d47c-117">CommonParameters</span></span>
<span data-ttu-id="4d47c-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d47c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d47c-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d47c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d47c-120">입력</span><span class="sxs-lookup"><span data-stu-id="4d47c-120">INPUTS</span></span>

### <span data-ttu-id="4d47c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d47c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d47c-122">출력</span><span class="sxs-lookup"><span data-stu-id="4d47c-122">OUTPUTS</span></span>

### <span data-ttu-id="4d47c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="4d47c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="4d47c-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d47c-124">NOTES</span></span>

## <span data-ttu-id="4d47c-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d47c-125">RELATED LINKS</span></span>

[<span data-ttu-id="4d47c-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d47c-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4d47c-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d47c-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4d47c-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d47c-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4d47c-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d47c-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


