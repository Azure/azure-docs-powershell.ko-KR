---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360991"
---
# <span data-ttu-id="656c2-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="656c2-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="656c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="656c2-102">SYNOPSIS</span></span>
<span data-ttu-id="656c2-103">애플리케이션 게이트웨이에 대한 신뢰할 수 있는 클라이언트 CA 인증서 체인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="656c2-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="656c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="656c2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="656c2-105">설명</span><span class="sxs-lookup"><span data-stu-id="656c2-105">DESCRIPTION</span></span>
<span data-ttu-id="656c2-106">New-AzApplicationGatewayTrustedClientCertificate cmdlet은 애플리케이션 게이트웨이에 대한 신뢰할 수 있는 클라이언트 CA 인증서 체인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="656c2-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="656c2-107">예제</span><span class="sxs-lookup"><span data-stu-id="656c2-107">EXAMPLES</span></span>

### <span data-ttu-id="656c2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="656c2-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="656c2-109">이 명령은 클라이언트 CA 인증서의 경로를 입력으로 사용하여 신뢰할 수 있는 새 클라이언트 CA 인증서 체인 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="656c2-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="656c2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="656c2-110">PARAMETERS</span></span>

### <span data-ttu-id="656c2-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="656c2-111">-CertificateFile</span></span>
<span data-ttu-id="656c2-112">신뢰할 수 있는 클라이언트 CA 인증서 체인 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="656c2-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="656c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="656c2-113">-DefaultProfile</span></span>
<span data-ttu-id="656c2-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="656c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="656c2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="656c2-115">-Name</span></span>
<span data-ttu-id="656c2-116">신뢰할 수 있는 클라이언트 CA 인증서 체인의 이름</span><span class="sxs-lookup"><span data-stu-id="656c2-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="656c2-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="656c2-117">-Confirm</span></span>
<span data-ttu-id="656c2-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="656c2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="656c2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="656c2-119">-WhatIf</span></span>
<span data-ttu-id="656c2-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="656c2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="656c2-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="656c2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="656c2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="656c2-122">CommonParameters</span></span>
<span data-ttu-id="656c2-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="656c2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="656c2-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="656c2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="656c2-125">입력</span><span class="sxs-lookup"><span data-stu-id="656c2-125">INPUTS</span></span>

### <span data-ttu-id="656c2-126">없음</span><span class="sxs-lookup"><span data-stu-id="656c2-126">None</span></span>

## <span data-ttu-id="656c2-127">출력</span><span class="sxs-lookup"><span data-stu-id="656c2-127">OUTPUTS</span></span>

### <span data-ttu-id="656c2-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="656c2-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="656c2-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="656c2-129">NOTES</span></span>

## <span data-ttu-id="656c2-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="656c2-130">RELATED LINKS</span></span>

[<span data-ttu-id="656c2-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="656c2-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="656c2-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="656c2-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="656c2-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="656c2-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="656c2-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="656c2-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)