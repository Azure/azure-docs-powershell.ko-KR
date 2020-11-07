---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: cbe38933cb4c2c75b5219bf0deccc0b28052a61f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881449"
---
# <span data-ttu-id="28542-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="28542-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="28542-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28542-102">SYNOPSIS</span></span>
<span data-ttu-id="28542-103">응용 프로그램 게이트웨이에서 기존 상태 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28542-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28542-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28542-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28542-105">설명은</span><span class="sxs-lookup"><span data-stu-id="28542-105">DESCRIPTION</span></span>
<span data-ttu-id="28542-106">Get-AzureRmApplicationGatewayProbeConfig cmdlet은 응용 프로그램 게이트웨이에서 기존 상태 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28542-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="28542-107">예제의</span><span class="sxs-lookup"><span data-stu-id="28542-107">EXAMPLES</span></span>

### <span data-ttu-id="28542-108">예제 1: 응용 프로그램 게이트웨이에서 기존 프로브 가져오기</span><span class="sxs-lookup"><span data-stu-id="28542-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="28542-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에서 Probe02 이라는 상태 프로브를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28542-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="28542-110">변수</span><span class="sxs-lookup"><span data-stu-id="28542-110">PARAMETERS</span></span>

### <span data-ttu-id="28542-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28542-111">-ApplicationGateway</span></span>
<span data-ttu-id="28542-112">이 cmdlet이 프로브 구성을 가져오는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28542-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="28542-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28542-113">-DefaultProfile</span></span>
<span data-ttu-id="28542-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28542-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28542-115">-이름</span><span class="sxs-lookup"><span data-stu-id="28542-115">-Name</span></span>
<span data-ttu-id="28542-116">프로브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28542-116">Specifies the name of the probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28542-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28542-117">CommonParameters</span></span>
<span data-ttu-id="28542-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28542-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28542-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28542-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28542-120">입력</span><span class="sxs-lookup"><span data-stu-id="28542-120">INPUTS</span></span>

### <span data-ttu-id="28542-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28542-121">PSApplicationGateway</span></span>
<span data-ttu-id="28542-122">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="28542-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="28542-123">출력</span><span class="sxs-lookup"><span data-stu-id="28542-123">OUTPUTS</span></span>

### <span data-ttu-id="28542-124">Microsoft. \*. m i m a. 모델. m i m a 검색</span><span class="sxs-lookup"><span data-stu-id="28542-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="28542-125">System.webserver. t e 1 [Microsoft Azure. \* Psapplication게이트웨이 검색]</span><span class="sxs-lookup"><span data-stu-id="28542-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="28542-126">상속자</span><span class="sxs-lookup"><span data-stu-id="28542-126">NOTES</span></span>

## <span data-ttu-id="28542-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28542-127">RELATED LINKS</span></span>

[<span data-ttu-id="28542-128">기존 application gateway에 프로브 추가</span><span class="sxs-lookup"><span data-stu-id="28542-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="28542-129">추가-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="28542-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="28542-130">새로운 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="28542-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="28542-131">제거-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="28542-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="28542-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="28542-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

