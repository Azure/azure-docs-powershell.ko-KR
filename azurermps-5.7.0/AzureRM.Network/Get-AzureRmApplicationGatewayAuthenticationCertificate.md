---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bec9d197d039ea3934607ee291bdd6511ae6f4a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532130"
---
# <span data-ttu-id="ca9fa-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ca9fa-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ca9fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9fa-103">응용 프로그램 게이트웨이에 대 한 인증 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca9fa-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca9fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca9fa-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca9fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ca9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9fa-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 대 한 인증 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca9fa-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="ca9fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ca9fa-107">EXAMPLES</span></span>

## <span data-ttu-id="ca9fa-108">변수</span><span class="sxs-lookup"><span data-stu-id="ca9fa-108">PARAMETERS</span></span>

### <span data-ttu-id="ca9fa-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca9fa-109">-ApplicationGateway</span></span>
<span data-ttu-id="ca9fa-110">이 cmdlet이 인증 인증서를 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca9fa-110">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="ca9fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9fa-111">-DefaultProfile</span></span>
<span data-ttu-id="ca9fa-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca9fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca9fa-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ca9fa-113">-Name</span></span>
<span data-ttu-id="ca9fa-114">이 cmdlet이 가져오는 인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca9fa-114">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ca9fa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9fa-115">CommonParameters</span></span>
<span data-ttu-id="ca9fa-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca9fa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9fa-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9fa-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9fa-118">입력</span><span class="sxs-lookup"><span data-stu-id="ca9fa-118">INPUTS</span></span>

### <span data-ttu-id="ca9fa-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ca9fa-119">System.String</span></span>

## <span data-ttu-id="ca9fa-120">출력</span><span class="sxs-lookup"><span data-stu-id="ca9fa-120">OUTPUTS</span></span>

### <span data-ttu-id="ca9fa-121">Microsoft. \*. m i m. 모델</span><span class="sxs-lookup"><span data-stu-id="ca9fa-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ca9fa-122">상속자</span><span class="sxs-lookup"><span data-stu-id="ca9fa-122">NOTES</span></span>
* <span data-ttu-id="ca9fa-123">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="ca9fa-123">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ca9fa-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca9fa-124">RELATED LINKS</span></span>

[<span data-ttu-id="ca9fa-125">추가-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ca9fa-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ca9fa-126">새로운 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ca9fa-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ca9fa-127">제거-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ca9fa-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ca9fa-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ca9fa-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


