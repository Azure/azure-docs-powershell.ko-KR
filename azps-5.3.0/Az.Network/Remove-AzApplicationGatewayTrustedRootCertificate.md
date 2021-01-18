---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495177"
---
# <span data-ttu-id="af6e1-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="af6e1-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="af6e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="af6e1-103">애플리케이션 게이트웨이에서 신뢰할 수 있는 루트 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="af6e1-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="af6e1-104">구문</span><span class="sxs-lookup"><span data-stu-id="af6e1-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af6e1-105">설명</span><span class="sxs-lookup"><span data-stu-id="af6e1-105">DESCRIPTION</span></span>
<span data-ttu-id="af6e1-106">**Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet은 기존 Application Gateway에서 신뢰할 수 있는 루트 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="af6e1-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="af6e1-107">예제</span><span class="sxs-lookup"><span data-stu-id="af6e1-107">EXAMPLES</span></span>

### <span data-ttu-id="af6e1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="af6e1-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="af6e1-109">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $gw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="af6e1-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="af6e1-110">두 번째 명령은 애플리케이션 게이트웨이에서 myRootCA라는 신뢰할 수 있는 루트 인증서를 $gw.</span><span class="sxs-lookup"><span data-stu-id="af6e1-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="af6e1-111">세 번째 명령은 Azure에서 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="af6e1-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="af6e1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af6e1-112">PARAMETERS</span></span>

### <span data-ttu-id="af6e1-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af6e1-113">-ApplicationGateway</span></span>
<span data-ttu-id="af6e1-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af6e1-114">The applicationGateway</span></span>

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

### <span data-ttu-id="af6e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af6e1-115">-DefaultProfile</span></span>
<span data-ttu-id="af6e1-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af6e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af6e1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="af6e1-117">-Name</span></span>
<span data-ttu-id="af6e1-118">TrustedRoot 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="af6e1-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="af6e1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af6e1-119">-Confirm</span></span>
<span data-ttu-id="af6e1-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af6e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af6e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af6e1-121">-WhatIf</span></span>
<span data-ttu-id="af6e1-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="af6e1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af6e1-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af6e1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af6e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af6e1-124">CommonParameters</span></span>
<span data-ttu-id="af6e1-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af6e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af6e1-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="af6e1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af6e1-127">입력</span><span class="sxs-lookup"><span data-stu-id="af6e1-127">INPUTS</span></span>

### <span data-ttu-id="af6e1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af6e1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="af6e1-129">출력</span><span class="sxs-lookup"><span data-stu-id="af6e1-129">OUTPUTS</span></span>

### <span data-ttu-id="af6e1-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af6e1-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="af6e1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af6e1-131">NOTES</span></span>

## <span data-ttu-id="af6e1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af6e1-132">RELATED LINKS</span></span>

[<span data-ttu-id="af6e1-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="af6e1-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="af6e1-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="af6e1-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="af6e1-135">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="af6e1-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="af6e1-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="af6e1-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
