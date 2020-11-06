---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: cd88a6ddf591ec4bace75fec1cb51bf1b4769583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530001"
---
# <span data-ttu-id="2ab91-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ab91-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="2ab91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ab91-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab91-103">Azure application gateway에서 SSL 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ab91-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ab91-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ab91-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ab91-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2ab91-105">DESCRIPTION</span></span>
<span data-ttu-id="2ab91-106">**AzureRmApplicationGatewaySslCertificate** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 SSL (Secure Sockets layer) 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ab91-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="2ab91-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2ab91-107">EXAMPLES</span></span>

### <span data-ttu-id="2ab91-108">예제 1: 응용 프로그램 게이트웨이에서 SSL 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="2ab91-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="2ab91-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ab91-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="2ab91-110">두 번째 명령은 $AppGW 변수에 저장 된 응용 프로그램 게이트웨이에서 Cert02 이라는 이름의 SSL 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ab91-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="2ab91-111">변수</span><span class="sxs-lookup"><span data-stu-id="2ab91-111">PARAMETERS</span></span>

### <span data-ttu-id="2ab91-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ab91-112">-ApplicationGateway</span></span>
<span data-ttu-id="2ab91-113">이 cmdlet이 SSL 인증서를 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ab91-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="2ab91-114">-이름</span><span class="sxs-lookup"><span data-stu-id="2ab91-114">-Name</span></span>
<span data-ttu-id="2ab91-115">이 cmdlet이 제거 하는 SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ab91-115">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2ab91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab91-116">-DefaultProfile</span></span>
<span data-ttu-id="2ab91-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ab91-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ab91-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab91-118">CommonParameters</span></span>
<span data-ttu-id="2ab91-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ab91-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab91-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab91-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab91-121">입력</span><span class="sxs-lookup"><span data-stu-id="2ab91-121">INPUTS</span></span>

### <span data-ttu-id="2ab91-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2ab91-122">System.String</span></span>

## <span data-ttu-id="2ab91-123">출력</span><span class="sxs-lookup"><span data-stu-id="2ab91-123">OUTPUTS</span></span>

### <span data-ttu-id="2ab91-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ab91-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2ab91-125">상속자</span><span class="sxs-lookup"><span data-stu-id="2ab91-125">NOTES</span></span>

## <span data-ttu-id="2ab91-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ab91-126">RELATED LINKS</span></span>

[<span data-ttu-id="2ab91-127">추가-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ab91-127">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2ab91-128">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ab91-128">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2ab91-129">새로운 AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ab91-129">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2ab91-130">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ab91-130">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


