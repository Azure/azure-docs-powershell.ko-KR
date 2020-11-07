---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: df81af46023c1e28ecfe39cf880f45cd9b2319ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711264"
---
# <span data-ttu-id="2cebc-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2cebc-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="2cebc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cebc-102">SYNOPSIS</span></span>
<span data-ttu-id="2cebc-103">기존 응용 프로그램 게이트웨이에서 상태 프로브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cebc-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cebc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2cebc-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cebc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2cebc-105">DESCRIPTION</span></span>
<span data-ttu-id="2cebc-106">Remove-AzureRmApplicationGatewayProbeConfig cmdlet은 기존 응용 프로그램 게이트웨이에서 heath probe를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cebc-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="2cebc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2cebc-107">EXAMPLES</span></span>

### <span data-ttu-id="2cebc-108">예제 1: 기존 응용 프로그램 게이트웨이에서 상태 프로브 제거</span><span class="sxs-lookup"><span data-stu-id="2cebc-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="2cebc-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에서 Probe04 이라는 상태 프로브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cebc-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="2cebc-110">변수</span><span class="sxs-lookup"><span data-stu-id="2cebc-110">PARAMETERS</span></span>

### <span data-ttu-id="2cebc-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cebc-111">-ApplicationGateway</span></span>
<span data-ttu-id="2cebc-112">이 cmdlet이 프로브를 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cebc-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="2cebc-113">-이름</span><span class="sxs-lookup"><span data-stu-id="2cebc-113">-Name</span></span>
<span data-ttu-id="2cebc-114">이 cmdlet이 제거할 프로브 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cebc-114">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="2cebc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cebc-115">-DefaultProfile</span></span>
<span data-ttu-id="2cebc-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2cebc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cebc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cebc-117">CommonParameters</span></span>
<span data-ttu-id="2cebc-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cebc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cebc-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cebc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cebc-120">입력</span><span class="sxs-lookup"><span data-stu-id="2cebc-120">INPUTS</span></span>

### <span data-ttu-id="2cebc-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cebc-121">PSApplicationGateway</span></span>
<span data-ttu-id="2cebc-122">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cebc-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="2cebc-123">출력</span><span class="sxs-lookup"><span data-stu-id="2cebc-123">OUTPUTS</span></span>

### <span data-ttu-id="2cebc-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cebc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2cebc-125">상속자</span><span class="sxs-lookup"><span data-stu-id="2cebc-125">NOTES</span></span>

## <span data-ttu-id="2cebc-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2cebc-126">RELATED LINKS</span></span>

[<span data-ttu-id="2cebc-127">기존 응용 프로그램 게이트웨이에서 프로브 제거</span><span class="sxs-lookup"><span data-stu-id="2cebc-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="2cebc-128">추가-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2cebc-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2cebc-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2cebc-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2cebc-130">새로운 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2cebc-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2cebc-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2cebc-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

