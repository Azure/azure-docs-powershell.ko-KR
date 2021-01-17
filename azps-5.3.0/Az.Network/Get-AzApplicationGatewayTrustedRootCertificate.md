---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380206"
---
# <span data-ttu-id="14e0b-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="14e0b-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="14e0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="14e0b-103">Application Gateway에서 특정 이름으로 신뢰할 수 있는 루트 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14e0b-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="14e0b-104">구문</span><span class="sxs-lookup"><span data-stu-id="14e0b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14e0b-105">설명</span><span class="sxs-lookup"><span data-stu-id="14e0b-105">DESCRIPTION</span></span>
<span data-ttu-id="14e0b-106">**Get-AzApplicationGatewayTrustedRootCertificate** cmdlet은 Application Gateway에서 특정 이름으로 신뢰할 수 있는 루트 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14e0b-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="14e0b-107">예제</span><span class="sxs-lookup"><span data-stu-id="14e0b-107">EXAMPLES</span></span>

### <span data-ttu-id="14e0b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="14e0b-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="14e0b-109">첫 번째 명령은 Application Gateway를 사용하여 애플리케이션 게이트웨이를 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="14e0b-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="14e0b-110">두 번째 명령은 Application Gateway에서 지정된 이름의 신뢰할 수 있는 루트 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14e0b-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="14e0b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14e0b-111">PARAMETERS</span></span>

### <span data-ttu-id="14e0b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14e0b-112">-ApplicationGateway</span></span>
<span data-ttu-id="14e0b-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14e0b-113">The applicationGateway</span></span>

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

### <span data-ttu-id="14e0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e0b-114">-DefaultProfile</span></span>
<span data-ttu-id="14e0b-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14e0b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14e0b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="14e0b-116">-Name</span></span>
<span data-ttu-id="14e0b-117">TrustedRoot 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="14e0b-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="14e0b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e0b-118">CommonParameters</span></span>
<span data-ttu-id="14e0b-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14e0b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e0b-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14e0b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e0b-121">입력</span><span class="sxs-lookup"><span data-stu-id="14e0b-121">INPUTS</span></span>

### <span data-ttu-id="14e0b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14e0b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14e0b-123">출력</span><span class="sxs-lookup"><span data-stu-id="14e0b-123">OUTPUTS</span></span>

### <span data-ttu-id="14e0b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="14e0b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="14e0b-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14e0b-125">NOTES</span></span>

## <span data-ttu-id="14e0b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14e0b-126">RELATED LINKS</span></span>

[<span data-ttu-id="14e0b-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="14e0b-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="14e0b-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="14e0b-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="14e0b-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="14e0b-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="14e0b-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="14e0b-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
