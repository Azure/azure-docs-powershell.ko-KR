---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b8e74c8630dc7f5ba0cd3633314b416ca9a3e39e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986729"
---
# <span data-ttu-id="6b6b5-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b6b5-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6b6b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b6b5-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6b5-103">Azure 애플리케이션 게이트웨이에서 SSL 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6b6b5-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="6b6b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b6b5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b6b5-105">설명</span><span class="sxs-lookup"><span data-stu-id="6b6b5-105">DESCRIPTION</span></span>
<span data-ttu-id="6b6b5-106">**Remove-AzApplicationGatewaySslCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에서 SSL(Secure Sockets Layer) 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6b6b5-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="6b6b5-107">예제</span><span class="sxs-lookup"><span data-stu-id="6b6b5-107">EXAMPLES</span></span>

### <span data-ttu-id="6b6b5-108">예제 1: 애플리케이션 게이트웨이에서 SSL 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="6b6b5-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="6b6b5-109">첫 번째 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이를 얻게 하여 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6b6b5-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6b6b5-110">두 번째 명령은 애플리케이션 게이트웨이에서 Cert02라는 SSL 인증서를 $AppGW 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6b6b5-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="6b6b5-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b6b5-111">PARAMETERS</span></span>

### <span data-ttu-id="6b6b5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b6b5-112">-ApplicationGateway</span></span>
<span data-ttu-id="6b6b5-113">이 cmdlet에서 SSL 인증서를 제거하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b6b5-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="6b6b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6b5-114">-DefaultProfile</span></span>
<span data-ttu-id="6b6b5-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b6b5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b6b5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6b6b5-116">-Name</span></span>
<span data-ttu-id="6b6b5-117">이 cmdlet이 제거한 SSL 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b6b5-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6b6b5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6b5-118">CommonParameters</span></span>
<span data-ttu-id="6b6b5-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b6b5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6b5-120">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6b6b5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6b5-121">입력</span><span class="sxs-lookup"><span data-stu-id="6b6b5-121">INPUTS</span></span>

### <span data-ttu-id="6b6b5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b6b5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6b6b5-123">출력</span><span class="sxs-lookup"><span data-stu-id="6b6b5-123">OUTPUTS</span></span>

### <span data-ttu-id="6b6b5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b6b5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6b6b5-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b6b5-125">NOTES</span></span>

## <span data-ttu-id="6b6b5-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b6b5-126">RELATED LINKS</span></span>

[<span data-ttu-id="6b6b5-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b6b5-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6b6b5-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b6b5-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6b6b5-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b6b5-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6b6b5-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b6b5-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


