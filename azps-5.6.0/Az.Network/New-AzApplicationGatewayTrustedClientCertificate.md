---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e34d170167aac09cd64ca11d0838f36fc0515423
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990033"
---
# <span data-ttu-id="b3f5a-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b3f5a-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="b3f5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f5a-103">애플리케이션 게이트웨이에 대한 신뢰할 수 있는 클라이언트 CA 인증서 체인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3f5a-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="b3f5a-104">구문</span><span class="sxs-lookup"><span data-stu-id="b3f5a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3f5a-105">설명</span><span class="sxs-lookup"><span data-stu-id="b3f5a-105">DESCRIPTION</span></span>
<span data-ttu-id="b3f5a-106">New-AzApplicationGatewayTrustedClientCertificate cmdlet은 애플리케이션 게이트웨이에 대한 신뢰할 수 있는 클라이언트 CA 인증서 체인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3f5a-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="b3f5a-107">예제</span><span class="sxs-lookup"><span data-stu-id="b3f5a-107">EXAMPLES</span></span>

### <span data-ttu-id="b3f5a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b3f5a-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="b3f5a-109">명령은 클라이언트 CA 인증서의 경로를 입력으로 사용하여 새 신뢰할 수 있는 클라이언트 CA 인증서 체인 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3f5a-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="b3f5a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b3f5a-110">PARAMETERS</span></span>

### <span data-ttu-id="b3f5a-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b3f5a-111">-CertificateFile</span></span>
<span data-ttu-id="b3f5a-112">신뢰할 수 있는 클라이언트 CA 인증서 체인 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="b3f5a-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="b3f5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f5a-113">-DefaultProfile</span></span>
<span data-ttu-id="b3f5a-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f5a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3f5a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b3f5a-115">-Name</span></span>
<span data-ttu-id="b3f5a-116">신뢰할 수 있는 클라이언트 CA 인증서 체인의 이름</span><span class="sxs-lookup"><span data-stu-id="b3f5a-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="b3f5a-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b3f5a-117">-Confirm</span></span>
<span data-ttu-id="b3f5a-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3f5a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3f5a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3f5a-119">-WhatIf</span></span>
<span data-ttu-id="b3f5a-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3f5a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3f5a-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3f5a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3f5a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f5a-122">CommonParameters</span></span>
<span data-ttu-id="b3f5a-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b3f5a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f5a-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3f5a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f5a-125">입력</span><span class="sxs-lookup"><span data-stu-id="b3f5a-125">INPUTS</span></span>

### <span data-ttu-id="b3f5a-126">없음</span><span class="sxs-lookup"><span data-stu-id="b3f5a-126">None</span></span>

## <span data-ttu-id="b3f5a-127">출력</span><span class="sxs-lookup"><span data-stu-id="b3f5a-127">OUTPUTS</span></span>

### <span data-ttu-id="b3f5a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b3f5a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="b3f5a-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b3f5a-129">NOTES</span></span>

## <span data-ttu-id="b3f5a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3f5a-130">RELATED LINKS</span></span>

[<span data-ttu-id="b3f5a-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b3f5a-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b3f5a-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b3f5a-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b3f5a-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b3f5a-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b3f5a-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b3f5a-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)