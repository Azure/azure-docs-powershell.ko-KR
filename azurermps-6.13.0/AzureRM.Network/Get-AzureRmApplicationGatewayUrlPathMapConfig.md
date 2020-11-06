---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: bcd1ec3e1f4dfdd62b8b22b798bad491c359a410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533371"
---
# <span data-ttu-id="86f55-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="86f55-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="86f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86f55-102">SYNOPSIS</span></span>
<span data-ttu-id="86f55-103">백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86f55-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86f55-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86f55-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86f55-105">설명은</span><span class="sxs-lookup"><span data-stu-id="86f55-105">DESCRIPTION</span></span>
<span data-ttu-id="86f55-106">**AzureRmApplicationGatewayURLPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86f55-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="86f55-107">예제의</span><span class="sxs-lookup"><span data-stu-id="86f55-107">EXAMPLES</span></span>

### <span data-ttu-id="86f55-108">예제 1: URL 경로 맵 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="86f55-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="86f55-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에 있는 백 엔드 서버에서 URL 경로 맵 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86f55-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="86f55-110">변수</span><span class="sxs-lookup"><span data-stu-id="86f55-110">PARAMETERS</span></span>

### <span data-ttu-id="86f55-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86f55-111">-ApplicationGateway</span></span>
<span data-ttu-id="86f55-112">이 cmdlet이 URL 경로 맵 구성을 가져오는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f55-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="86f55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f55-113">-DefaultProfile</span></span>
<span data-ttu-id="86f55-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86f55-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86f55-115">-이름</span><span class="sxs-lookup"><span data-stu-id="86f55-115">-Name</span></span>
<span data-ttu-id="86f55-116">이 cmdlet이 경로 맵 구성을 가져올 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f55-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="86f55-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f55-117">CommonParameters</span></span>
<span data-ttu-id="86f55-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f55-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f55-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86f55-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f55-120">입력</span><span class="sxs-lookup"><span data-stu-id="86f55-120">INPUTS</span></span>

### <span data-ttu-id="86f55-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86f55-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="86f55-122">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="86f55-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="86f55-123">출력</span><span class="sxs-lookup"><span data-stu-id="86f55-123">OUTPUTS</span></span>

### <span data-ttu-id="86f55-124">PSApplicationGatewayUrlPathMap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="86f55-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="86f55-125">상속자</span><span class="sxs-lookup"><span data-stu-id="86f55-125">NOTES</span></span>

## <span data-ttu-id="86f55-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86f55-126">RELATED LINKS</span></span>

[<span data-ttu-id="86f55-127">추가-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="86f55-127">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="86f55-128">새로운 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="86f55-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="86f55-129">제거-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="86f55-129">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="86f55-130">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="86f55-130">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


