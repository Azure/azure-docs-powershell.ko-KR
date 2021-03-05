---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e8bb89f90772006ceb567ff235746a778c840bdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990052"
---
# <span data-ttu-id="31ee3-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31ee3-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="31ee3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="31ee3-103">애플리케이션 게이트웨이에 신뢰할 수 있는 루트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="31ee3-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="31ee3-104">구문</span><span class="sxs-lookup"><span data-stu-id="31ee3-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31ee3-105">설명</span><span class="sxs-lookup"><span data-stu-id="31ee3-105">DESCRIPTION</span></span>
<span data-ttu-id="31ee3-106">**Add-AzApplicationGatewayTrustedRootCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 신뢰할 수 있는 루트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="31ee3-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="31ee3-107">예제</span><span class="sxs-lookup"><span data-stu-id="31ee3-107">EXAMPLES</span></span>

### <span data-ttu-id="31ee3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="31ee3-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="31ee3-109">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 변수에 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="31ee3-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="31ee3-110">두 번째 명령은 루트 인증서의 경로를 입력으로 취하는 Application Gateway에 새 신뢰할 수 있는 루트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="31ee3-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="31ee3-111">세 번째 명령은 백end 서버 인증서를 유효성 검사하기 위해 신뢰할 수 있는 루트 인증서를 사용하여 새 백end http 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31ee3-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="31ee3-112">네 번째 명령은 Application Gateway를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="31ee3-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="31ee3-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="31ee3-113">PARAMETERS</span></span>

### <span data-ttu-id="31ee3-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31ee3-114">-ApplicationGateway</span></span>
<span data-ttu-id="31ee3-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31ee3-115">The applicationGateway</span></span>

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

### <span data-ttu-id="31ee3-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="31ee3-116">-CertificateFile</span></span>
<span data-ttu-id="31ee3-117">인증서 CER 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="31ee3-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="31ee3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ee3-118">-DefaultProfile</span></span>
<span data-ttu-id="31ee3-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31ee3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31ee3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="31ee3-120">-Name</span></span>
<span data-ttu-id="31ee3-121">TrustedRoot 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="31ee3-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="31ee3-122">-확인</span><span class="sxs-lookup"><span data-stu-id="31ee3-122">-Confirm</span></span>
<span data-ttu-id="31ee3-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="31ee3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31ee3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ee3-124">-WhatIf</span></span>
<span data-ttu-id="31ee3-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="31ee3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31ee3-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31ee3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31ee3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ee3-127">CommonParameters</span></span>
<span data-ttu-id="31ee3-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31ee3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ee3-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="31ee3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ee3-130">입력</span><span class="sxs-lookup"><span data-stu-id="31ee3-130">INPUTS</span></span>

### <span data-ttu-id="31ee3-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31ee3-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="31ee3-132">출력</span><span class="sxs-lookup"><span data-stu-id="31ee3-132">OUTPUTS</span></span>

### <span data-ttu-id="31ee3-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31ee3-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="31ee3-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31ee3-134">NOTES</span></span>

## <span data-ttu-id="31ee3-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31ee3-135">RELATED LINKS</span></span>

[<span data-ttu-id="31ee3-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31ee3-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="31ee3-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31ee3-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="31ee3-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31ee3-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="31ee3-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31ee3-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
