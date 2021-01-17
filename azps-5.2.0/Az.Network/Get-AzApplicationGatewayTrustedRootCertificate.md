---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338001"
---
# <span data-ttu-id="4687f-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4687f-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="4687f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4687f-102">SYNOPSIS</span></span>
<span data-ttu-id="4687f-103">Application Gateway에서 특정 이름으로 신뢰할 수 있는 루트 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4687f-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="4687f-104">구문</span><span class="sxs-lookup"><span data-stu-id="4687f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4687f-105">설명</span><span class="sxs-lookup"><span data-stu-id="4687f-105">DESCRIPTION</span></span>
<span data-ttu-id="4687f-106">**Get-AzApplicationGatewayTrustedRootCertificate** cmdlet은 Application Gateway에서 특정 이름으로 신뢰할 수 있는 루트 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4687f-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="4687f-107">예제</span><span class="sxs-lookup"><span data-stu-id="4687f-107">EXAMPLES</span></span>

### <span data-ttu-id="4687f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4687f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="4687f-109">첫 번째 명령은 Application Gateway를 사용하여 애플리케이션 게이트웨이를 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4687f-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="4687f-110">두 번째 명령은 Application Gateway에서 지정된 이름의 신뢰할 수 있는 루트 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4687f-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="4687f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4687f-111">PARAMETERS</span></span>

### <span data-ttu-id="4687f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4687f-112">-ApplicationGateway</span></span>
<span data-ttu-id="4687f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4687f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="4687f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4687f-114">-DefaultProfile</span></span>
<span data-ttu-id="4687f-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4687f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4687f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4687f-116">-Name</span></span>
<span data-ttu-id="4687f-117">TrustedRoot 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="4687f-117">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4687f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4687f-118">CommonParameters</span></span>
<span data-ttu-id="4687f-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4687f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4687f-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4687f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4687f-121">입력</span><span class="sxs-lookup"><span data-stu-id="4687f-121">INPUTS</span></span>

### <span data-ttu-id="4687f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4687f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4687f-123">출력</span><span class="sxs-lookup"><span data-stu-id="4687f-123">OUTPUTS</span></span>

### <span data-ttu-id="4687f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4687f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="4687f-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4687f-125">NOTES</span></span>

## <span data-ttu-id="4687f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4687f-126">RELATED LINKS</span></span>

[<span data-ttu-id="4687f-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4687f-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="4687f-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4687f-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="4687f-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4687f-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="4687f-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4687f-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
