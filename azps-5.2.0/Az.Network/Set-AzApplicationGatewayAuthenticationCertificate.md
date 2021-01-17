---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 5af778b84981b5b15acaa688bd8ad1702e5ab7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329709"
---
# <span data-ttu-id="408a7-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="408a7-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="408a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="408a7-102">SYNOPSIS</span></span>
<span data-ttu-id="408a7-103">애플리케이션 게이트웨이에 대한 인증 인증서를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="408a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="408a7-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="408a7-105">설명</span><span class="sxs-lookup"><span data-stu-id="408a7-105">DESCRIPTION</span></span>
<span data-ttu-id="408a7-106">**Set-AzApplicationGatewayAuthenticationCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 인증 인증서를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="408a7-107">예제</span><span class="sxs-lookup"><span data-stu-id="408a7-107">EXAMPLES</span></span>

### <span data-ttu-id="408a7-108">예제 1: 인증 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="408a7-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="408a7-109">첫 번째 명령은 appGwName이라는 애플리케이션 게이트웨이를 다운로드하고 결과를 $appgw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="408a7-110">두 번째 명령은 애플리케이션 게이트웨이에서 cert01이라는 인증 인증서를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="408a7-111">세 번째 명령은 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="408a7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="408a7-112">PARAMETERS</span></span>

### <span data-ttu-id="408a7-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="408a7-113">-ApplicationGateway</span></span>
<span data-ttu-id="408a7-114">이 cmdlet이 인증 인증서를 업데이트하는 애플리케이션 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="408a7-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="408a7-115">-CertificateFile</span></span>
<span data-ttu-id="408a7-116">이 cmdlet이 인증서를 업데이트하는 인증 인증서 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="408a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408a7-117">-DefaultProfile</span></span>
<span data-ttu-id="408a7-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="408a7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="408a7-119">-Name</span></span>
<span data-ttu-id="408a7-120">이 cmdlet이 업데이트하는 인증 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="408a7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="408a7-121">-Confirm</span></span>
<span data-ttu-id="408a7-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="408a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="408a7-123">-WhatIf</span></span>
<span data-ttu-id="408a7-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="408a7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="408a7-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="408a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408a7-126">CommonParameters</span></span>
<span data-ttu-id="408a7-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="408a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408a7-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="408a7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408a7-129">입력</span><span class="sxs-lookup"><span data-stu-id="408a7-129">INPUTS</span></span>

### <span data-ttu-id="408a7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="408a7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="408a7-131">출력</span><span class="sxs-lookup"><span data-stu-id="408a7-131">OUTPUTS</span></span>

### <span data-ttu-id="408a7-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="408a7-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="408a7-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="408a7-133">NOTES</span></span>
* <span data-ttu-id="408a7-134">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="408a7-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="408a7-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="408a7-135">RELATED LINKS</span></span>

[<span data-ttu-id="408a7-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="408a7-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="408a7-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="408a7-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="408a7-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="408a7-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="408a7-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="408a7-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


