---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: fc4457e23f50dea3d70a3af2115a93e460dc6a1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534272"
---
# <span data-ttu-id="9d86b-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9d86b-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9d86b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d86b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d86b-103">응용 프로그램 게이트웨이에 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d86b-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d86b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9d86b-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d86b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9d86b-105">DESCRIPTION</span></span>
<span data-ttu-id="9d86b-106">**Add-AzureRmApplicationGatewaySslCertificate** cmdlet은 응용 프로그램 게이트웨이에 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d86b-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="9d86b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9d86b-107">EXAMPLES</span></span>

### <span data-ttu-id="9d86b-108">예제 1: 응용 프로그램 게이트웨이에 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d86b-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="9d86b-109">이 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져온 다음 Cert01 라는 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d86b-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="9d86b-110">변수</span><span class="sxs-lookup"><span data-stu-id="9d86b-110">PARAMETERS</span></span>

### <span data-ttu-id="9d86b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d86b-111">-ApplicationGateway</span></span>
<span data-ttu-id="9d86b-112">이 cmdlet이 SSL 인증서를 추가 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d86b-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="9d86b-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9d86b-113">-CertificateFile</span></span>
<span data-ttu-id="9d86b-114">이 cmdlet에 추가 되는 SSL 인증서의 .pfx 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d86b-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9d86b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d86b-115">-DefaultProfile</span></span>
<span data-ttu-id="9d86b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9d86b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d86b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="9d86b-117">-Name</span></span>
<span data-ttu-id="9d86b-118">이 cmdlet에 추가 되는 SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d86b-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9d86b-119">-암호</span><span class="sxs-lookup"><span data-stu-id="9d86b-119">-Password</span></span>
<span data-ttu-id="9d86b-120">이 cmdlet이 추가 하는 SSL 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d86b-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d86b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d86b-121">CommonParameters</span></span>
<span data-ttu-id="9d86b-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d86b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d86b-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d86b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d86b-124">입력</span><span class="sxs-lookup"><span data-stu-id="9d86b-124">INPUTS</span></span>

### <span data-ttu-id="9d86b-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d86b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="9d86b-126">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9d86b-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="9d86b-127">출력</span><span class="sxs-lookup"><span data-stu-id="9d86b-127">OUTPUTS</span></span>

### <span data-ttu-id="9d86b-128">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d86b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d86b-129">상속자</span><span class="sxs-lookup"><span data-stu-id="9d86b-129">NOTES</span></span>

## <span data-ttu-id="9d86b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d86b-130">RELATED LINKS</span></span>

[<span data-ttu-id="9d86b-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9d86b-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9d86b-132">새로운 AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9d86b-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9d86b-133">제거-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9d86b-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9d86b-134">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9d86b-134">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


