---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f040110ea3e00e99b989c07e8757d3c3a0c4b976
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993944"
---
# <span data-ttu-id="b142f-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b142f-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="b142f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b142f-102">SYNOPSIS</span></span>
<span data-ttu-id="b142f-103">Application Gateway에서 특정 이름으로 신뢰할 수 있는 루트 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b142f-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="b142f-104">구문</span><span class="sxs-lookup"><span data-stu-id="b142f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b142f-105">설명</span><span class="sxs-lookup"><span data-stu-id="b142f-105">DESCRIPTION</span></span>
<span data-ttu-id="b142f-106">**Get-AzApplicationGatewayTrustedRootCertificate** cmdlet은 Application Gateway에서 특정 이름으로 신뢰할 수 있는 루트 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b142f-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="b142f-107">예제</span><span class="sxs-lookup"><span data-stu-id="b142f-107">EXAMPLES</span></span>

### <span data-ttu-id="b142f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b142f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="b142f-109">첫 번째 명령은 Application Gateway를 얻게 하여 변수에 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b142f-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="b142f-110">두 번째 명령은 Application Gateway에서 지정된 이름이 있는 신뢰할 수 있는 루트 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b142f-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="b142f-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b142f-111">PARAMETERS</span></span>

### <span data-ttu-id="b142f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b142f-112">-ApplicationGateway</span></span>
<span data-ttu-id="b142f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b142f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b142f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b142f-114">-DefaultProfile</span></span>
<span data-ttu-id="b142f-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b142f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b142f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b142f-116">-Name</span></span>
<span data-ttu-id="b142f-117">TrustedRoot 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="b142f-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="b142f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b142f-118">CommonParameters</span></span>
<span data-ttu-id="b142f-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b142f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b142f-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b142f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b142f-121">입력</span><span class="sxs-lookup"><span data-stu-id="b142f-121">INPUTS</span></span>

### <span data-ttu-id="b142f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b142f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b142f-123">출력</span><span class="sxs-lookup"><span data-stu-id="b142f-123">OUTPUTS</span></span>

### <span data-ttu-id="b142f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b142f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="b142f-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b142f-125">NOTES</span></span>

## <span data-ttu-id="b142f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b142f-126">RELATED LINKS</span></span>

[<span data-ttu-id="b142f-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b142f-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b142f-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b142f-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b142f-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b142f-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b142f-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b142f-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
