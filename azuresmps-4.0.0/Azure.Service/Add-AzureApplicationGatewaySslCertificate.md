---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BA63476C-25CC-444D-AD2C-51BF76374FBC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76ac1f2d1ba5c64fb12bc10320efff8c34538ab8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045736"
---
# <span data-ttu-id="929d7-101">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="929d7-101">Add-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="929d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="929d7-102">SYNOPSIS</span></span>
<span data-ttu-id="929d7-103">응용 프로그램 게이트웨이에 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-103">Adds an SSL certificate to an Application Gateway.</span></span>

## <span data-ttu-id="929d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="929d7-104">SYNTAX</span></span>

```
Add-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String> -Password <String>
 -CertificateFile <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="929d7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="929d7-105">DESCRIPTION</span></span>
<span data-ttu-id="929d7-106">**AzureApplicationGatewaySslCertificate** Cmdlet은 Azure Application GATEWAY에 SSL (Secure Sockets layer) 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-106">The **Add-AzureApplicationGatewaySslCertificate** cmdlet adds a Secure Sockets Layer (SSL) certificate to an Azure Application Gateway.</span></span>

## <span data-ttu-id="929d7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="929d7-107">EXAMPLES</span></span>

### <span data-ttu-id="929d7-108">예제 1: SSL 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="929d7-108">Example 1: Add an SSL certificate</span></span>
```
PS C:\> Add-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13" -Password "password" -CertificateFile "c:\Certs\sslCertificate.pfx"
```

<span data-ttu-id="929d7-109">이 명령은 SslCertificate13 이라는 이름의 SSL 인증서를 ApplicationGateway08 라는 응용 프로그램 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-109">This command adds an SSL certificate named SslCertificate13 to the Application Gateway named ApplicationGateway08.</span></span>
<span data-ttu-id="929d7-110">명령은 인증서 파일의 경로와 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-110">The command specifies the path of the certificate file and the password for the certificate.</span></span>

## <span data-ttu-id="929d7-111">변수</span><span class="sxs-lookup"><span data-stu-id="929d7-111">PARAMETERS</span></span>

### <span data-ttu-id="929d7-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="929d7-112">-CertificateFile</span></span>
<span data-ttu-id="929d7-113">SSL 인증서 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-113">Specifies the path of an SSL certificate file.</span></span>
<span data-ttu-id="929d7-114">이 cmdlet은이 매개 변수에서 지정 하는 파일에 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-114">This cmdlet adds the certificate in the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="929d7-115">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="929d7-115">-CertificateName</span></span>
<span data-ttu-id="929d7-116">SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-116">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="929d7-117">이 cmdlet은이 매개 변수에서 지정 하는 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-117">This cmdlet adds the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="929d7-118">-이름</span><span class="sxs-lookup"><span data-stu-id="929d7-118">-Name</span></span>
<span data-ttu-id="929d7-119">이 cmdlet이 SSL 인증서를 추가 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-119">Specifies the name of the Application Gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="929d7-120">-암호</span><span class="sxs-lookup"><span data-stu-id="929d7-120">-Password</span></span>
<span data-ttu-id="929d7-121">이 cmdlet이 추가 하는 SSL 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-121">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="929d7-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="929d7-122">-Profile</span></span>
<span data-ttu-id="929d7-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="929d7-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="929d7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929d7-125">CommonParameters</span></span>
<span data-ttu-id="929d7-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="929d7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929d7-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="929d7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929d7-128">입력</span><span class="sxs-lookup"><span data-stu-id="929d7-128">INPUTS</span></span>

### <span data-ttu-id="929d7-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="929d7-129">System.String</span></span>

## <span data-ttu-id="929d7-130">출력</span><span class="sxs-lookup"><span data-stu-id="929d7-130">OUTPUTS</span></span>

### <span data-ttu-id="929d7-131">WindowsAzure의. i a m a 관리 응답</span><span class="sxs-lookup"><span data-stu-id="929d7-131">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="929d7-132">상속자</span><span class="sxs-lookup"><span data-stu-id="929d7-132">NOTES</span></span>

## <span data-ttu-id="929d7-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="929d7-133">RELATED LINKS</span></span>

[<span data-ttu-id="929d7-134">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="929d7-134">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="929d7-135">제거-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="929d7-135">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
