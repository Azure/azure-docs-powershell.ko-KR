---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 687752d74e13030cd954736132dba845c2c55127
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380381"
---
# <span data-ttu-id="30d71-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="30d71-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="30d71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30d71-102">SYNOPSIS</span></span>
<span data-ttu-id="30d71-103">애플리케이션 게이트웨이에 인증 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="30d71-104">구문</span><span class="sxs-lookup"><span data-stu-id="30d71-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30d71-105">설명</span><span class="sxs-lookup"><span data-stu-id="30d71-105">DESCRIPTION</span></span>
<span data-ttu-id="30d71-106">**Add-AzApplicationGatewayAuthenticationCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 인증 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="30d71-107">예제</span><span class="sxs-lookup"><span data-stu-id="30d71-107">EXAMPLES</span></span>

### <span data-ttu-id="30d71-108">예제 1: 애플리케이션 게이트웨이에 인증 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="30d71-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="30d71-109">첫 번째 명령은 appGwName이라는 애플리케이션 게이트웨이를 $appgw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="30d71-110">두 번째 명령은 애플리케이션 게이트웨이에 cert01이라는 인증 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="30d71-111">세 번째 명령은 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="30d71-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30d71-112">PARAMETERS</span></span>

### <span data-ttu-id="30d71-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30d71-113">-ApplicationGateway</span></span>
<span data-ttu-id="30d71-114">이 cmdlet에서 인증 인증서를 추가하는 애플리케이션 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="30d71-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="30d71-115">-CertificateFile</span></span>
<span data-ttu-id="30d71-116">이 cmdlet이 추가하는 인증 인증서의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="30d71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d71-117">-DefaultProfile</span></span>
<span data-ttu-id="30d71-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30d71-119">-Name</span><span class="sxs-lookup"><span data-stu-id="30d71-119">-Name</span></span>
<span data-ttu-id="30d71-120">이 cmdlet이 애플리케이션 게이트웨이에 추가하는 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="30d71-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30d71-121">-Confirm</span></span>
<span data-ttu-id="30d71-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30d71-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30d71-123">-WhatIf</span></span>
<span data-ttu-id="30d71-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="30d71-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30d71-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30d71-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d71-126">CommonParameters</span></span>
<span data-ttu-id="30d71-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30d71-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d71-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="30d71-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d71-129">입력</span><span class="sxs-lookup"><span data-stu-id="30d71-129">INPUTS</span></span>

### <span data-ttu-id="30d71-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30d71-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30d71-131">출력</span><span class="sxs-lookup"><span data-stu-id="30d71-131">OUTPUTS</span></span>

### <span data-ttu-id="30d71-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30d71-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30d71-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="30d71-133">NOTES</span></span>
* <span data-ttu-id="30d71-134">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="30d71-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="30d71-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30d71-135">RELATED LINKS</span></span>

[<span data-ttu-id="30d71-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="30d71-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="30d71-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="30d71-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="30d71-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="30d71-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="30d71-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="30d71-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


