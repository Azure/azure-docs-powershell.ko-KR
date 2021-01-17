---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326332"
---
# <span data-ttu-id="913a0-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="913a0-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="913a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="913a0-102">SYNOPSIS</span></span>
<span data-ttu-id="913a0-103">애플리케이션 게이트웨이에서 사용자 지정 오류를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="913a0-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="913a0-104">구문</span><span class="sxs-lookup"><span data-stu-id="913a0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="913a0-105">설명</span><span class="sxs-lookup"><span data-stu-id="913a0-105">DESCRIPTION</span></span>
<span data-ttu-id="913a0-106">**Get-AzApplicationGatewayCustomError** cmdlet은 애플리케이션 게이트웨이에서 사용자 지정 오류를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="913a0-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="913a0-107">예제</span><span class="sxs-lookup"><span data-stu-id="913a0-107">EXAMPLES</span></span>

### <span data-ttu-id="913a0-108">예제 1: 애플리케이션 게이트웨이에서 사용자 지정 오류 발생</span><span class="sxs-lookup"><span data-stu-id="913a0-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="913a0-109">이 명령은 애플리케이션 게이트웨이에서 http 상태 코드 502의 사용자 지정 오류를 $appgw.</span><span class="sxs-lookup"><span data-stu-id="913a0-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="913a0-110">예제 2: 애플리케이션 게이트웨이의 모든 사용자 지정 오류 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="913a0-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="913a0-111">이 명령은 애플리케이션 게이트웨이에서 모든 사용자 지정 오류 목록을 $appgw.</span><span class="sxs-lookup"><span data-stu-id="913a0-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="913a0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="913a0-112">PARAMETERS</span></span>

### <span data-ttu-id="913a0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="913a0-113">-ApplicationGateway</span></span>
<span data-ttu-id="913a0-114">The Application Gateway</span><span class="sxs-lookup"><span data-stu-id="913a0-114">The Application Gateway</span></span>

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

### <span data-ttu-id="913a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913a0-115">-DefaultProfile</span></span>
<span data-ttu-id="913a0-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="913a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="913a0-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="913a0-117">-StatusCode</span></span>
<span data-ttu-id="913a0-118">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="913a0-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913a0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913a0-119">CommonParameters</span></span>
<span data-ttu-id="913a0-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="913a0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913a0-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="913a0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913a0-122">입력</span><span class="sxs-lookup"><span data-stu-id="913a0-122">INPUTS</span></span>

### <span data-ttu-id="913a0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="913a0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="913a0-124">출력</span><span class="sxs-lookup"><span data-stu-id="913a0-124">OUTPUTS</span></span>

### <span data-ttu-id="913a0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="913a0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="913a0-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="913a0-126">NOTES</span></span>

## <span data-ttu-id="913a0-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="913a0-127">RELATED LINKS</span></span>

[<span data-ttu-id="913a0-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="913a0-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="913a0-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="913a0-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="913a0-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="913a0-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="913a0-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="913a0-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
