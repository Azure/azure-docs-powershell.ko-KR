---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369097"
---
# <span data-ttu-id="049a6-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="049a6-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="049a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="049a6-102">SYNOPSIS</span></span>
<span data-ttu-id="049a6-103">기존 애플리케이션 게이트웨이에서 상태 프로브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="049a6-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="049a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="049a6-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="049a6-105">설명</span><span class="sxs-lookup"><span data-stu-id="049a6-105">DESCRIPTION</span></span>
<span data-ttu-id="049a6-106">이 Remove-AzApplicationGatewayProbeConfig cmdlet은 기존 애플리케이션 게이트웨이에서 열 프로브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="049a6-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="049a6-107">예제</span><span class="sxs-lookup"><span data-stu-id="049a6-107">EXAMPLES</span></span>

### <span data-ttu-id="049a6-108">예제 1: 기존 애플리케이션 게이트웨이에서 상태 프로브 제거</span><span class="sxs-lookup"><span data-stu-id="049a6-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="049a6-109">이 명령은 게이트웨이라는 애플리케이션 게이트웨이에서 Probe04라는 상태 프로브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="049a6-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="049a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="049a6-110">PARAMETERS</span></span>

### <span data-ttu-id="049a6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="049a6-111">-ApplicationGateway</span></span>
<span data-ttu-id="049a6-112">이 cmdlet이 프로브를 제거하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="049a6-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="049a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="049a6-113">-DefaultProfile</span></span>
<span data-ttu-id="049a6-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="049a6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="049a6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="049a6-115">-Name</span></span>
<span data-ttu-id="049a6-116">이 cmdlet이 제거되는 프로브의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="049a6-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="049a6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049a6-117">CommonParameters</span></span>
<span data-ttu-id="049a6-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="049a6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049a6-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="049a6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049a6-120">입력</span><span class="sxs-lookup"><span data-stu-id="049a6-120">INPUTS</span></span>

### <span data-ttu-id="049a6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="049a6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="049a6-122">출력</span><span class="sxs-lookup"><span data-stu-id="049a6-122">OUTPUTS</span></span>

### <span data-ttu-id="049a6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="049a6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="049a6-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="049a6-124">NOTES</span></span>

## <span data-ttu-id="049a6-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="049a6-125">RELATED LINKS</span></span>

[<span data-ttu-id="049a6-126">기존 애플리케이션 게이트웨이에서 프로브 제거</span><span class="sxs-lookup"><span data-stu-id="049a6-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="049a6-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="049a6-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="049a6-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="049a6-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="049a6-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="049a6-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="049a6-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="049a6-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

