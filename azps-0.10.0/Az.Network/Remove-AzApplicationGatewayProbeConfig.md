---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 320588b81791c033b94a07261f769fa0886d2f2c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875361"
---
# <span data-ttu-id="04d59-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04d59-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="04d59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04d59-102">SYNOPSIS</span></span>
<span data-ttu-id="04d59-103">기존 응용 프로그램 게이트웨이에서 상태 프로브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d59-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="04d59-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04d59-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04d59-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04d59-105">DESCRIPTION</span></span>
<span data-ttu-id="04d59-106">Remove-AzApplicationGatewayProbeConfig cmdlet은 기존 응용 프로그램 게이트웨이에서 heath probe를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d59-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="04d59-107">예제의</span><span class="sxs-lookup"><span data-stu-id="04d59-107">EXAMPLES</span></span>

### <span data-ttu-id="04d59-108">예제 1: 기존 응용 프로그램 게이트웨이에서 상태 프로브 제거</span><span class="sxs-lookup"><span data-stu-id="04d59-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="04d59-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에서 Probe04 이라는 상태 프로브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d59-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="04d59-110">변수</span><span class="sxs-lookup"><span data-stu-id="04d59-110">PARAMETERS</span></span>

### <span data-ttu-id="04d59-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04d59-111">-ApplicationGateway</span></span>
<span data-ttu-id="04d59-112">이 cmdlet이 프로브를 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d59-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="04d59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d59-113">-DefaultProfile</span></span>
<span data-ttu-id="04d59-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04d59-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04d59-115">-이름</span><span class="sxs-lookup"><span data-stu-id="04d59-115">-Name</span></span>
<span data-ttu-id="04d59-116">이 cmdlet이 제거할 프로브 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d59-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d59-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d59-117">CommonParameters</span></span>
<span data-ttu-id="04d59-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d59-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d59-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04d59-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d59-120">입력</span><span class="sxs-lookup"><span data-stu-id="04d59-120">INPUTS</span></span>

### <span data-ttu-id="04d59-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04d59-121">PSApplicationGateway</span></span>
<span data-ttu-id="04d59-122">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d59-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="04d59-123">출력</span><span class="sxs-lookup"><span data-stu-id="04d59-123">OUTPUTS</span></span>

### <span data-ttu-id="04d59-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04d59-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="04d59-125">상속자</span><span class="sxs-lookup"><span data-stu-id="04d59-125">NOTES</span></span>

## <span data-ttu-id="04d59-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04d59-126">RELATED LINKS</span></span>

[<span data-ttu-id="04d59-127">기존 응용 프로그램 게이트웨이에서 프로브 제거</span><span class="sxs-lookup"><span data-stu-id="04d59-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="04d59-128">추가-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04d59-128">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="04d59-129">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04d59-129">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="04d59-130">새로운 AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04d59-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="04d59-131">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04d59-131">Set-AzApplicationGatewayProbeConfig</span></span>]()

