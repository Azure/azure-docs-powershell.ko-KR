---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 02416fdb18f01c9a2af6c091b0be109b479ce45d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042056"
---
# <span data-ttu-id="ee8eb-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee8eb-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ee8eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee8eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8eb-103">응용 프로그램 게이트웨이에서 인증 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="ee8eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee8eb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee8eb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ee8eb-105">DESCRIPTION</span></span>
<span data-ttu-id="ee8eb-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에서 인증 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="ee8eb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ee8eb-107">EXAMPLES</span></span>

### <span data-ttu-id="ee8eb-108">예제 1: 응용 프로그램 게이트웨이에서 인증 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="ee8eb-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="ee8eb-109">첫 번째 명령은 appGwName 이라는 응용 프로그램 게이트웨이를 가져와 결과를 $appgw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="ee8eb-110">두 번째 명령은 응용 프로그램 게이트웨이에서 cert01 이라는 인증 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="ee8eb-111">세 번째 명령은 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="ee8eb-112">변수</span><span class="sxs-lookup"><span data-stu-id="ee8eb-112">PARAMETERS</span></span>

### <span data-ttu-id="ee8eb-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee8eb-113">-ApplicationGateway</span></span>
<span data-ttu-id="ee8eb-114">이 cmdlet에서 인증 인증서를 제거 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="ee8eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee8eb-115">-DefaultProfile</span></span>
<span data-ttu-id="ee8eb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee8eb-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ee8eb-117">-Name</span></span>
<span data-ttu-id="ee8eb-118">이 cmdlet이 제거 하는 인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ee8eb-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ee8eb-119">-Confirm</span></span>
<span data-ttu-id="ee8eb-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee8eb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee8eb-121">-WhatIf</span></span>
<span data-ttu-id="ee8eb-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee8eb-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee8eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8eb-124">CommonParameters</span></span>
<span data-ttu-id="ee8eb-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee8eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8eb-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee8eb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8eb-127">입력</span><span class="sxs-lookup"><span data-stu-id="ee8eb-127">INPUTS</span></span>

### <span data-ttu-id="ee8eb-128">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee8eb-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ee8eb-129">출력</span><span class="sxs-lookup"><span data-stu-id="ee8eb-129">OUTPUTS</span></span>

### <span data-ttu-id="ee8eb-130">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee8eb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ee8eb-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ee8eb-131">NOTES</span></span>
* <span data-ttu-id="ee8eb-132">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="ee8eb-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ee8eb-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee8eb-133">RELATED LINKS</span></span>

[<span data-ttu-id="ee8eb-134">추가-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee8eb-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ee8eb-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee8eb-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ee8eb-136">새로운 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee8eb-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ee8eb-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee8eb-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


