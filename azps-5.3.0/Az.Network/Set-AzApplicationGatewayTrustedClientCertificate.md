---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 5f52b68e538072e6ff6aecde99f59337b532130c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495158"
---
# <span data-ttu-id="123d9-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="123d9-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="123d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="123d9-102">SYNOPSIS</span></span>
<span data-ttu-id="123d9-103">애플리케이션 게이트웨이의 신뢰할 수 있는 클라이언트 CA 인증서 체인을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="123d9-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="123d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="123d9-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="123d9-105">설명</span><span class="sxs-lookup"><span data-stu-id="123d9-105">DESCRIPTION</span></span>
<span data-ttu-id="123d9-106">**Set-AzApplicationGatewayTrustedClientCertificate** cmdlet은 애플리케이션 게이트웨이의 신뢰할 수 있는 클라이언트 CA 인증서 체인을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="123d9-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="123d9-107">예제</span><span class="sxs-lookup"><span data-stu-id="123d9-107">EXAMPLES</span></span>

### <span data-ttu-id="123d9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="123d9-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="123d9-109">위의 예제 시나리오에서는 기존 신뢰할 수 있는 클라이언트 CA 인증서 체인 개체를 업데이트하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="123d9-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="123d9-110">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $gw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="123d9-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="123d9-111">두 번째 명령은 새 CA 인증서 체인 파일을 사용하여 기존 신뢰할 수 있는 클라이언트 CA 인증서 체인 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="123d9-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="123d9-112">세 번째 명령은 Azure에서 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="123d9-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="123d9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="123d9-113">PARAMETERS</span></span>

### <span data-ttu-id="123d9-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="123d9-114">-ApplicationGateway</span></span>
<span data-ttu-id="123d9-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="123d9-115">The applicationGateway</span></span>

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

### <span data-ttu-id="123d9-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="123d9-116">-CertificateFile</span></span>
<span data-ttu-id="123d9-117">신뢰할 수 있는 클라이언트 CA 인증서 체인 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="123d9-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="123d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123d9-118">-DefaultProfile</span></span>
<span data-ttu-id="123d9-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="123d9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="123d9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="123d9-120">-Name</span></span>
<span data-ttu-id="123d9-121">신뢰할 수 있는 클라이언트 CA 인증서 체인의 이름</span><span class="sxs-lookup"><span data-stu-id="123d9-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="123d9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="123d9-122">-Confirm</span></span>
<span data-ttu-id="123d9-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="123d9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="123d9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="123d9-124">-WhatIf</span></span>
<span data-ttu-id="123d9-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="123d9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="123d9-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="123d9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="123d9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123d9-127">CommonParameters</span></span>
<span data-ttu-id="123d9-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="123d9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123d9-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="123d9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123d9-130">입력</span><span class="sxs-lookup"><span data-stu-id="123d9-130">INPUTS</span></span>

### <span data-ttu-id="123d9-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="123d9-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="123d9-132">출력</span><span class="sxs-lookup"><span data-stu-id="123d9-132">OUTPUTS</span></span>

### <span data-ttu-id="123d9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="123d9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="123d9-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="123d9-134">NOTES</span></span>

## <span data-ttu-id="123d9-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="123d9-135">RELATED LINKS</span></span>

[<span data-ttu-id="123d9-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="123d9-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="123d9-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="123d9-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="123d9-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="123d9-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="123d9-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="123d9-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)