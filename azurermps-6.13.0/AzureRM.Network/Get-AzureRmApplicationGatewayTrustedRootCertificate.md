---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c37c55539f983b490c917e1fe062f14b252ee477
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703451"
---
# <span data-ttu-id="41fb2-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="41fb2-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="41fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="41fb2-103">응용 프로그램 게이트웨이에서 특정 이름의 신뢰할 수 있는 루트 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41fb2-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41fb2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41fb2-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41fb2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="41fb2-105">DESCRIPTION</span></span>
<span data-ttu-id="41fb2-106">**AzureRmApplicationGatewayTrustedRootCertificate** Cmdlet은 응용 프로그램 게이트웨이에서 특정 이름을 갖는 신뢰할 수 있는 루트 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41fb2-106">The **Get-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="41fb2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="41fb2-107">EXAMPLES</span></span>

### <span data-ttu-id="41fb2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="41fb2-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="41fb2-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $gw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="41fb2-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="41fb2-110">두 번째 명령은 응용 프로그램 게이트웨이에서 지정 된 이름의 신뢰할 수 있는 루트 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41fb2-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="41fb2-111">변수</span><span class="sxs-lookup"><span data-stu-id="41fb2-111">PARAMETERS</span></span>

### <span data-ttu-id="41fb2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41fb2-112">-ApplicationGateway</span></span>
<span data-ttu-id="41fb2-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41fb2-113">The applicationGateway</span></span>

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

### <span data-ttu-id="41fb2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41fb2-114">-DefaultProfile</span></span>
<span data-ttu-id="41fb2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41fb2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41fb2-116">-이름</span><span class="sxs-lookup"><span data-stu-id="41fb2-116">-Name</span></span>
<span data-ttu-id="41fb2-117">(이)가 게 된 루트 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41fb2-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="41fb2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41fb2-118">CommonParameters</span></span>
<span data-ttu-id="41fb2-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41fb2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41fb2-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41fb2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41fb2-121">입력</span><span class="sxs-lookup"><span data-stu-id="41fb2-121">INPUTS</span></span>

### <span data-ttu-id="41fb2-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41fb2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="41fb2-123">출력</span><span class="sxs-lookup"><span data-stu-id="41fb2-123">OUTPUTS</span></span>

### <span data-ttu-id="41fb2-124">Microsoft. 네트워크. Psapplication게이트웨이를 위한 Rootcertificate</span><span class="sxs-lookup"><span data-stu-id="41fb2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="41fb2-125">상속자</span><span class="sxs-lookup"><span data-stu-id="41fb2-125">NOTES</span></span>

## <span data-ttu-id="41fb2-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41fb2-126">RELATED LINKS</span></span>
