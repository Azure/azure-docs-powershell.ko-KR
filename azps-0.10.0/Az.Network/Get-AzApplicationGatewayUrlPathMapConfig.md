---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 92d970d87b79b1a392b6da73c567d6e8445cfd90
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875608"
---
# <span data-ttu-id="08c2d-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="08c2d-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="08c2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="08c2d-103">백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08c2d-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="08c2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08c2d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08c2d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="08c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="08c2d-106">**AzApplicationGatewayURLPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08c2d-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="08c2d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="08c2d-107">EXAMPLES</span></span>

### <span data-ttu-id="08c2d-108">예제 1: URL 경로 맵 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="08c2d-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="08c2d-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에 있는 백 엔드 서버에서 URL 경로 맵 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08c2d-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="08c2d-110">변수</span><span class="sxs-lookup"><span data-stu-id="08c2d-110">PARAMETERS</span></span>

### <span data-ttu-id="08c2d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08c2d-111">-ApplicationGateway</span></span>
<span data-ttu-id="08c2d-112">이 cmdlet이 URL 경로 맵 구성을 가져오는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08c2d-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08c2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c2d-113">-DefaultProfile</span></span>
<span data-ttu-id="08c2d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08c2d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08c2d-115">-이름</span><span class="sxs-lookup"><span data-stu-id="08c2d-115">-Name</span></span>
<span data-ttu-id="08c2d-116">이 cmdlet이 경로 맵 구성을 가져올 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08c2d-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08c2d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c2d-117">CommonParameters</span></span>
<span data-ttu-id="08c2d-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08c2d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c2d-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08c2d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c2d-120">입력</span><span class="sxs-lookup"><span data-stu-id="08c2d-120">INPUTS</span></span>

### <span data-ttu-id="08c2d-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08c2d-121">PSApplicationGateway</span></span>
<span data-ttu-id="08c2d-122">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="08c2d-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="08c2d-123">출력</span><span class="sxs-lookup"><span data-stu-id="08c2d-123">OUTPUTS</span></span>

### <span data-ttu-id="08c2d-124">PSApplicationGatewayUrlPathMap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="08c2d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="08c2d-125">System.webserver. t e 1.aspx ' 1 [Microsoft Azure. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="08c2d-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="08c2d-126">상속자</span><span class="sxs-lookup"><span data-stu-id="08c2d-126">NOTES</span></span>

## <span data-ttu-id="08c2d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08c2d-127">RELATED LINKS</span></span>

[<span data-ttu-id="08c2d-128">추가-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="08c2d-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="08c2d-129">새로운 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="08c2d-129">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="08c2d-130">제거-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="08c2d-130">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="08c2d-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="08c2d-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


