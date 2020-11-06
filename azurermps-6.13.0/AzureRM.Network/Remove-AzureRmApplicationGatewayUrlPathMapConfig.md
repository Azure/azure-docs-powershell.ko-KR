---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 68676c05757a58f2c1094e36338d17a52de6b040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527827"
---
# <span data-ttu-id="4ac28-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4ac28-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4ac28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ac28-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac28-103">백 엔드 서버 풀에 대 한 URL 경로 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ac28-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ac28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ac28-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ac28-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4ac28-105">DESCRIPTION</span></span>
<span data-ttu-id="4ac28-106">**AzureRmApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ac28-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4ac28-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4ac28-107">EXAMPLES</span></span>

## <span data-ttu-id="4ac28-108">변수</span><span class="sxs-lookup"><span data-stu-id="4ac28-108">PARAMETERS</span></span>

### <span data-ttu-id="4ac28-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ac28-109">-ApplicationGateway</span></span>
<span data-ttu-id="4ac28-110">이 cmdlet이 URL 경로 맵 구성을 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ac28-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="4ac28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac28-111">-DefaultProfile</span></span>
<span data-ttu-id="4ac28-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac28-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ac28-113">-이름</span><span class="sxs-lookup"><span data-stu-id="4ac28-113">-Name</span></span>
<span data-ttu-id="4ac28-114">이 cmdlet이 백 엔드 서버에서 제거 하는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ac28-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac28-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac28-115">CommonParameters</span></span>
<span data-ttu-id="4ac28-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ac28-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac28-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ac28-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac28-118">입력</span><span class="sxs-lookup"><span data-stu-id="4ac28-118">INPUTS</span></span>

### <span data-ttu-id="4ac28-119">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ac28-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="4ac28-120">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4ac28-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="4ac28-121">출력</span><span class="sxs-lookup"><span data-stu-id="4ac28-121">OUTPUTS</span></span>

### <span data-ttu-id="4ac28-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ac28-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ac28-123">상속자</span><span class="sxs-lookup"><span data-stu-id="4ac28-123">NOTES</span></span>

## <span data-ttu-id="4ac28-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ac28-124">RELATED LINKS</span></span>

[<span data-ttu-id="4ac28-125">추가-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4ac28-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4ac28-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4ac28-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4ac28-127">새로운 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4ac28-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4ac28-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4ac28-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


