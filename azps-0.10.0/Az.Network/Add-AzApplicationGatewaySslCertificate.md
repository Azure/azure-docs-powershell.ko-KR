---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 964e99912e4f21d48e89b725da1aa44ac32ea186
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875688"
---
# <span data-ttu-id="94243-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="94243-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="94243-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94243-102">SYNOPSIS</span></span>
<span data-ttu-id="94243-103">응용 프로그램 게이트웨이에 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="94243-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="94243-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94243-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94243-105">설명은</span><span class="sxs-lookup"><span data-stu-id="94243-105">DESCRIPTION</span></span>
<span data-ttu-id="94243-106">**Add-AzApplicationGatewaySslCertificate** cmdlet은 응용 프로그램 게이트웨이에 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="94243-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="94243-107">예제의</span><span class="sxs-lookup"><span data-stu-id="94243-107">EXAMPLES</span></span>

### <span data-ttu-id="94243-108">예제 1: 응용 프로그램 게이트웨이에 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="94243-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="94243-109">이 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져온 다음 Cert01 라는 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="94243-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="94243-110">변수</span><span class="sxs-lookup"><span data-stu-id="94243-110">PARAMETERS</span></span>

### <span data-ttu-id="94243-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94243-111">-ApplicationGateway</span></span>
<span data-ttu-id="94243-112">이 cmdlet이 SSL 인증서를 추가 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94243-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="94243-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="94243-113">-CertificateFile</span></span>
<span data-ttu-id="94243-114">이 cmdlet에 추가 되는 SSL 인증서의 .pfx 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94243-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94243-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94243-115">-DefaultProfile</span></span>
<span data-ttu-id="94243-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94243-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94243-117">-이름</span><span class="sxs-lookup"><span data-stu-id="94243-117">-Name</span></span>
<span data-ttu-id="94243-118">이 cmdlet에 추가 되는 SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94243-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94243-119">-암호</span><span class="sxs-lookup"><span data-stu-id="94243-119">-Password</span></span>
<span data-ttu-id="94243-120">이 cmdlet이 추가 하는 SSL 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94243-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94243-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94243-121">CommonParameters</span></span>
<span data-ttu-id="94243-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94243-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94243-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94243-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94243-124">입력</span><span class="sxs-lookup"><span data-stu-id="94243-124">INPUTS</span></span>

### <span data-ttu-id="94243-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="94243-125">System.String</span></span>

## <span data-ttu-id="94243-126">출력</span><span class="sxs-lookup"><span data-stu-id="94243-126">OUTPUTS</span></span>

### <span data-ttu-id="94243-127">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94243-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="94243-128">상속자</span><span class="sxs-lookup"><span data-stu-id="94243-128">NOTES</span></span>

## <span data-ttu-id="94243-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94243-129">RELATED LINKS</span></span>

[<span data-ttu-id="94243-130">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="94243-130">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="94243-131">새로운 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="94243-131">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="94243-132">제거-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="94243-132">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="94243-133">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="94243-133">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


