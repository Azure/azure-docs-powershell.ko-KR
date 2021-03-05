---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: aa6dbacb85263d8f0169f913c07e56a9dbd1c7ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994056"
---
# <span data-ttu-id="64f0b-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="64f0b-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="64f0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="64f0b-103">애플리케이션 게이트웨이에 대한 SSL 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64f0b-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="64f0b-104">구문</span><span class="sxs-lookup"><span data-stu-id="64f0b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64f0b-105">설명</span><span class="sxs-lookup"><span data-stu-id="64f0b-105">DESCRIPTION</span></span>
<span data-ttu-id="64f0b-106">**Get-AzApplicationGatewaySslCertificate** cmdlet은 애플리케이션 게이트웨이에 대한 SSL 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64f0b-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="64f0b-107">예제</span><span class="sxs-lookup"><span data-stu-id="64f0b-107">EXAMPLES</span></span>

### <span data-ttu-id="64f0b-108">예제 1: 특정 SSL 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64f0b-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="64f0b-109">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="64f0b-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="64f0b-110">두 번째 명령은 애플리케이션 게이트웨이에서 Cert01이라는 SSL 인증서를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="64f0b-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="64f0b-111">명령은 인증서를 $Cert.</span><span class="sxs-lookup"><span data-stu-id="64f0b-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="64f0b-112">예제 2: SSL 인증서 목록 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64f0b-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="64f0b-113">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="64f0b-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="64f0b-114">이 두 번째 명령은 애플리케이션 게이트웨이의 SSL 인증서 목록을 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="64f0b-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="64f0b-115">그런 다음, 명령은 결과를 변수에 $Certs.</span><span class="sxs-lookup"><span data-stu-id="64f0b-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="64f0b-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="64f0b-116">PARAMETERS</span></span>

### <span data-ttu-id="64f0b-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="64f0b-117">-ApplicationGateway</span></span>
<span data-ttu-id="64f0b-118">SSL 인증서를 포함하는 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64f0b-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="64f0b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f0b-119">-DefaultProfile</span></span>
<span data-ttu-id="64f0b-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64f0b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64f0b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="64f0b-121">-Name</span></span>
<span data-ttu-id="64f0b-122">이 cmdlet에서 얻을 SSL 인증서 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64f0b-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="64f0b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f0b-123">CommonParameters</span></span>
<span data-ttu-id="64f0b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="64f0b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f0b-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64f0b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f0b-126">입력</span><span class="sxs-lookup"><span data-stu-id="64f0b-126">INPUTS</span></span>

### <span data-ttu-id="64f0b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="64f0b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="64f0b-128">출력</span><span class="sxs-lookup"><span data-stu-id="64f0b-128">OUTPUTS</span></span>

### <span data-ttu-id="64f0b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="64f0b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="64f0b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="64f0b-130">NOTES</span></span>

## <span data-ttu-id="64f0b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64f0b-131">RELATED LINKS</span></span>

[<span data-ttu-id="64f0b-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="64f0b-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="64f0b-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="64f0b-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="64f0b-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="64f0b-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="64f0b-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="64f0b-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


