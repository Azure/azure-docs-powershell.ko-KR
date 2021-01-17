---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: a9b0d41ad700d0591e38fa339c38efb85cb00859
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379275"
---
# <span data-ttu-id="2598a-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2598a-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="2598a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2598a-102">SYNOPSIS</span></span>
<span data-ttu-id="2598a-103">애플리케이션 게이트웨이에 대한 SSL 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2598a-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="2598a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2598a-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2598a-105">설명</span><span class="sxs-lookup"><span data-stu-id="2598a-105">DESCRIPTION</span></span>
<span data-ttu-id="2598a-106">**New-AzApplicationGatewaySslProfile** cmdlet은 애플리케이션 게이트웨이에 대한 SSL 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2598a-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="2598a-107">ssl 프로필은 HTTPS 수신기에서 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="2598a-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="2598a-108">예제</span><span class="sxs-lookup"><span data-stu-id="2598a-108">EXAMPLES</span></span>

### <span data-ttu-id="2598a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="2598a-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="2598a-110">첫 번째 명령은 새 SSL 정책을 만들고 새 $sslPolicy 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2598a-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="2598a-111">두 번째 명령은 신뢰할 수 있는 클라이언트 CA 인증서 체인을 만들고 $ClientCert 01 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2598a-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="2598a-112">세 번째 명령은 ssl 정책 및 신뢰할 수 있는 클라이언트 CA 인증서 체인을 사용하여 새 SSL 프로필을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2598a-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="2598a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2598a-113">PARAMETERS</span></span>

### <span data-ttu-id="2598a-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2598a-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="2598a-115">클라이언트 인증 구성 설정</span><span class="sxs-lookup"><span data-stu-id="2598a-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="2598a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2598a-116">-DefaultProfile</span></span>
<span data-ttu-id="2598a-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2598a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2598a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2598a-118">-Name</span></span>
<span data-ttu-id="2598a-119">SSL 프로필의 이름</span><span class="sxs-lookup"><span data-stu-id="2598a-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="2598a-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="2598a-120">-SslPolicy</span></span>
<span data-ttu-id="2598a-121">SSL 정책</span><span class="sxs-lookup"><span data-stu-id="2598a-121">SSL policy</span></span>

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

### <span data-ttu-id="2598a-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="2598a-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="2598a-123">신뢰할 수 있는 클라이언트 CA 인증서 체인</span><span class="sxs-lookup"><span data-stu-id="2598a-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="2598a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2598a-124">CommonParameters</span></span>
<span data-ttu-id="2598a-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2598a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2598a-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2598a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2598a-127">입력</span><span class="sxs-lookup"><span data-stu-id="2598a-127">INPUTS</span></span>

### <span data-ttu-id="2598a-128">없음</span><span class="sxs-lookup"><span data-stu-id="2598a-128">None</span></span>

## <span data-ttu-id="2598a-129">출력</span><span class="sxs-lookup"><span data-stu-id="2598a-129">OUTPUTS</span></span>

### <span data-ttu-id="2598a-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2598a-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="2598a-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2598a-131">NOTES</span></span>

## <span data-ttu-id="2598a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2598a-132">RELATED LINKS</span></span>

[<span data-ttu-id="2598a-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2598a-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2598a-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2598a-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2598a-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2598a-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2598a-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2598a-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)