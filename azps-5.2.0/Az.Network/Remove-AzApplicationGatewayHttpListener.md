---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 81b750188a85add491e519c023c765f302e31dea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323469"
---
# <span data-ttu-id="fd4bd-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fd4bd-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="fd4bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4bd-103">애플리케이션 게이트웨이에서 HTTP 수신기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4bd-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="fd4bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd4bd-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd4bd-105">설명</span><span class="sxs-lookup"><span data-stu-id="fd4bd-105">DESCRIPTION</span></span>
<span data-ttu-id="fd4bd-106">**Remove-AzApplicationGatewayHttpListener** cmdlet은 Azure 애플리케이션 게이트웨이에서 HTTP 수신기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4bd-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="fd4bd-107">예제</span><span class="sxs-lookup"><span data-stu-id="fd4bd-107">EXAMPLES</span></span>

### <span data-ttu-id="fd4bd-108">예제 1: 애플리케이션 게이트웨이 HTTP 수신기 제거</span><span class="sxs-lookup"><span data-stu-id="fd4bd-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="fd4bd-109">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4bd-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fd4bd-110">두 번째 명령은 수신기 이름이 Listener02인 HTTP 수신기를 로컬에 저장된 애플리케이션 게이트웨이에서 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fd4bd-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="fd4bd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd4bd-111">PARAMETERS</span></span>

### <span data-ttu-id="fd4bd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd4bd-112">-ApplicationGateway</span></span>
<span data-ttu-id="fd4bd-113">HTTP 수신기를 제거할 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4bd-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="fd4bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4bd-114">-DefaultProfile</span></span>
<span data-ttu-id="fd4bd-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd4bd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd4bd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fd4bd-116">-Name</span></span>
<span data-ttu-id="fd4bd-117">이 cmdlet이 제거하는 HTTP 수신기 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4bd-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fd4bd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4bd-118">CommonParameters</span></span>
<span data-ttu-id="fd4bd-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4bd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4bd-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fd4bd-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4bd-121">입력</span><span class="sxs-lookup"><span data-stu-id="fd4bd-121">INPUTS</span></span>

### <span data-ttu-id="fd4bd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd4bd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fd4bd-123">출력</span><span class="sxs-lookup"><span data-stu-id="fd4bd-123">OUTPUTS</span></span>

### <span data-ttu-id="fd4bd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fd4bd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="fd4bd-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd4bd-125">NOTES</span></span>

## <span data-ttu-id="fd4bd-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd4bd-126">RELATED LINKS</span></span>

[<span data-ttu-id="fd4bd-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fd4bd-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="fd4bd-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fd4bd-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="fd4bd-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fd4bd-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="fd4bd-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fd4bd-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


