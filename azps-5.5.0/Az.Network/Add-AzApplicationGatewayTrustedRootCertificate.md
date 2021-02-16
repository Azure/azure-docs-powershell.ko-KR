---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f5e8624beeb8053cbf054526cddc24c7da6cdf3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192033"
---
# <span data-ttu-id="f1c08-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f1c08-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f1c08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1c08-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c08-103">애플리케이션 게이트웨이에 신뢰할 수 있는 루트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c08-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="f1c08-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1c08-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1c08-105">설명</span><span class="sxs-lookup"><span data-stu-id="f1c08-105">DESCRIPTION</span></span>
<span data-ttu-id="f1c08-106">**Add-AzApplicationGatewayTrustedRootCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 신뢰할 수 있는 루트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c08-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="f1c08-107">예제</span><span class="sxs-lookup"><span data-stu-id="f1c08-107">EXAMPLES</span></span>

### <span data-ttu-id="f1c08-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1c08-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="f1c08-109">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c08-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="f1c08-110">두 번째 명령은 루트 인증서의 경로를 입력으로 사용하여 Application Gateway에 신뢰할 수 있는 새 루트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c08-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="f1c08-111">세 번째 명령은 백end 서버 인증서의 유효성을 검사하기 위해 신뢰할 수 있는 루트 인증서를 사용하여 새 백end http 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f1c08-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="f1c08-112">네 번째 명령은 Application Gateway를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c08-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="f1c08-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1c08-113">PARAMETERS</span></span>

### <span data-ttu-id="f1c08-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1c08-114">-ApplicationGateway</span></span>
<span data-ttu-id="f1c08-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1c08-115">The applicationGateway</span></span>

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

### <span data-ttu-id="f1c08-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f1c08-116">-CertificateFile</span></span>
<span data-ttu-id="f1c08-117">인증서 CER 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="f1c08-117">Path of certificate CER file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c08-118">-DefaultProfile</span></span>
<span data-ttu-id="f1c08-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1c08-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1c08-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f1c08-120">-Name</span></span>
<span data-ttu-id="f1c08-121">TrustedRoot 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="f1c08-121">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c08-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1c08-122">-Confirm</span></span>
<span data-ttu-id="f1c08-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1c08-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c08-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1c08-124">-WhatIf</span></span>
<span data-ttu-id="f1c08-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f1c08-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1c08-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1c08-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c08-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c08-127">CommonParameters</span></span>
<span data-ttu-id="f1c08-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c08-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c08-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f1c08-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c08-130">입력</span><span class="sxs-lookup"><span data-stu-id="f1c08-130">INPUTS</span></span>

### <span data-ttu-id="f1c08-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1c08-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1c08-132">출력</span><span class="sxs-lookup"><span data-stu-id="f1c08-132">OUTPUTS</span></span>

### <span data-ttu-id="f1c08-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1c08-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1c08-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1c08-134">NOTES</span></span>

## <span data-ttu-id="f1c08-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1c08-135">RELATED LINKS</span></span>

[<span data-ttu-id="f1c08-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f1c08-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f1c08-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f1c08-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f1c08-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f1c08-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f1c08-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f1c08-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
