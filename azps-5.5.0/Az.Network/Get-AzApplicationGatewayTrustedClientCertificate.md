---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 99d56b837b67fe8b816c4f27c8658932a74452e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193916"
---
# <span data-ttu-id="60d17-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="60d17-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="60d17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60d17-102">SYNOPSIS</span></span>
<span data-ttu-id="60d17-103">Application Gateway에서 특정 이름으로 신뢰할 수 있는 클라이언트 CA 인증서 체인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="60d17-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="60d17-104">구문</span><span class="sxs-lookup"><span data-stu-id="60d17-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60d17-105">설명</span><span class="sxs-lookup"><span data-stu-id="60d17-105">DESCRIPTION</span></span>
<span data-ttu-id="60d17-106">Get-AzApplicationGatewayTrustedClientCertificate cmdlet은 Application Gateway에서 특정 이름으로 신뢰할 수 있는 클라이언트 CA 인증서 체인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="60d17-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="60d17-107">예제</span><span class="sxs-lookup"><span data-stu-id="60d17-107">EXAMPLES</span></span>

### <span data-ttu-id="60d17-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="60d17-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="60d17-109">첫 번째 명령은 Application Gateway를 사용하여 애플리케이션 게이트웨이를 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="60d17-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="60d17-110">두 번째 명령은 Application Gateway에서 지정된 이름으로 신뢰할 수 있는 클라이언트 CA 인증서 체인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="60d17-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="60d17-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60d17-111">PARAMETERS</span></span>

### <span data-ttu-id="60d17-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60d17-112">-ApplicationGateway</span></span>
<span data-ttu-id="60d17-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60d17-113">The applicationGateway</span></span>

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

### <span data-ttu-id="60d17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d17-114">-DefaultProfile</span></span>
<span data-ttu-id="60d17-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60d17-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60d17-116">-Name</span><span class="sxs-lookup"><span data-stu-id="60d17-116">-Name</span></span>
<span data-ttu-id="60d17-117">신뢰할 수 있는 클라이언트 CA 인증서 체인의 이름</span><span class="sxs-lookup"><span data-stu-id="60d17-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="60d17-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d17-118">CommonParameters</span></span>
<span data-ttu-id="60d17-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="60d17-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d17-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60d17-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d17-121">입력</span><span class="sxs-lookup"><span data-stu-id="60d17-121">INPUTS</span></span>

### <span data-ttu-id="60d17-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60d17-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="60d17-123">출력</span><span class="sxs-lookup"><span data-stu-id="60d17-123">OUTPUTS</span></span>

### <span data-ttu-id="60d17-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="60d17-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="60d17-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="60d17-125">NOTES</span></span>

## <span data-ttu-id="60d17-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60d17-126">RELATED LINKS</span></span>

[<span data-ttu-id="60d17-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="60d17-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="60d17-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="60d17-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="60d17-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="60d17-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="60d17-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="60d17-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)