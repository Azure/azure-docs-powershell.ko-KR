---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c1c630c39039d39b1957ccab78bb96d8f085176c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341673"
---
# <span data-ttu-id="35e01-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35e01-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="35e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35e01-102">SYNOPSIS</span></span>
<span data-ttu-id="35e01-103">애플리케이션 게이트웨이에서 요청 라우팅 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="35e01-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="35e01-104">구문</span><span class="sxs-lookup"><span data-stu-id="35e01-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35e01-105">설명</span><span class="sxs-lookup"><span data-stu-id="35e01-105">DESCRIPTION</span></span>
<span data-ttu-id="35e01-106">**Remove-AzApplicationGatewayRequestRoutingRule** cmdlet은 Azure 애플리케이션 게이트웨이에서 요청 라우팅 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="35e01-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="35e01-107">예제</span><span class="sxs-lookup"><span data-stu-id="35e01-107">EXAMPLES</span></span>

### <span data-ttu-id="35e01-108">예제 1: 애플리케이션 게이트웨이에서 요청 라우팅 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="35e01-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="35e01-109">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="35e01-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="35e01-110">두 번째 명령은 규칙에 저장된 애플리케이션 게이트웨이에서 Rule02라는 요청 라우팅 규칙을 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="35e01-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="35e01-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35e01-111">PARAMETERS</span></span>

### <span data-ttu-id="35e01-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35e01-112">-ApplicationGateway</span></span>
<span data-ttu-id="35e01-113">요청 라우팅 규칙을 제거할 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="35e01-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="35e01-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e01-114">-DefaultProfile</span></span>
<span data-ttu-id="35e01-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35e01-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35e01-116">-Name</span><span class="sxs-lookup"><span data-stu-id="35e01-116">-Name</span></span>
<span data-ttu-id="35e01-117">이 cmdlet이 제거되는 요청 라우팅 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="35e01-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="35e01-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e01-118">CommonParameters</span></span>
<span data-ttu-id="35e01-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="35e01-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e01-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35e01-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e01-121">입력</span><span class="sxs-lookup"><span data-stu-id="35e01-121">INPUTS</span></span>

### <span data-ttu-id="35e01-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35e01-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="35e01-123">출력</span><span class="sxs-lookup"><span data-stu-id="35e01-123">OUTPUTS</span></span>

### <span data-ttu-id="35e01-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35e01-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="35e01-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="35e01-125">NOTES</span></span>

## <span data-ttu-id="35e01-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35e01-126">RELATED LINKS</span></span>

[<span data-ttu-id="35e01-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35e01-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="35e01-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35e01-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="35e01-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35e01-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="35e01-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35e01-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

