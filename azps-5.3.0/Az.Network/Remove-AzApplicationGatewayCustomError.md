---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378799"
---
# <span data-ttu-id="14d82-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14d82-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="14d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14d82-102">SYNOPSIS</span></span>
<span data-ttu-id="14d82-103">애플리케이션 게이트웨이에서 사용자 지정 오류를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="14d82-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="14d82-104">구문</span><span class="sxs-lookup"><span data-stu-id="14d82-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14d82-105">설명</span><span class="sxs-lookup"><span data-stu-id="14d82-105">DESCRIPTION</span></span>
<span data-ttu-id="14d82-106">**Remove-AzApplicationGatewayCustomError** cmdlet은 애플리케이션 게이트웨이에서 사용자 지정 오류를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="14d82-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="14d82-107">예제</span><span class="sxs-lookup"><span data-stu-id="14d82-107">EXAMPLES</span></span>

### <span data-ttu-id="14d82-108">예제 1: 애플리케이션 게이트웨이에서 사용자 지정 오류를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="14d82-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="14d82-109">이 명령은 애플리케이션 게이트웨이에서 http 상태 코드 502의 사용자 지정 $appgw 업데이트된 게이트웨이를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="14d82-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="14d82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14d82-110">PARAMETERS</span></span>

### <span data-ttu-id="14d82-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14d82-111">-ApplicationGateway</span></span>
<span data-ttu-id="14d82-112">The Application Gateway</span><span class="sxs-lookup"><span data-stu-id="14d82-112">The Application Gateway</span></span>

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

### <span data-ttu-id="14d82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d82-113">-DefaultProfile</span></span>
<span data-ttu-id="14d82-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14d82-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14d82-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="14d82-115">-StatusCode</span></span>
<span data-ttu-id="14d82-116">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="14d82-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="14d82-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d82-117">CommonParameters</span></span>
<span data-ttu-id="14d82-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14d82-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d82-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="14d82-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d82-120">입력</span><span class="sxs-lookup"><span data-stu-id="14d82-120">INPUTS</span></span>

### <span data-ttu-id="14d82-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14d82-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14d82-122">출력</span><span class="sxs-lookup"><span data-stu-id="14d82-122">OUTPUTS</span></span>

### <span data-ttu-id="14d82-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14d82-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="14d82-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14d82-124">NOTES</span></span>

## <span data-ttu-id="14d82-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14d82-125">RELATED LINKS</span></span>

[<span data-ttu-id="14d82-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14d82-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="14d82-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14d82-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="14d82-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14d82-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="14d82-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14d82-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
