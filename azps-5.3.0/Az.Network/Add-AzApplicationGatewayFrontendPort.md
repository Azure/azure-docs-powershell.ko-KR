---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9cd7cd0b859ff806b084ebfe1c76e07aed3a7c43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380325"
---
# <span data-ttu-id="d6b69-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d6b69-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d6b69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6b69-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b69-103">애플리케이션 게이트웨이에 프런트 엔드 포트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b69-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="d6b69-104">구문</span><span class="sxs-lookup"><span data-stu-id="d6b69-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6b69-105">설명</span><span class="sxs-lookup"><span data-stu-id="d6b69-105">DESCRIPTION</span></span>
<span data-ttu-id="d6b69-106">**Add-AzApplicationGatewayFrontendPort** cmdlet은 애플리케이션 게이트웨이에 프런트 엔드 포트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b69-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="d6b69-107">예제</span><span class="sxs-lookup"><span data-stu-id="d6b69-107">EXAMPLES</span></span>

### <span data-ttu-id="d6b69-108">예제 1: 애플리케이션 게이트웨이에 프런트 엔드 포트 추가</span><span class="sxs-lookup"><span data-stu-id="d6b69-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="d6b69-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b69-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d6b69-110">두 번째 명령은 포트 80을 게이트웨이에 저장된 애플리케이션 게이트웨이의 프런트 엔드 포트로 $AppGw FrontEndPort01의 이름을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b69-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="d6b69-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6b69-111">PARAMETERS</span></span>

### <span data-ttu-id="d6b69-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6b69-112">-ApplicationGateway</span></span>
<span data-ttu-id="d6b69-113">이 cmdlet이 프런트 엔드 포트를 추가할 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b69-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="d6b69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b69-114">-DefaultProfile</span></span>
<span data-ttu-id="d6b69-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6b69-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6b69-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d6b69-116">-Name</span></span>
<span data-ttu-id="d6b69-117">프런트 엔드 포트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b69-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="d6b69-118">-Port</span><span class="sxs-lookup"><span data-stu-id="d6b69-118">-Port</span></span>
<span data-ttu-id="d6b69-119">포트 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b69-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="d6b69-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b69-120">CommonParameters</span></span>
<span data-ttu-id="d6b69-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b69-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b69-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d6b69-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b69-123">입력</span><span class="sxs-lookup"><span data-stu-id="d6b69-123">INPUTS</span></span>

### <span data-ttu-id="d6b69-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6b69-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d6b69-125">출력</span><span class="sxs-lookup"><span data-stu-id="d6b69-125">OUTPUTS</span></span>

### <span data-ttu-id="d6b69-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6b69-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d6b69-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d6b69-127">NOTES</span></span>

## <span data-ttu-id="d6b69-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6b69-128">RELATED LINKS</span></span>

[<span data-ttu-id="d6b69-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d6b69-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d6b69-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d6b69-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d6b69-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d6b69-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d6b69-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d6b69-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


