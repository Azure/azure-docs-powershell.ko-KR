---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 8930041959712b7533651262a39409e884ffb177
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362944"
---
# <span data-ttu-id="d556c-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d556c-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="d556c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d556c-102">SYNOPSIS</span></span>
<span data-ttu-id="d556c-103">애플리케이션 게이트웨이에 SSL 프로필을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d556c-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="d556c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d556c-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d556c-105">설명</span><span class="sxs-lookup"><span data-stu-id="d556c-105">DESCRIPTION</span></span>
<span data-ttu-id="d556c-106">**Add-AzApplicationGatewaySslProfile** cmdlet은 애플리케이션 게이트웨이에 SSL 프로필을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d556c-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="d556c-107">SSL 프로필은 HTTPS 수신기에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d556c-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="d556c-108">예제</span><span class="sxs-lookup"><span data-stu-id="d556c-108">EXAMPLES</span></span>

### <span data-ttu-id="d556c-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="d556c-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="d556c-110">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d556c-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d556c-111">두 번째 명령은 새 SSL 정책을 만들고 새 $sslPolicy 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d556c-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="d556c-112">세 번째 및 네 번째 명령은 두 개의 신뢰할 수 있는 클라이언트 CA 인증서 체인을 만들고 $ClientCert 01 및 $ClientCert 02 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d556c-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="d556c-113">다섯 번째 명령은 SSL 정책 및 신뢰할 수 있는 클라이언트 CA 인증서 체인이 있는 SSL 프로필을 애플리케이션 게이트웨이에 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d556c-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="d556c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d556c-114">PARAMETERS</span></span>

### <span data-ttu-id="d556c-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d556c-115">-ApplicationGateway</span></span>
<span data-ttu-id="d556c-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d556c-116">The applicationGateway</span></span>

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

### <span data-ttu-id="d556c-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="d556c-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="d556c-118">클라이언트 인증 구성 설정</span><span class="sxs-lookup"><span data-stu-id="d556c-118">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d556c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d556c-119">-DefaultProfile</span></span>
<span data-ttu-id="d556c-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d556c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d556c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d556c-121">-Name</span></span>
<span data-ttu-id="d556c-122">SSL 프로필의 이름</span><span class="sxs-lookup"><span data-stu-id="d556c-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="d556c-123">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="d556c-123">-SslPolicy</span></span>
<span data-ttu-id="d556c-124">SSL 정책</span><span class="sxs-lookup"><span data-stu-id="d556c-124">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d556c-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="d556c-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="d556c-126">신뢰할 수 있는 클라이언트 CA 인증서 체인</span><span class="sxs-lookup"><span data-stu-id="d556c-126">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d556c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d556c-127">CommonParameters</span></span>
<span data-ttu-id="d556c-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d556c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d556c-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d556c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d556c-130">입력</span><span class="sxs-lookup"><span data-stu-id="d556c-130">INPUTS</span></span>

### <span data-ttu-id="d556c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d556c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d556c-132">출력</span><span class="sxs-lookup"><span data-stu-id="d556c-132">OUTPUTS</span></span>

### <span data-ttu-id="d556c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d556c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d556c-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d556c-134">NOTES</span></span>

## <span data-ttu-id="d556c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d556c-135">RELATED LINKS</span></span>

[<span data-ttu-id="d556c-136">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d556c-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d556c-137">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d556c-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d556c-138">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d556c-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d556c-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d556c-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)