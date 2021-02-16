---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192012"
---
# <span data-ttu-id="193b3-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="193b3-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="193b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="193b3-102">SYNOPSIS</span></span>
<span data-ttu-id="193b3-103">Application Gateway에서 기존 리디렉션 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="193b3-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="193b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="193b3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="193b3-105">설명</span><span class="sxs-lookup"><span data-stu-id="193b3-105">DESCRIPTION</span></span>
<span data-ttu-id="193b3-106">**Get-AzApplicationGatewayRedirectConfiguration** cmdlet은 Application Gateway에서 기존 리디렉션 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="193b3-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="193b3-107">예제</span><span class="sxs-lookup"><span data-stu-id="193b3-107">EXAMPLES</span></span>

### <span data-ttu-id="193b3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="193b3-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="193b3-109">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 사용하여 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="193b3-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="193b3-110">두 번째 명령은 애플리케이션이라는 변수에 저장된 Application Gateway에서 Redirect01이라는 리디렉션 구성을 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="193b3-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="193b3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="193b3-111">PARAMETERS</span></span>

### <span data-ttu-id="193b3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="193b3-112">-ApplicationGateway</span></span>
<span data-ttu-id="193b3-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="193b3-113">The applicationGateway</span></span>

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

### <span data-ttu-id="193b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="193b3-114">-DefaultProfile</span></span>
<span data-ttu-id="193b3-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="193b3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="193b3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="193b3-116">-Name</span></span>
<span data-ttu-id="193b3-117">요청 라우팅 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="193b3-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="193b3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="193b3-118">CommonParameters</span></span>
<span data-ttu-id="193b3-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="193b3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="193b3-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="193b3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="193b3-121">입력</span><span class="sxs-lookup"><span data-stu-id="193b3-121">INPUTS</span></span>

### <span data-ttu-id="193b3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="193b3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="193b3-123">출력</span><span class="sxs-lookup"><span data-stu-id="193b3-123">OUTPUTS</span></span>

### <span data-ttu-id="193b3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="193b3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="193b3-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="193b3-125">NOTES</span></span>

## <span data-ttu-id="193b3-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="193b3-126">RELATED LINKS</span></span>

[<span data-ttu-id="193b3-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="193b3-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="193b3-128">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="193b3-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="193b3-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="193b3-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="193b3-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="193b3-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
