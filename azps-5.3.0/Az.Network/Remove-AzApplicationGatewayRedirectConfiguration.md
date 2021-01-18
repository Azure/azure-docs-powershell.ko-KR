---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493184"
---
# <span data-ttu-id="f1b17-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1b17-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="f1b17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1b17-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b17-103">기존 Application Gateway에서 리디렉션 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f1b17-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="f1b17-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1b17-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1b17-105">설명</span><span class="sxs-lookup"><span data-stu-id="f1b17-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b17-106">**Remove-AzApplicationGatewayRedirectConfiguration** cmdlet은 기존 Application Gateway에서 리디렉션 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f1b17-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="f1b17-107">예제</span><span class="sxs-lookup"><span data-stu-id="f1b17-107">EXAMPLES</span></span>

### <span data-ttu-id="f1b17-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1b17-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="f1b17-109">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f1b17-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f1b17-110">두 번째 명령은 애플리케이션에 저장된 애플리케이션 게이트웨이에서 Redirect01이라는 리디렉션 구성을 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f1b17-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f1b17-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1b17-111">PARAMETERS</span></span>

### <span data-ttu-id="f1b17-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1b17-112">-ApplicationGateway</span></span>
<span data-ttu-id="f1b17-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1b17-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f1b17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b17-114">-DefaultProfile</span></span>
<span data-ttu-id="f1b17-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1b17-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1b17-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f1b17-116">-Name</span></span>
<span data-ttu-id="f1b17-117">리디렉션 구성의 이름</span><span class="sxs-lookup"><span data-stu-id="f1b17-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="f1b17-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b17-118">CommonParameters</span></span>
<span data-ttu-id="f1b17-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1b17-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b17-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f1b17-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b17-121">입력</span><span class="sxs-lookup"><span data-stu-id="f1b17-121">INPUTS</span></span>

### <span data-ttu-id="f1b17-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1b17-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1b17-123">출력</span><span class="sxs-lookup"><span data-stu-id="f1b17-123">OUTPUTS</span></span>

### <span data-ttu-id="f1b17-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1b17-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1b17-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1b17-125">NOTES</span></span>

## <span data-ttu-id="f1b17-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1b17-126">RELATED LINKS</span></span>

[<span data-ttu-id="f1b17-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1b17-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f1b17-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1b17-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f1b17-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1b17-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f1b17-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1b17-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
