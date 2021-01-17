---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369888"
---
# <span data-ttu-id="c1aef-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1aef-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c1aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1aef-102">SYNOPSIS</span></span>
<span data-ttu-id="c1aef-103">애플리케이션 게이트웨이에서 프런트 엔드 포트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1aef-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="c1aef-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1aef-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1aef-105">설명</span><span class="sxs-lookup"><span data-stu-id="c1aef-105">DESCRIPTION</span></span>
<span data-ttu-id="c1aef-106">**Remove-AzApplicationGatewayFrontendPort** cmdlet은 Azure 애플리케이션 게이트웨이에서 프런트 엔드 포트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1aef-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="c1aef-107">예제</span><span class="sxs-lookup"><span data-stu-id="c1aef-107">EXAMPLES</span></span>

### <span data-ttu-id="c1aef-108">예: 애플리케이션 게이트웨이에서 프런트 엔드 포트 제거</span><span class="sxs-lookup"><span data-stu-id="c1aef-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="c1aef-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 사용하여 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c1aef-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="c1aef-110">두 번째 명령은 애플리케이션 게이트웨이에서 FrontEndPort02라는 포트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1aef-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="c1aef-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1aef-111">PARAMETERS</span></span>

### <span data-ttu-id="c1aef-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1aef-112">-ApplicationGateway</span></span>
<span data-ttu-id="c1aef-113">프런트 엔드 포트를 제거할 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1aef-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="c1aef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1aef-114">-DefaultProfile</span></span>
<span data-ttu-id="c1aef-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1aef-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1aef-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c1aef-116">-Name</span></span>
<span data-ttu-id="c1aef-117">제거할 프런트 엔드 포트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1aef-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="c1aef-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1aef-118">CommonParameters</span></span>
<span data-ttu-id="c1aef-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1aef-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1aef-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c1aef-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1aef-121">입력</span><span class="sxs-lookup"><span data-stu-id="c1aef-121">INPUTS</span></span>

### <span data-ttu-id="c1aef-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1aef-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1aef-123">출력</span><span class="sxs-lookup"><span data-stu-id="c1aef-123">OUTPUTS</span></span>

### <span data-ttu-id="c1aef-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1aef-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1aef-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1aef-125">NOTES</span></span>

## <span data-ttu-id="c1aef-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1aef-126">RELATED LINKS</span></span>

[<span data-ttu-id="c1aef-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1aef-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c1aef-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1aef-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c1aef-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1aef-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c1aef-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1aef-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


