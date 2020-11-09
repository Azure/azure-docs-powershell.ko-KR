---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 5af778b84981b5b15acaa688bd8ad1702e5ab7e3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311354"
---
# <span data-ttu-id="2cf73-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2cf73-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="2cf73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cf73-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf73-103">Application gateway에 대 한 인증 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="2cf73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2cf73-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cf73-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2cf73-105">DESCRIPTION</span></span>
<span data-ttu-id="2cf73-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 대 한 인증 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="2cf73-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2cf73-107">EXAMPLES</span></span>

### <span data-ttu-id="2cf73-108">예제 1: 인증 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="2cf73-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="2cf73-109">첫 번째 명령은 appGwName 이라는 응용 프로그램 게이트웨이를 가져와 결과를 $appgw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="2cf73-110">두 번째 명령은 응용 프로그램 게이트웨이에서 cert01 이라는 인증 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="2cf73-111">세 번째 명령은 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="2cf73-112">변수</span><span class="sxs-lookup"><span data-stu-id="2cf73-112">PARAMETERS</span></span>

### <span data-ttu-id="2cf73-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cf73-113">-ApplicationGateway</span></span>
<span data-ttu-id="2cf73-114">이 cmdlet이 인증 인증서를 업데이트 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="2cf73-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="2cf73-115">-CertificateFile</span></span>
<span data-ttu-id="2cf73-116">이 cmdlet이 인증서를 업데이트 하는 인증 인증서 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="2cf73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf73-117">-DefaultProfile</span></span>
<span data-ttu-id="2cf73-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cf73-119">-이름</span><span class="sxs-lookup"><span data-stu-id="2cf73-119">-Name</span></span>
<span data-ttu-id="2cf73-120">이 cmdlet이 업데이트 하는 인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="2cf73-121">-확인</span><span class="sxs-lookup"><span data-stu-id="2cf73-121">-Confirm</span></span>
<span data-ttu-id="2cf73-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cf73-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cf73-123">-WhatIf</span></span>
<span data-ttu-id="2cf73-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cf73-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cf73-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf73-126">CommonParameters</span></span>
<span data-ttu-id="2cf73-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf73-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf73-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf73-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf73-129">입력</span><span class="sxs-lookup"><span data-stu-id="2cf73-129">INPUTS</span></span>

### <span data-ttu-id="2cf73-130">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cf73-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2cf73-131">출력</span><span class="sxs-lookup"><span data-stu-id="2cf73-131">OUTPUTS</span></span>

### <span data-ttu-id="2cf73-132">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cf73-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2cf73-133">상속자</span><span class="sxs-lookup"><span data-stu-id="2cf73-133">NOTES</span></span>
* <span data-ttu-id="2cf73-134">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="2cf73-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2cf73-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2cf73-135">RELATED LINKS</span></span>

[<span data-ttu-id="2cf73-136">추가-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2cf73-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2cf73-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2cf73-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2cf73-138">새로운 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2cf73-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2cf73-139">제거-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2cf73-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


