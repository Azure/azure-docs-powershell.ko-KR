---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179953"
---
# <span data-ttu-id="116b1-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="116b1-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="116b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="116b1-102">SYNOPSIS</span></span>
<span data-ttu-id="116b1-103">애플리케이션 게이트웨이에 신뢰할 수 있는 클라이언트 CA 인증서 체인을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="116b1-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="116b1-104">구문</span><span class="sxs-lookup"><span data-stu-id="116b1-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="116b1-105">설명</span><span class="sxs-lookup"><span data-stu-id="116b1-105">DESCRIPTION</span></span>
<span data-ttu-id="116b1-106">**Add-AzApplicationGatewayTrustedClientCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 신뢰할 수 있는 클라이언트 CA 인증서 체인을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="116b1-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="116b1-107">예제</span><span class="sxs-lookup"><span data-stu-id="116b1-107">EXAMPLES</span></span>

### <span data-ttu-id="116b1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="116b1-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="116b1-109">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="116b1-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="116b1-110">두 번째 명령은 클라이언트 CA 인증서의 경로를 입력으로 사용하여 신뢰할 수 있는 새 클라이언트 CA 인증서 체인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="116b1-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="116b1-111">세 번째 명령은 신뢰할 수 있는 클라이언트 인증서를 사용하여 SSL 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="116b1-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="116b1-112">네 번째 명령은 Application Gateway를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="116b1-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="116b1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="116b1-113">PARAMETERS</span></span>

### <span data-ttu-id="116b1-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="116b1-114">-ApplicationGateway</span></span>
<span data-ttu-id="116b1-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="116b1-115">The applicationGateway</span></span>

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

### <span data-ttu-id="116b1-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="116b1-116">-CertificateFile</span></span>
<span data-ttu-id="116b1-117">신뢰할 수 있는 클라이언트 CA 인증서 체인 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="116b1-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="116b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116b1-118">-DefaultProfile</span></span>
<span data-ttu-id="116b1-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="116b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="116b1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="116b1-120">-Name</span></span>
<span data-ttu-id="116b1-121">신뢰할 수 있는 클라이언트 CA 인증서 체인의 이름</span><span class="sxs-lookup"><span data-stu-id="116b1-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="116b1-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="116b1-122">-Confirm</span></span>
<span data-ttu-id="116b1-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="116b1-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116b1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="116b1-124">-WhatIf</span></span>
<span data-ttu-id="116b1-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="116b1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="116b1-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="116b1-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116b1-127">CommonParameters</span></span>
<span data-ttu-id="116b1-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="116b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116b1-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="116b1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116b1-130">입력</span><span class="sxs-lookup"><span data-stu-id="116b1-130">INPUTS</span></span>

### <span data-ttu-id="116b1-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="116b1-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="116b1-132">출력</span><span class="sxs-lookup"><span data-stu-id="116b1-132">OUTPUTS</span></span>

### <span data-ttu-id="116b1-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="116b1-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="116b1-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="116b1-134">NOTES</span></span>

## <span data-ttu-id="116b1-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="116b1-135">RELATED LINKS</span></span>

[<span data-ttu-id="116b1-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="116b1-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="116b1-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="116b1-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="116b1-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="116b1-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="116b1-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="116b1-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)