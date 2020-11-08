---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046494"
---
# <span data-ttu-id="14f1a-101">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="14f1a-101">Remove-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="14f1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="14f1a-103">응용 프로그램 게이트웨이에서 SSL 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f1a-103">Removes an SSL certificate from an application gateway.</span></span>

## <span data-ttu-id="14f1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14f1a-104">SYNTAX</span></span>

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="14f1a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="14f1a-105">DESCRIPTION</span></span>
<span data-ttu-id="14f1a-106">**AzureApplicationGatewaySslCertificate** cmdlet은 응용 프로그램 게이트웨이에서 SSL (Secure Sockets layer) 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f1a-106">The **Remove-AzureApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an application gateway.</span></span>

## <span data-ttu-id="14f1a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="14f1a-107">EXAMPLES</span></span>

### <span data-ttu-id="14f1a-108">예제 1: SSL 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="14f1a-108">Example 1: Remove an SSL certificate</span></span>
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="14f1a-109">이 명령은 ApplicationGateway08 이라는 응용 프로그램 게이트웨이에서 SslCertificate13 이라는 이름의 SSL 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f1a-109">This command removes an SSL certificate named SslCertificate13 from the application gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="14f1a-110">변수</span><span class="sxs-lookup"><span data-stu-id="14f1a-110">PARAMETERS</span></span>

### <span data-ttu-id="14f1a-111">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="14f1a-111">-CertificateName</span></span>
<span data-ttu-id="14f1a-112">SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f1a-112">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="14f1a-113">이 cmdlet은이 매개 변수에서 지정 하는 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f1a-113">This cmdlet removes the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="14f1a-114">-이름</span><span class="sxs-lookup"><span data-stu-id="14f1a-114">-Name</span></span>
<span data-ttu-id="14f1a-115">이 cmdlet이 SSL 인증서를 제거 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f1a-115">Specifies the name of the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="14f1a-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="14f1a-116">-Profile</span></span>
<span data-ttu-id="14f1a-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f1a-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14f1a-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="14f1a-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14f1a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f1a-119">CommonParameters</span></span>
<span data-ttu-id="14f1a-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f1a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f1a-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f1a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f1a-122">입력</span><span class="sxs-lookup"><span data-stu-id="14f1a-122">INPUTS</span></span>

### <span data-ttu-id="14f1a-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14f1a-123">System.String</span></span>

## <span data-ttu-id="14f1a-124">출력</span><span class="sxs-lookup"><span data-stu-id="14f1a-124">OUTPUTS</span></span>

### <span data-ttu-id="14f1a-125">WindowsAzure의. i a m a 관리 응답</span><span class="sxs-lookup"><span data-stu-id="14f1a-125">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="14f1a-126">상속자</span><span class="sxs-lookup"><span data-stu-id="14f1a-126">NOTES</span></span>

## <span data-ttu-id="14f1a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14f1a-127">RELATED LINKS</span></span>

[<span data-ttu-id="14f1a-128">추가-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="14f1a-128">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="14f1a-129">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="14f1a-129">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)
