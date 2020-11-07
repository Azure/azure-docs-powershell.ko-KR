---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 62d58803f4b1c7cae39e41e5f903cbfaf022e632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700642"
---
# <span data-ttu-id="97b51-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="97b51-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="97b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97b51-102">SYNOPSIS</span></span>
<span data-ttu-id="97b51-103">응용 프로그램 게이트웨이에서 기존 상태 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97b51-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="97b51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97b51-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97b51-105">설명은</span><span class="sxs-lookup"><span data-stu-id="97b51-105">DESCRIPTION</span></span>
<span data-ttu-id="97b51-106">Get-AzApplicationGatewayProbeConfig cmdlet은 응용 프로그램 게이트웨이에서 기존 상태 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97b51-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="97b51-107">예제의</span><span class="sxs-lookup"><span data-stu-id="97b51-107">EXAMPLES</span></span>

### <span data-ttu-id="97b51-108">예제 1: 응용 프로그램 게이트웨이에서 기존 프로브 가져오기</span><span class="sxs-lookup"><span data-stu-id="97b51-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="97b51-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에서 Probe02 이라는 상태 프로브를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97b51-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="97b51-110">변수</span><span class="sxs-lookup"><span data-stu-id="97b51-110">PARAMETERS</span></span>

### <span data-ttu-id="97b51-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97b51-111">-ApplicationGateway</span></span>
<span data-ttu-id="97b51-112">이 cmdlet이 프로브 구성을 가져오는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97b51-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="97b51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b51-113">-DefaultProfile</span></span>
<span data-ttu-id="97b51-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97b51-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97b51-115">-이름</span><span class="sxs-lookup"><span data-stu-id="97b51-115">-Name</span></span>
<span data-ttu-id="97b51-116">프로브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97b51-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="97b51-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b51-117">CommonParameters</span></span>
<span data-ttu-id="97b51-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97b51-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b51-119">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="97b51-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b51-120">입력</span><span class="sxs-lookup"><span data-stu-id="97b51-120">INPUTS</span></span>

### <span data-ttu-id="97b51-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97b51-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97b51-122">출력</span><span class="sxs-lookup"><span data-stu-id="97b51-122">OUTPUTS</span></span>

### <span data-ttu-id="97b51-123">Microsoft. \*. m i m a. 모델. m i m a 검색</span><span class="sxs-lookup"><span data-stu-id="97b51-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="97b51-124">상속자</span><span class="sxs-lookup"><span data-stu-id="97b51-124">NOTES</span></span>

## <span data-ttu-id="97b51-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97b51-125">RELATED LINKS</span></span>

[<span data-ttu-id="97b51-126">기존 application gateway에 프로브 추가</span><span class="sxs-lookup"><span data-stu-id="97b51-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="97b51-127">추가-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="97b51-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="97b51-128">새로운 AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="97b51-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="97b51-129">제거-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="97b51-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="97b51-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="97b51-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

