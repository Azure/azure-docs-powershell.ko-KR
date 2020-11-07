---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1743ed0427fdc0dd952c9b86d51c13c3ed855620
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870302"
---
# <span data-ttu-id="5411a-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5411a-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5411a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5411a-102">SYNOPSIS</span></span>
<span data-ttu-id="5411a-103">응용 프로그램 게이트웨이에 대 한 인증 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5411a-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="5411a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5411a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5411a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5411a-105">DESCRIPTION</span></span>
<span data-ttu-id="5411a-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 대 한 인증 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5411a-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5411a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5411a-107">EXAMPLES</span></span>

### <span data-ttu-id="5411a-108">예제 1: 지정 된 인증 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="5411a-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="5411a-109">첫 번째 명령은 appGwName 이라는 응용 프로그램 게이트웨이를 가져와이를 $appgw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5411a-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="5411a-110">두 번째 명령은 pool01 이라는 인증 인증서를 가져와이를 $pool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5411a-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="5411a-111">변수</span><span class="sxs-lookup"><span data-stu-id="5411a-111">PARAMETERS</span></span>

### <span data-ttu-id="5411a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5411a-112">-ApplicationGateway</span></span>
<span data-ttu-id="5411a-113">이 cmdlet이 인증 인증서를 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5411a-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="5411a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5411a-114">-DefaultProfile</span></span>
<span data-ttu-id="5411a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5411a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5411a-116">-이름</span><span class="sxs-lookup"><span data-stu-id="5411a-116">-Name</span></span>
<span data-ttu-id="5411a-117">이 cmdlet이 가져오는 인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5411a-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5411a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5411a-118">CommonParameters</span></span>
<span data-ttu-id="5411a-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5411a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5411a-120">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5411a-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5411a-121">입력</span><span class="sxs-lookup"><span data-stu-id="5411a-121">INPUTS</span></span>

### <span data-ttu-id="5411a-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5411a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5411a-123">출력</span><span class="sxs-lookup"><span data-stu-id="5411a-123">OUTPUTS</span></span>

### <span data-ttu-id="5411a-124">Microsoft. \*. m i m. 모델</span><span class="sxs-lookup"><span data-stu-id="5411a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5411a-125">상속자</span><span class="sxs-lookup"><span data-stu-id="5411a-125">NOTES</span></span>
* <span data-ttu-id="5411a-126">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="5411a-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5411a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5411a-127">RELATED LINKS</span></span>

[<span data-ttu-id="5411a-128">추가-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5411a-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5411a-129">새로운 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5411a-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5411a-130">제거-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5411a-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5411a-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5411a-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


