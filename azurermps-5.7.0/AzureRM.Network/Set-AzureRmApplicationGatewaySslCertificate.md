---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1af7ef3b60fa296a5fb8190675393a0726d0502b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528020"
---
# <span data-ttu-id="ac283-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ac283-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="ac283-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac283-102">SYNOPSIS</span></span>
<span data-ttu-id="ac283-103">SSL 인증서의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac283-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac283-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac283-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac283-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ac283-105">DESCRIPTION</span></span>
<span data-ttu-id="ac283-106">**AzureRmApplicationGatewaySslCertificate** CMDLET은 SSL 인증서의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac283-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="ac283-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ac283-107">EXAMPLES</span></span>

### <span data-ttu-id="ac283-108">예제 1: SSL 인증서의 목표 상태 설정</span><span class="sxs-lookup"><span data-stu-id="ac283-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="ac283-109">이 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이에서 SSL 인증서에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac283-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="ac283-110">변수</span><span class="sxs-lookup"><span data-stu-id="ac283-110">PARAMETERS</span></span>

### <span data-ttu-id="ac283-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac283-111">-ApplicationGateway</span></span>
<span data-ttu-id="ac283-112">SSL (Secure Socket Layer) 인증서가 연결 되는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac283-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="ac283-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ac283-113">-CertificateFile</span></span>
<span data-ttu-id="ac283-114">SSL 인증서의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac283-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="ac283-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac283-115">-DefaultProfile</span></span>
<span data-ttu-id="ac283-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac283-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac283-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ac283-117">-Name</span></span>
<span data-ttu-id="ac283-118">SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac283-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="ac283-119">-암호</span><span class="sxs-lookup"><span data-stu-id="ac283-119">-Password</span></span>
<span data-ttu-id="ac283-120">SSL 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac283-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="ac283-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac283-121">CommonParameters</span></span>
<span data-ttu-id="ac283-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac283-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac283-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac283-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac283-124">입력</span><span class="sxs-lookup"><span data-stu-id="ac283-124">INPUTS</span></span>

### <span data-ttu-id="ac283-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ac283-125">System.String</span></span>

## <span data-ttu-id="ac283-126">출력</span><span class="sxs-lookup"><span data-stu-id="ac283-126">OUTPUTS</span></span>

### <span data-ttu-id="ac283-127">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac283-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ac283-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ac283-128">NOTES</span></span>

## <span data-ttu-id="ac283-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac283-129">RELATED LINKS</span></span>

[<span data-ttu-id="ac283-130">추가-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ac283-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ac283-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ac283-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ac283-132">새로운 AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ac283-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ac283-133">제거-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ac283-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


