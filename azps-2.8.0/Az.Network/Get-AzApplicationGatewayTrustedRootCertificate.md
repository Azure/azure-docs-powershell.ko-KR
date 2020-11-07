---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 1e617ef1283937116bd97c24a968f247fa7552de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870762"
---
# <span data-ttu-id="089f4-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="089f4-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="089f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="089f4-102">SYNOPSIS</span></span>
<span data-ttu-id="089f4-103">응용 프로그램 게이트웨이에서 특정 이름의 신뢰할 수 있는 루트 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="089f4-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="089f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="089f4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="089f4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="089f4-105">DESCRIPTION</span></span>
<span data-ttu-id="089f4-106">**AzApplicationGatewayTrustedRootCertificate** Cmdlet은 응용 프로그램 게이트웨이에서 특정 이름을 갖는 신뢰할 수 있는 루트 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="089f4-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="089f4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="089f4-107">EXAMPLES</span></span>

### <span data-ttu-id="089f4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="089f4-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="089f4-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $gw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="089f4-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="089f4-110">두 번째 명령은 응용 프로그램 게이트웨이에서 지정 된 이름의 신뢰할 수 있는 루트 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="089f4-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="089f4-111">변수</span><span class="sxs-lookup"><span data-stu-id="089f4-111">PARAMETERS</span></span>

### <span data-ttu-id="089f4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="089f4-112">-ApplicationGateway</span></span>
<span data-ttu-id="089f4-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="089f4-113">The applicationGateway</span></span>

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

### <span data-ttu-id="089f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089f4-114">-DefaultProfile</span></span>
<span data-ttu-id="089f4-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="089f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="089f4-116">-이름</span><span class="sxs-lookup"><span data-stu-id="089f4-116">-Name</span></span>
<span data-ttu-id="089f4-117">(이)가 게 된 루트 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="089f4-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="089f4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089f4-118">CommonParameters</span></span>
<span data-ttu-id="089f4-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="089f4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089f4-120">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="089f4-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089f4-121">입력</span><span class="sxs-lookup"><span data-stu-id="089f4-121">INPUTS</span></span>

### <span data-ttu-id="089f4-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="089f4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="089f4-123">출력</span><span class="sxs-lookup"><span data-stu-id="089f4-123">OUTPUTS</span></span>

### <span data-ttu-id="089f4-124">Microsoft. 네트워크. Psapplication게이트웨이를 위한 Rootcertificate</span><span class="sxs-lookup"><span data-stu-id="089f4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="089f4-125">상속자</span><span class="sxs-lookup"><span data-stu-id="089f4-125">NOTES</span></span>

## <span data-ttu-id="089f4-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="089f4-126">RELATED LINKS</span></span>

[<span data-ttu-id="089f4-127">추가-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="089f4-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="089f4-128">새로운 AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="089f4-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="089f4-129">제거-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="089f4-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="089f4-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="089f4-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
