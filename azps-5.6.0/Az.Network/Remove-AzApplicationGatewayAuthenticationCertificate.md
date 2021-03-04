---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: aa8bd1b8850c1aa7f859d1797a961e32c22aa9e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953771"
---
# <span data-ttu-id="53942-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="53942-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="53942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53942-102">SYNOPSIS</span></span>
<span data-ttu-id="53942-103">애플리케이션 게이트웨이에서 인증 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="53942-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="53942-104">구문</span><span class="sxs-lookup"><span data-stu-id="53942-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53942-105">설명</span><span class="sxs-lookup"><span data-stu-id="53942-105">DESCRIPTION</span></span>
<span data-ttu-id="53942-106">**Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에서 인증 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="53942-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="53942-107">예제</span><span class="sxs-lookup"><span data-stu-id="53942-107">EXAMPLES</span></span>

### <span data-ttu-id="53942-108">예제 1: 애플리케이션 게이트웨이에서 인증 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="53942-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="53942-109">첫 번째 명령은 appGwName이라는 애플리케이션 게이트웨이를 얻게 하여 결과를 $appgw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="53942-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="53942-110">두 번째 명령은 애플리케이션 게이트웨이에서 cert01이라는 인증 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="53942-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="53942-111">세 번째 명령은 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="53942-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="53942-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="53942-112">PARAMETERS</span></span>

### <span data-ttu-id="53942-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53942-113">-ApplicationGateway</span></span>
<span data-ttu-id="53942-114">이 cmdlet에서 인증 인증서를 제거하는 애플리케이션 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53942-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="53942-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53942-115">-DefaultProfile</span></span>
<span data-ttu-id="53942-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53942-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53942-117">-Name</span><span class="sxs-lookup"><span data-stu-id="53942-117">-Name</span></span>
<span data-ttu-id="53942-118">이 cmdlet이 제거하는 인증 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53942-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="53942-119">-확인</span><span class="sxs-lookup"><span data-stu-id="53942-119">-Confirm</span></span>
<span data-ttu-id="53942-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="53942-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53942-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53942-121">-WhatIf</span></span>
<span data-ttu-id="53942-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="53942-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53942-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53942-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53942-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53942-124">CommonParameters</span></span>
<span data-ttu-id="53942-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="53942-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53942-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="53942-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53942-127">입력</span><span class="sxs-lookup"><span data-stu-id="53942-127">INPUTS</span></span>

### <span data-ttu-id="53942-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53942-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53942-129">출력</span><span class="sxs-lookup"><span data-stu-id="53942-129">OUTPUTS</span></span>

### <span data-ttu-id="53942-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53942-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53942-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="53942-131">NOTES</span></span>
* <span data-ttu-id="53942-132">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="53942-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="53942-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53942-133">RELATED LINKS</span></span>

[<span data-ttu-id="53942-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="53942-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="53942-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="53942-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="53942-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="53942-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="53942-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="53942-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


