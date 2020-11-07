---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1a1d484d3b8d23633393c0f300f84091b06c1d0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870918"
---
# <span data-ttu-id="ce74c-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce74c-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ce74c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce74c-102">SYNOPSIS</span></span>
<span data-ttu-id="ce74c-103">응용 프로그램 게이트웨이에 인증 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="ce74c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce74c-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce74c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce74c-105">DESCRIPTION</span></span>
<span data-ttu-id="ce74c-106">**Add-AzApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 인증 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="ce74c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ce74c-107">EXAMPLES</span></span>

### <span data-ttu-id="ce74c-108">예제 1: 응용 프로그램 게이트웨이에 인증 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="ce74c-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="ce74c-109">첫 번째 명령은 appGwName 이라는 응용 프로그램 게이트웨이를 가져와이를 $appgw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="ce74c-110">두 번째 명령은 cert01 이라는 인증 인증서를 응용 프로그램 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="ce74c-111">세 번째 명령은 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="ce74c-112">변수</span><span class="sxs-lookup"><span data-stu-id="ce74c-112">PARAMETERS</span></span>

### <span data-ttu-id="ce74c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce74c-113">-ApplicationGateway</span></span>
<span data-ttu-id="ce74c-114">이 cmdlet이 인증 인증서를 추가 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="ce74c-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ce74c-115">-CertificateFile</span></span>
<span data-ttu-id="ce74c-116">이 cmdlet이 추가 하는 인증 인증서의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="ce74c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce74c-117">-DefaultProfile</span></span>
<span data-ttu-id="ce74c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce74c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ce74c-119">-Name</span></span>
<span data-ttu-id="ce74c-120">이 cmdlet이 응용 프로그램 게이트웨이에 추가 하는 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="ce74c-121">-확인</span><span class="sxs-lookup"><span data-stu-id="ce74c-121">-Confirm</span></span>
<span data-ttu-id="ce74c-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce74c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce74c-123">-WhatIf</span></span>
<span data-ttu-id="ce74c-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce74c-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce74c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce74c-126">CommonParameters</span></span>
<span data-ttu-id="ce74c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce74c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce74c-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce74c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce74c-129">입력</span><span class="sxs-lookup"><span data-stu-id="ce74c-129">INPUTS</span></span>

### <span data-ttu-id="ce74c-130">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce74c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ce74c-131">출력</span><span class="sxs-lookup"><span data-stu-id="ce74c-131">OUTPUTS</span></span>

### <span data-ttu-id="ce74c-132">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce74c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ce74c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="ce74c-133">NOTES</span></span>
* <span data-ttu-id="ce74c-134">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="ce74c-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ce74c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce74c-135">RELATED LINKS</span></span>

[<span data-ttu-id="ce74c-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce74c-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ce74c-137">새로운 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce74c-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ce74c-138">제거-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce74c-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ce74c-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce74c-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


