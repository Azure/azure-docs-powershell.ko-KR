---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048883"
---
# <span data-ttu-id="24243-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="24243-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="24243-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24243-102">SYNOPSIS</span></span>
<span data-ttu-id="24243-103">기존 응용 프로그램 게이트웨이에서 상태 프로브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24243-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="24243-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24243-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24243-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24243-105">DESCRIPTION</span></span>
<span data-ttu-id="24243-106">Remove-AzApplicationGatewayProbeConfig cmdlet은 기존 응용 프로그램 게이트웨이에서 heath probe를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24243-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="24243-107">예제의</span><span class="sxs-lookup"><span data-stu-id="24243-107">EXAMPLES</span></span>

### <span data-ttu-id="24243-108">예제 1: 기존 응용 프로그램 게이트웨이에서 상태 프로브 제거</span><span class="sxs-lookup"><span data-stu-id="24243-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="24243-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에서 Probe04 이라는 상태 프로브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24243-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="24243-110">변수</span><span class="sxs-lookup"><span data-stu-id="24243-110">PARAMETERS</span></span>

### <span data-ttu-id="24243-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24243-111">-ApplicationGateway</span></span>
<span data-ttu-id="24243-112">이 cmdlet이 프로브를 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24243-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="24243-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24243-113">-DefaultProfile</span></span>
<span data-ttu-id="24243-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24243-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24243-115">-이름</span><span class="sxs-lookup"><span data-stu-id="24243-115">-Name</span></span>
<span data-ttu-id="24243-116">이 cmdlet이 제거할 프로브 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24243-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="24243-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24243-117">CommonParameters</span></span>
<span data-ttu-id="24243-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24243-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24243-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24243-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24243-120">입력</span><span class="sxs-lookup"><span data-stu-id="24243-120">INPUTS</span></span>

### <span data-ttu-id="24243-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24243-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24243-122">출력</span><span class="sxs-lookup"><span data-stu-id="24243-122">OUTPUTS</span></span>

### <span data-ttu-id="24243-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24243-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24243-124">상속자</span><span class="sxs-lookup"><span data-stu-id="24243-124">NOTES</span></span>

## <span data-ttu-id="24243-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24243-125">RELATED LINKS</span></span>

[<span data-ttu-id="24243-126">기존 응용 프로그램 게이트웨이에서 프로브 제거</span><span class="sxs-lookup"><span data-stu-id="24243-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="24243-127">추가-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="24243-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="24243-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="24243-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="24243-129">새로운 AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="24243-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="24243-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="24243-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

