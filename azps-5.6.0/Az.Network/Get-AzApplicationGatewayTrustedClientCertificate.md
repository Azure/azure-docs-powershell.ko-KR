---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: b9522cf7bc29f01215cbac7473c58643b8d63b5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993953"
---
# <span data-ttu-id="e3f97-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f97-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="e3f97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3f97-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f97-103">Application Gateway에서 특정 이름으로 신뢰할 수 있는 클라이언트 CA 인증서 체인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e3f97-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="e3f97-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3f97-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3f97-105">설명</span><span class="sxs-lookup"><span data-stu-id="e3f97-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f97-106">Get-AzApplicationGatewayTrustedClientCertificate cmdlet은 Application Gateway에서 특정 이름으로 신뢰할 수 있는 클라이언트 CA 인증서 체인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e3f97-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="e3f97-107">예제</span><span class="sxs-lookup"><span data-stu-id="e3f97-107">EXAMPLES</span></span>

### <span data-ttu-id="e3f97-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3f97-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="e3f97-109">첫 번째 명령은 Application Gateway를 얻게 하여 변수에 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f97-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="e3f97-110">두 번째 명령은 Application Gateway에서 지정된 이름으로 신뢰할 수 있는 클라이언트 CA 인증서 체인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e3f97-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="e3f97-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e3f97-111">PARAMETERS</span></span>

### <span data-ttu-id="e3f97-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3f97-112">-ApplicationGateway</span></span>
<span data-ttu-id="e3f97-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3f97-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f97-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f97-114">-DefaultProfile</span></span>
<span data-ttu-id="e3f97-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3f97-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f97-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e3f97-116">-Name</span></span>
<span data-ttu-id="e3f97-117">신뢰할 수 있는 클라이언트 CA 인증서 체인의 이름</span><span class="sxs-lookup"><span data-stu-id="e3f97-117">The name of the trusted client CA certificate chain</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f97-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f97-118">CommonParameters</span></span>
<span data-ttu-id="e3f97-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f97-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f97-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3f97-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f97-121">입력</span><span class="sxs-lookup"><span data-stu-id="e3f97-121">INPUTS</span></span>

### <span data-ttu-id="e3f97-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3f97-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3f97-123">출력</span><span class="sxs-lookup"><span data-stu-id="e3f97-123">OUTPUTS</span></span>

### <span data-ttu-id="e3f97-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f97-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="e3f97-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3f97-125">NOTES</span></span>

## <span data-ttu-id="e3f97-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3f97-126">RELATED LINKS</span></span>

[<span data-ttu-id="e3f97-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f97-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="e3f97-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f97-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="e3f97-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f97-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="e3f97-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f97-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)