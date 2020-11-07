---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: b3e2b3ea03ca0bae0db1bea1606e4ae6b94a597e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875624"
---
# <span data-ttu-id="6036f-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6036f-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="6036f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6036f-102">SYNOPSIS</span></span>
<span data-ttu-id="6036f-103">응용 프로그램 게이트웨이에서 기존 상태 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6036f-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="6036f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6036f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6036f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6036f-105">DESCRIPTION</span></span>
<span data-ttu-id="6036f-106">Get-AzApplicationGatewayProbeConfig cmdlet은 응용 프로그램 게이트웨이에서 기존 상태 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6036f-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="6036f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6036f-107">EXAMPLES</span></span>

### <span data-ttu-id="6036f-108">예제 1: 응용 프로그램 게이트웨이에서 기존 프로브 가져오기</span><span class="sxs-lookup"><span data-stu-id="6036f-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="6036f-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에서 Probe02 이라는 상태 프로브를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6036f-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="6036f-110">변수</span><span class="sxs-lookup"><span data-stu-id="6036f-110">PARAMETERS</span></span>

### <span data-ttu-id="6036f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6036f-111">-ApplicationGateway</span></span>
<span data-ttu-id="6036f-112">이 cmdlet이 프로브 구성을 가져오는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6036f-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="6036f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6036f-113">-DefaultProfile</span></span>
<span data-ttu-id="6036f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6036f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6036f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="6036f-115">-Name</span></span>
<span data-ttu-id="6036f-116">프로브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6036f-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="6036f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6036f-117">CommonParameters</span></span>
<span data-ttu-id="6036f-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6036f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6036f-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6036f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6036f-120">입력</span><span class="sxs-lookup"><span data-stu-id="6036f-120">INPUTS</span></span>

### <span data-ttu-id="6036f-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6036f-121">PSApplicationGateway</span></span>
<span data-ttu-id="6036f-122">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6036f-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="6036f-123">출력</span><span class="sxs-lookup"><span data-stu-id="6036f-123">OUTPUTS</span></span>

### <span data-ttu-id="6036f-124">Microsoft. \*. m i m a. 모델. m i m a 검색</span><span class="sxs-lookup"><span data-stu-id="6036f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="6036f-125">System.webserver. t e 1 [Microsoft Azure. \* Psapplication게이트웨이 검색]</span><span class="sxs-lookup"><span data-stu-id="6036f-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="6036f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="6036f-126">NOTES</span></span>

## <span data-ttu-id="6036f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6036f-127">RELATED LINKS</span></span>

[<span data-ttu-id="6036f-128">기존 application gateway에 프로브 추가</span><span class="sxs-lookup"><span data-stu-id="6036f-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="6036f-129">추가-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6036f-129">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6036f-130">새로운 AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6036f-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6036f-131">제거-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6036f-131">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6036f-132">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6036f-132">Set-AzApplicationGatewayProbeConfig</span></span>]()

