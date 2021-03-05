---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: ac4da06b2f90f9d7bb5c3cbccbde98c8c65db481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982475"
---
# <span data-ttu-id="29475-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="29475-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="29475-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29475-102">SYNOPSIS</span></span>
<span data-ttu-id="29475-103">애플리케이션 게이트웨이에 신뢰할 수 있는 클라이언트 CA 인증서 체인을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="29475-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="29475-104">구문</span><span class="sxs-lookup"><span data-stu-id="29475-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29475-105">설명</span><span class="sxs-lookup"><span data-stu-id="29475-105">DESCRIPTION</span></span>
<span data-ttu-id="29475-106">**Add-AzApplicationGatewayTrustedClientCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 신뢰할 수 있는 클라이언트 CA 인증서 체인을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="29475-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="29475-107">예제</span><span class="sxs-lookup"><span data-stu-id="29475-107">EXAMPLES</span></span>

### <span data-ttu-id="29475-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="29475-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="29475-109">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 변수에 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="29475-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="29475-110">두 번째 명령은 클라이언트 CA 인증서의 경로를 입력으로 사용하여 새 신뢰할 수 있는 클라이언트 CA 인증서 체인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29475-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="29475-111">세 번째 명령은 신뢰할 수 있는 클라이언트 인증서를 사용하여 SSL 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29475-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="29475-112">네 번째 명령은 Application Gateway를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="29475-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="29475-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="29475-113">PARAMETERS</span></span>

### <span data-ttu-id="29475-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29475-114">-ApplicationGateway</span></span>
<span data-ttu-id="29475-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29475-115">The applicationGateway</span></span>

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

### <span data-ttu-id="29475-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="29475-116">-CertificateFile</span></span>
<span data-ttu-id="29475-117">신뢰할 수 있는 클라이언트 CA 인증서 체인 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="29475-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="29475-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29475-118">-DefaultProfile</span></span>
<span data-ttu-id="29475-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29475-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29475-120">-Name</span><span class="sxs-lookup"><span data-stu-id="29475-120">-Name</span></span>
<span data-ttu-id="29475-121">신뢰할 수 있는 클라이언트 CA 인증서 체인의 이름</span><span class="sxs-lookup"><span data-stu-id="29475-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="29475-122">-확인</span><span class="sxs-lookup"><span data-stu-id="29475-122">-Confirm</span></span>
<span data-ttu-id="29475-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="29475-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29475-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29475-124">-WhatIf</span></span>
<span data-ttu-id="29475-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="29475-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29475-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29475-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29475-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29475-127">CommonParameters</span></span>
<span data-ttu-id="29475-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29475-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29475-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29475-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29475-130">입력</span><span class="sxs-lookup"><span data-stu-id="29475-130">INPUTS</span></span>

### <span data-ttu-id="29475-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29475-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="29475-132">출력</span><span class="sxs-lookup"><span data-stu-id="29475-132">OUTPUTS</span></span>

### <span data-ttu-id="29475-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29475-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="29475-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29475-134">NOTES</span></span>

## <span data-ttu-id="29475-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29475-135">RELATED LINKS</span></span>

[<span data-ttu-id="29475-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="29475-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="29475-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="29475-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="29475-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="29475-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="29475-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="29475-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)