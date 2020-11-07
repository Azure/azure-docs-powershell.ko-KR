---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7b5f37cb42d128cbf44294520419c8f4d09124fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700197"
---
# <span data-ttu-id="b4a8c-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b4a8c-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b4a8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a8c-103">Azure application gateway에서 SSL 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a8c-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="b4a8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4a8c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4a8c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4a8c-105">DESCRIPTION</span></span>
<span data-ttu-id="b4a8c-106">**AzApplicationGatewaySslCertificate** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 SSL (Secure Sockets layer) 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a8c-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="b4a8c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b4a8c-107">EXAMPLES</span></span>

### <span data-ttu-id="b4a8c-108">예제 1: 응용 프로그램 게이트웨이에서 SSL 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="b4a8c-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="b4a8c-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a8c-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b4a8c-110">두 번째 명령은 $AppGW 변수에 저장 된 응용 프로그램 게이트웨이에서 Cert02 이라는 이름의 SSL 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a8c-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="b4a8c-111">변수</span><span class="sxs-lookup"><span data-stu-id="b4a8c-111">PARAMETERS</span></span>

### <span data-ttu-id="b4a8c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4a8c-112">-ApplicationGateway</span></span>
<span data-ttu-id="b4a8c-113">이 cmdlet이 SSL 인증서를 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a8c-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="b4a8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a8c-114">-DefaultProfile</span></span>
<span data-ttu-id="b4a8c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a8c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4a8c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="b4a8c-116">-Name</span></span>
<span data-ttu-id="b4a8c-117">이 cmdlet이 제거 하는 SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a8c-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b4a8c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a8c-118">CommonParameters</span></span>
<span data-ttu-id="b4a8c-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a8c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a8c-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4a8c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a8c-121">입력</span><span class="sxs-lookup"><span data-stu-id="b4a8c-121">INPUTS</span></span>

### <span data-ttu-id="b4a8c-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4a8c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4a8c-123">출력</span><span class="sxs-lookup"><span data-stu-id="b4a8c-123">OUTPUTS</span></span>

### <span data-ttu-id="b4a8c-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4a8c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4a8c-125">상속자</span><span class="sxs-lookup"><span data-stu-id="b4a8c-125">NOTES</span></span>

## <span data-ttu-id="b4a8c-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4a8c-126">RELATED LINKS</span></span>

[<span data-ttu-id="b4a8c-127">추가-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b4a8c-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b4a8c-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b4a8c-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b4a8c-129">새로운 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b4a8c-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b4a8c-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b4a8c-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)

