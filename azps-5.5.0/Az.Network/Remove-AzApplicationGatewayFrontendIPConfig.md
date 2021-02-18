---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d376bc1e70d0441f139b64c19466a88daf6877c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206645"
---
# <span data-ttu-id="25753-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="25753-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="25753-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25753-102">SYNOPSIS</span></span>
<span data-ttu-id="25753-103">애플리케이션 게이트웨이에서 프런트 엔드 IP 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25753-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="25753-104">구문</span><span class="sxs-lookup"><span data-stu-id="25753-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25753-105">설명</span><span class="sxs-lookup"><span data-stu-id="25753-105">DESCRIPTION</span></span>
<span data-ttu-id="25753-106">**Remove-AzApplicationGatewayFrontendIPConfig** cmdlet은 Azure 애플리케이션 게이트웨이에서 프런트 엔드 IP를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25753-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="25753-107">예제</span><span class="sxs-lookup"><span data-stu-id="25753-107">EXAMPLES</span></span>

### <span data-ttu-id="25753-108">예제 1: 프런트 엔드 IP 구성 제거</span><span class="sxs-lookup"><span data-stu-id="25753-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="25753-109">첫 번째 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이를 사용하여 애플리케이션 $AppGw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="25753-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="25753-110">두 번째 명령은 애플리케이션 게이트웨이에서 FrontEndIP02라는 프런트 엔드 IP 구성을 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="25753-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="25753-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25753-111">PARAMETERS</span></span>

### <span data-ttu-id="25753-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25753-112">-ApplicationGateway</span></span>
<span data-ttu-id="25753-113">프런트 엔드 IP 구성을 제거할 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25753-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="25753-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25753-114">-DefaultProfile</span></span>
<span data-ttu-id="25753-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25753-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25753-116">-Name</span><span class="sxs-lookup"><span data-stu-id="25753-116">-Name</span></span>
<span data-ttu-id="25753-117">제거할 프런트 엔드 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25753-117">Specifies the name of a front-end IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25753-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25753-118">CommonParameters</span></span>
<span data-ttu-id="25753-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25753-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25753-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25753-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25753-121">입력</span><span class="sxs-lookup"><span data-stu-id="25753-121">INPUTS</span></span>

### <span data-ttu-id="25753-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25753-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="25753-123">출력</span><span class="sxs-lookup"><span data-stu-id="25753-123">OUTPUTS</span></span>

### <span data-ttu-id="25753-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25753-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="25753-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25753-125">NOTES</span></span>

## <span data-ttu-id="25753-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25753-126">RELATED LINKS</span></span>

[<span data-ttu-id="25753-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="25753-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="25753-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="25753-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="25753-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="25753-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="25753-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="25753-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


