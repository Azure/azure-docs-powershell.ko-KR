---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: f542783ce1edcebf0c0c4e70116423836ddff736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529494"
---
# <span data-ttu-id="99c76-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="99c76-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="99c76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99c76-102">SYNOPSIS</span></span>
<span data-ttu-id="99c76-103">기존 응용 프로그램 게이트웨이에서 리디렉션 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99c76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99c76-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99c76-105">설명은</span><span class="sxs-lookup"><span data-stu-id="99c76-105">DESCRIPTION</span></span>
<span data-ttu-id="99c76-106">**AzureRmApplicationGatewayRedirectConfiguration** cmdlet은 기존 응용 프로그램 게이트웨이에서 리디렉션 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="99c76-107">예제의</span><span class="sxs-lookup"><span data-stu-id="99c76-107">EXAMPLES</span></span>

### <span data-ttu-id="99c76-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="99c76-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="99c76-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="99c76-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 Redirect01 이라는 리디렉션 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="99c76-111">변수</span><span class="sxs-lookup"><span data-stu-id="99c76-111">PARAMETERS</span></span>

### <span data-ttu-id="99c76-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99c76-112">-ApplicationGateway</span></span>
<span data-ttu-id="99c76-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99c76-113">The applicationGateway</span></span>

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

### <span data-ttu-id="99c76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c76-114">-DefaultProfile</span></span>
<span data-ttu-id="99c76-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99c76-116">-이름</span><span class="sxs-lookup"><span data-stu-id="99c76-116">-Name</span></span>
<span data-ttu-id="99c76-117">리디렉션 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="99c76-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c76-118">CommonParameters</span></span>
<span data-ttu-id="99c76-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c76-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99c76-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c76-121">입력</span><span class="sxs-lookup"><span data-stu-id="99c76-121">INPUTS</span></span>

### <span data-ttu-id="99c76-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99c76-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="99c76-123">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="99c76-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="99c76-124">출력</span><span class="sxs-lookup"><span data-stu-id="99c76-124">OUTPUTS</span></span>

### <span data-ttu-id="99c76-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99c76-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99c76-126">상속자</span><span class="sxs-lookup"><span data-stu-id="99c76-126">NOTES</span></span>

## <span data-ttu-id="99c76-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99c76-127">RELATED LINKS</span></span>
