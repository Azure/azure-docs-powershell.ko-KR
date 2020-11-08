---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f5e8624beeb8053cbf054526cddc24c7da6cdf3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048944"
---
# <span data-ttu-id="3e854-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3e854-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="3e854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e854-102">SYNOPSIS</span></span>
<span data-ttu-id="3e854-103">신뢰할 수 있는 루트 인증서를 응용 프로그램 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="3e854-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3e854-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e854-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3e854-105">DESCRIPTION</span></span>
<span data-ttu-id="3e854-106">**AzApplicationGatewayTrustedRootCertificate** Cmdlet은 Azure application gateway에 신뢰할 수 있는 루트 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="3e854-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3e854-107">EXAMPLES</span></span>

### <span data-ttu-id="3e854-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3e854-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="3e854-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $gw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="3e854-110">두 번째 명령은 신뢰할 수 있는 루트 인증서를 응용 프로그램 게이트웨이에 추가 하 고 루트 인증서를 입력으로 경로를 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="3e854-111">세 번째 명령은 백 엔드 서버 인증서의 유효성을 검사 하기 위해 신뢰할 수 있는 루트 인증서를 사용 하 여 새 백 엔드 http 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="3e854-112">네 번째 명령은 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="3e854-113">변수</span><span class="sxs-lookup"><span data-stu-id="3e854-113">PARAMETERS</span></span>

### <span data-ttu-id="3e854-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e854-114">-ApplicationGateway</span></span>
<span data-ttu-id="3e854-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e854-115">The applicationGateway</span></span>

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

### <span data-ttu-id="3e854-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="3e854-116">-CertificateFile</span></span>
<span data-ttu-id="3e854-117">인증서 CER 파일 경로</span><span class="sxs-lookup"><span data-stu-id="3e854-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="3e854-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e854-118">-DefaultProfile</span></span>
<span data-ttu-id="3e854-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e854-120">-이름</span><span class="sxs-lookup"><span data-stu-id="3e854-120">-Name</span></span>
<span data-ttu-id="3e854-121">(이)가 게 된 루트 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="3e854-122">-확인</span><span class="sxs-lookup"><span data-stu-id="3e854-122">-Confirm</span></span>
<span data-ttu-id="3e854-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e854-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e854-124">-WhatIf</span></span>
<span data-ttu-id="3e854-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e854-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e854-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e854-127">CommonParameters</span></span>
<span data-ttu-id="3e854-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e854-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e854-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e854-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e854-130">입력</span><span class="sxs-lookup"><span data-stu-id="3e854-130">INPUTS</span></span>

### <span data-ttu-id="3e854-131">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e854-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e854-132">출력</span><span class="sxs-lookup"><span data-stu-id="3e854-132">OUTPUTS</span></span>

### <span data-ttu-id="3e854-133">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e854-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e854-134">상속자</span><span class="sxs-lookup"><span data-stu-id="3e854-134">NOTES</span></span>

## <span data-ttu-id="3e854-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e854-135">RELATED LINKS</span></span>

[<span data-ttu-id="3e854-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3e854-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="3e854-137">새로운 AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3e854-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="3e854-138">제거-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3e854-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="3e854-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3e854-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
