---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 08637412afafe9220107e95dd3cb7dcc5154ba26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184220"
---
# <span data-ttu-id="3d76b-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3d76b-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="3d76b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d76b-102">SYNOPSIS</span></span>
<span data-ttu-id="3d76b-103">애플리케이션 게이트웨이에 대한 프런트 엔드 포트를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d76b-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="3d76b-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d76b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d76b-105">설명</span><span class="sxs-lookup"><span data-stu-id="3d76b-105">DESCRIPTION</span></span>
<span data-ttu-id="3d76b-106">**Set-AzApplicationGatewayFrontendPort** cmdlet은 애플리케이션 게이트웨이에 대한 프런트 엔드 포트를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d76b-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="3d76b-107">예제</span><span class="sxs-lookup"><span data-stu-id="3d76b-107">EXAMPLES</span></span>

### <span data-ttu-id="3d76b-108">예제 1: 애플리케이션 게이트웨이 프런트 엔드 포트를 80으로 설정</span><span class="sxs-lookup"><span data-stu-id="3d76b-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="3d76b-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3d76b-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3d76b-110">두 번째 명령은 FrontEndPort01이라는 프런트 엔드 포트에 $AppGw 포트 80을 사용하기 위해 게이트웨이의 게이트웨이를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d76b-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="3d76b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d76b-111">PARAMETERS</span></span>

### <span data-ttu-id="3d76b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d76b-112">-ApplicationGateway</span></span>
<span data-ttu-id="3d76b-113">이 cmdlet이 프런트 엔드 포트를 연결한 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d76b-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="3d76b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d76b-114">-DefaultProfile</span></span>
<span data-ttu-id="3d76b-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d76b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d76b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3d76b-116">-Name</span></span>
<span data-ttu-id="3d76b-117">수정할 프런트 엔드 포트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d76b-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="3d76b-118">-Port</span><span class="sxs-lookup"><span data-stu-id="3d76b-118">-Port</span></span>
<span data-ttu-id="3d76b-119">프런트 엔드 포트에 사용할 포트 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d76b-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d76b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d76b-120">CommonParameters</span></span>
<span data-ttu-id="3d76b-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d76b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d76b-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3d76b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d76b-123">입력</span><span class="sxs-lookup"><span data-stu-id="3d76b-123">INPUTS</span></span>

### <span data-ttu-id="3d76b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d76b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3d76b-125">출력</span><span class="sxs-lookup"><span data-stu-id="3d76b-125">OUTPUTS</span></span>

### <span data-ttu-id="3d76b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d76b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3d76b-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d76b-127">NOTES</span></span>

## <span data-ttu-id="3d76b-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d76b-128">RELATED LINKS</span></span>

[<span data-ttu-id="3d76b-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3d76b-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="3d76b-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3d76b-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="3d76b-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3d76b-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="3d76b-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3d76b-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
