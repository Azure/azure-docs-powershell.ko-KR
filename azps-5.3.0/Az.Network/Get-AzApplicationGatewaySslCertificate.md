---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 3e7010309c6aed367e3771971a8b1c2841548fe0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492198"
---
# <span data-ttu-id="0bb4a-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0bb4a-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0bb4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb4a-103">애플리케이션 게이트웨이에 대한 SSL 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="0bb4a-104">구문</span><span class="sxs-lookup"><span data-stu-id="0bb4a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bb4a-105">설명</span><span class="sxs-lookup"><span data-stu-id="0bb4a-105">DESCRIPTION</span></span>
<span data-ttu-id="0bb4a-106">**Get-AzApplicationGatewaySslCertificate** cmdlet은 애플리케이션 게이트웨이에 대한 SSL 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="0bb4a-107">예제</span><span class="sxs-lookup"><span data-stu-id="0bb4a-107">EXAMPLES</span></span>

### <span data-ttu-id="0bb4a-108">예제 1: 특정 SSL 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="0bb4a-109">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 해당 애플리케이션이라는 변수에 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="0bb4a-110">두 번째 명령은 애플리케이션 게이트웨이에서 Cert01이라는 SSL 인증서를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="0bb4a-111">이 명령은 인증서를 $Cert.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="0bb4a-112">예제 2: SSL 인증서 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="0bb4a-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="0bb4a-113">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 해당 애플리케이션이라는 변수에 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="0bb4a-114">이 두 번째 명령은 애플리케이션 게이트웨이에서 SSL 인증서의 목록을 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="0bb4a-115">그런 다음 명령은 결과를 이름 지정한 변수에 $Certs.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="0bb4a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bb4a-116">PARAMETERS</span></span>

### <span data-ttu-id="0bb4a-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0bb4a-117">-ApplicationGateway</span></span>
<span data-ttu-id="0bb4a-118">SSL 인증서를 포함하는 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="0bb4a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb4a-119">-DefaultProfile</span></span>
<span data-ttu-id="0bb4a-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bb4a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0bb4a-121">-Name</span></span>
<span data-ttu-id="0bb4a-122">이 cmdlet에서 얻을 SSL 인증서 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0bb4a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb4a-123">CommonParameters</span></span>
<span data-ttu-id="0bb4a-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb4a-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0bb4a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb4a-126">입력</span><span class="sxs-lookup"><span data-stu-id="0bb4a-126">INPUTS</span></span>

### <span data-ttu-id="0bb4a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0bb4a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0bb4a-128">출력</span><span class="sxs-lookup"><span data-stu-id="0bb4a-128">OUTPUTS</span></span>

### <span data-ttu-id="0bb4a-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0bb4a-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0bb4a-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0bb4a-130">NOTES</span></span>

## <span data-ttu-id="0bb4a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bb4a-131">RELATED LINKS</span></span>

[<span data-ttu-id="0bb4a-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0bb4a-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0bb4a-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0bb4a-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0bb4a-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0bb4a-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0bb4a-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0bb4a-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


