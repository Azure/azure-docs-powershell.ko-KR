---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 033ca62f766f854be27ad75a6b63a8f883ba58d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882993"
---
# <span data-ttu-id="8ba59-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8ba59-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="8ba59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ba59-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba59-103">응용 프로그램 게이트웨이에 대 한 인증 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ba59-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ba59-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ba59-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ba59-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ba59-105">DESCRIPTION</span></span>
<span data-ttu-id="8ba59-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 대 한 인증 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ba59-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="8ba59-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8ba59-107">EXAMPLES</span></span>

### <span data-ttu-id="8ba59-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="8ba59-108">1:</span></span>
```

```

## <span data-ttu-id="8ba59-109">변수</span><span class="sxs-lookup"><span data-stu-id="8ba59-109">PARAMETERS</span></span>

### <span data-ttu-id="8ba59-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ba59-110">-ApplicationGateway</span></span>
<span data-ttu-id="8ba59-111">이 cmdlet이 인증 인증서를 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ba59-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="8ba59-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba59-112">-DefaultProfile</span></span>
<span data-ttu-id="8ba59-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ba59-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ba59-114">-이름</span><span class="sxs-lookup"><span data-stu-id="8ba59-114">-Name</span></span>
<span data-ttu-id="8ba59-115">이 cmdlet이 가져오는 인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ba59-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8ba59-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba59-116">CommonParameters</span></span>
<span data-ttu-id="8ba59-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ba59-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba59-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba59-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba59-119">입력</span><span class="sxs-lookup"><span data-stu-id="8ba59-119">INPUTS</span></span>

### <span data-ttu-id="8ba59-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8ba59-120">System.String</span></span>

## <span data-ttu-id="8ba59-121">출력</span><span class="sxs-lookup"><span data-stu-id="8ba59-121">OUTPUTS</span></span>

### <span data-ttu-id="8ba59-122">Microsoft. \*. m i m. 모델</span><span class="sxs-lookup"><span data-stu-id="8ba59-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="8ba59-123">상속자</span><span class="sxs-lookup"><span data-stu-id="8ba59-123">NOTES</span></span>
* <span data-ttu-id="8ba59-124">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="8ba59-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8ba59-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ba59-125">RELATED LINKS</span></span>

[<span data-ttu-id="8ba59-126">추가-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8ba59-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8ba59-127">새로운 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8ba59-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8ba59-128">제거-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8ba59-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8ba59-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8ba59-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


