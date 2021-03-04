---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 3c9b9b97e26738234acdf2c8f09c0e1da5eae2e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952144"
---
# <span data-ttu-id="2817d-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2817d-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="2817d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2817d-102">SYNOPSIS</span></span>
<span data-ttu-id="2817d-103">애플리케이션 게이트웨이의 신뢰할 수 있는 클라이언트 CA 인증서 체인을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2817d-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="2817d-104">구문</span><span class="sxs-lookup"><span data-stu-id="2817d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2817d-105">설명</span><span class="sxs-lookup"><span data-stu-id="2817d-105">DESCRIPTION</span></span>
<span data-ttu-id="2817d-106">**Set-AzApplicationGatewayTrustedClientCertificate** cmdlet은 애플리케이션 게이트웨이의 신뢰할 수 있는 클라이언트 CA 인증서 체인을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2817d-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="2817d-107">예제</span><span class="sxs-lookup"><span data-stu-id="2817d-107">EXAMPLES</span></span>

### <span data-ttu-id="2817d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2817d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="2817d-109">위의 예제 시나리오에서는 기존 신뢰할 수 있는 클라이언트 CA 인증서 체인 개체를 업데이트하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2817d-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="2817d-110">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 $gw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2817d-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="2817d-111">두 번째 명령은 새 CA 인증서 체인 파일을 사용하여 기존 신뢰할 수 있는 클라이언트 CA 인증서 체인 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2817d-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="2817d-112">세 번째 명령은 Azure에서 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2817d-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="2817d-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2817d-113">PARAMETERS</span></span>

### <span data-ttu-id="2817d-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2817d-114">-ApplicationGateway</span></span>
<span data-ttu-id="2817d-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2817d-115">The applicationGateway</span></span>

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

### <span data-ttu-id="2817d-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="2817d-116">-CertificateFile</span></span>
<span data-ttu-id="2817d-117">신뢰할 수 있는 클라이언트 CA 인증서 체인 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="2817d-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="2817d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2817d-118">-DefaultProfile</span></span>
<span data-ttu-id="2817d-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2817d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2817d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2817d-120">-Name</span></span>
<span data-ttu-id="2817d-121">신뢰할 수 있는 클라이언트 CA 인증서 체인의 이름</span><span class="sxs-lookup"><span data-stu-id="2817d-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="2817d-122">-확인</span><span class="sxs-lookup"><span data-stu-id="2817d-122">-Confirm</span></span>
<span data-ttu-id="2817d-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2817d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2817d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2817d-124">-WhatIf</span></span>
<span data-ttu-id="2817d-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2817d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2817d-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2817d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2817d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2817d-127">CommonParameters</span></span>
<span data-ttu-id="2817d-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2817d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2817d-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2817d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2817d-130">입력</span><span class="sxs-lookup"><span data-stu-id="2817d-130">INPUTS</span></span>

### <span data-ttu-id="2817d-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2817d-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2817d-132">출력</span><span class="sxs-lookup"><span data-stu-id="2817d-132">OUTPUTS</span></span>

### <span data-ttu-id="2817d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2817d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2817d-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2817d-134">NOTES</span></span>

## <span data-ttu-id="2817d-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2817d-135">RELATED LINKS</span></span>

[<span data-ttu-id="2817d-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2817d-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="2817d-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2817d-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="2817d-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2817d-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="2817d-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2817d-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)