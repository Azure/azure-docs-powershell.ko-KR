---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045664"
---
# <span data-ttu-id="62382-101">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="62382-101">Get-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="62382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62382-102">SYNOPSIS</span></span>
<span data-ttu-id="62382-103">응용 프로그램 게이트웨이 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62382-103">Gets Application Gateway certificates.</span></span>

## <span data-ttu-id="62382-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62382-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="62382-105">설명은</span><span class="sxs-lookup"><span data-stu-id="62382-105">DESCRIPTION</span></span>
<span data-ttu-id="62382-106">**AzureApplicationGatewaySslCertificate** Cmdlet은 Azure Application Gateway에 대 한 SSL (Secure Sockets layer) 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62382-106">The **Get-AzureApplicationGatewaySslCertificate** cmdlet gets Secure Sockets Layer (SSL) certificates for an Azure Application Gateway.</span></span>

## <span data-ttu-id="62382-107">예제의</span><span class="sxs-lookup"><span data-stu-id="62382-107">EXAMPLES</span></span>

### <span data-ttu-id="62382-108">예제 1: SSL 인증서 받기</span><span class="sxs-lookup"><span data-stu-id="62382-108">Example 1: Get an SSL certificate</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="62382-109">이 명령은 ApplicationGateway08 라는 응용 프로그램 게이트웨이에서 SslCertificate13 이라는 이름의 SSL 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62382-109">This command gets an SSL certificate named SslCertificate13 on the Application Gateway named ApplicationGateway08.</span></span>

### <span data-ttu-id="62382-110">예제 2: 모든 SSL 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="62382-110">Example 2: Get all SSL certificates</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

<span data-ttu-id="62382-111">이 명령은 ApplicationGateway08 이라는 응용 프로그램 게이트웨이에서 모든 SSL 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62382-111">This command gets all the SSL certificates on the Application Gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="62382-112">변수</span><span class="sxs-lookup"><span data-stu-id="62382-112">PARAMETERS</span></span>

### <span data-ttu-id="62382-113">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="62382-113">-CertificateName</span></span>
<span data-ttu-id="62382-114">SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62382-114">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="62382-115">이 cmdlet은이 매개 변수에서 지정 하는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62382-115">This cmdlet gets the certificate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62382-116">-이름</span><span class="sxs-lookup"><span data-stu-id="62382-116">-Name</span></span>
<span data-ttu-id="62382-117">이 cmdlet이 SSL 인증서를 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62382-117">Specifies the name of the Application Gateway from which this cmdlet gets an SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62382-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="62382-118">-Profile</span></span>
<span data-ttu-id="62382-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62382-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="62382-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="62382-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62382-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62382-121">CommonParameters</span></span>
<span data-ttu-id="62382-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62382-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62382-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62382-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62382-124">입력</span><span class="sxs-lookup"><span data-stu-id="62382-124">INPUTS</span></span>

### <span data-ttu-id="62382-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62382-125">System.String</span></span>

## <span data-ttu-id="62382-126">출력</span><span class="sxs-lookup"><span data-stu-id="62382-126">OUTPUTS</span></span>

### <span data-ttu-id="62382-127">Microsoft. 네트워킹과. i m m. i m a 인증서의 application<Certificate를 나열 하 고, Microsoft Azure. i m/application></span><span class="sxs-lookup"><span data-stu-id="62382-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate, List<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate></span></span>

## <span data-ttu-id="62382-128">상속자</span><span class="sxs-lookup"><span data-stu-id="62382-128">NOTES</span></span>

## <span data-ttu-id="62382-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62382-129">RELATED LINKS</span></span>

[<span data-ttu-id="62382-130">추가-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="62382-130">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="62382-131">제거-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="62382-131">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
