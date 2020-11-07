---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: cec5a6aa0b61889e7923ebce67d1247f99d215e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710984"
---
# <span data-ttu-id="07d91-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="07d91-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="07d91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07d91-102">SYNOPSIS</span></span>
<span data-ttu-id="07d91-103">SSL 인증서의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d91-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07d91-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07d91-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07d91-105">설명은</span><span class="sxs-lookup"><span data-stu-id="07d91-105">DESCRIPTION</span></span>
<span data-ttu-id="07d91-106">**AzureRmApplicationGatewaySslCertificate** CMDLET은 SSL 인증서의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d91-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="07d91-107">예제의</span><span class="sxs-lookup"><span data-stu-id="07d91-107">EXAMPLES</span></span>

### <span data-ttu-id="07d91-108">예제 1: SSL 인증서의 목표 상태 설정</span><span class="sxs-lookup"><span data-stu-id="07d91-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="07d91-109">이 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이에서 SSL 인증서에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d91-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="07d91-110">변수</span><span class="sxs-lookup"><span data-stu-id="07d91-110">PARAMETERS</span></span>

### <span data-ttu-id="07d91-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07d91-111">-ApplicationGateway</span></span>
<span data-ttu-id="07d91-112">SSL (Secure Socket Layer) 인증서가 연결 되는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d91-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="07d91-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="07d91-113">-CertificateFile</span></span>
<span data-ttu-id="07d91-114">SSL 인증서의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d91-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="07d91-115">-이름</span><span class="sxs-lookup"><span data-stu-id="07d91-115">-Name</span></span>
<span data-ttu-id="07d91-116">SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d91-116">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="07d91-117">-암호</span><span class="sxs-lookup"><span data-stu-id="07d91-117">-Password</span></span>
<span data-ttu-id="07d91-118">SSL 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d91-118">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="07d91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d91-119">-DefaultProfile</span></span>
<span data-ttu-id="07d91-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07d91-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07d91-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d91-121">CommonParameters</span></span>
<span data-ttu-id="07d91-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d91-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d91-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d91-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d91-124">입력</span><span class="sxs-lookup"><span data-stu-id="07d91-124">INPUTS</span></span>

### <span data-ttu-id="07d91-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="07d91-125">System.String</span></span>

## <span data-ttu-id="07d91-126">출력</span><span class="sxs-lookup"><span data-stu-id="07d91-126">OUTPUTS</span></span>

### <span data-ttu-id="07d91-127">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07d91-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="07d91-128">상속자</span><span class="sxs-lookup"><span data-stu-id="07d91-128">NOTES</span></span>

## <span data-ttu-id="07d91-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07d91-129">RELATED LINKS</span></span>

[<span data-ttu-id="07d91-130">추가-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="07d91-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="07d91-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="07d91-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="07d91-132">새로운 AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="07d91-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="07d91-133">제거-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="07d91-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


