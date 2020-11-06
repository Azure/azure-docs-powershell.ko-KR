---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 2b35d3978859c65ec5219fe3e0208776d7dc7d68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535968"
---
# <span data-ttu-id="01d2e-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="01d2e-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="01d2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="01d2e-103">응용 프로그램 게이트웨이에서 기존 리디렉션 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="01d2e-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01d2e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01d2e-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01d2e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01d2e-105">DESCRIPTION</span></span>
<span data-ttu-id="01d2e-106">**Get-AzureRmApplicationGatewayRedirectConfiguration** Cmdlet은 응용 프로그램 게이트웨이에서 기존 리디렉션 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="01d2e-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="01d2e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="01d2e-107">EXAMPLES</span></span>

### <span data-ttu-id="01d2e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="01d2e-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="01d2e-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="01d2e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="01d2e-110">두 번째 명령은 $AppGW 이라는 변수에 저장 된 응용 프로그램 게이트웨이에서 Redirect01 이라는 리디렉션 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="01d2e-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="01d2e-111">변수</span><span class="sxs-lookup"><span data-stu-id="01d2e-111">PARAMETERS</span></span>

### <span data-ttu-id="01d2e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01d2e-112">-ApplicationGateway</span></span>
<span data-ttu-id="01d2e-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01d2e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="01d2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d2e-114">-DefaultProfile</span></span>
<span data-ttu-id="01d2e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01d2e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01d2e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="01d2e-116">-Name</span></span>
<span data-ttu-id="01d2e-117">요청 라우팅 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01d2e-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="01d2e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d2e-118">CommonParameters</span></span>
<span data-ttu-id="01d2e-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01d2e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d2e-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d2e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d2e-121">입력</span><span class="sxs-lookup"><span data-stu-id="01d2e-121">INPUTS</span></span>

### <span data-ttu-id="01d2e-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01d2e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="01d2e-123">출력</span><span class="sxs-lookup"><span data-stu-id="01d2e-123">OUTPUTS</span></span>

### <span data-ttu-id="01d2e-124">Microsoft. 네트워크. Psapplication게이트웨이 Redirectconfiguration</span><span class="sxs-lookup"><span data-stu-id="01d2e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="01d2e-125">4.1.0.0 ' 1 [[Microsoft Azure.]. 모델의 Psapplication게이트웨이 Redirectconfiguration, Microsoft Azure. Network, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="01d2e-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="01d2e-126">상속자</span><span class="sxs-lookup"><span data-stu-id="01d2e-126">NOTES</span></span>

## <span data-ttu-id="01d2e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01d2e-127">RELATED LINKS</span></span>

