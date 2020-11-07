---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: ab5697091cf36018601bb2417e42e74f763a5d8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870258"
---
# <span data-ttu-id="4219f-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4219f-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="4219f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4219f-102">SYNOPSIS</span></span>
<span data-ttu-id="4219f-103">응용 프로그램 게이트웨이에 대 한 SSL 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="4219f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4219f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4219f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4219f-105">DESCRIPTION</span></span>
<span data-ttu-id="4219f-106">**Get-AzApplicationGatewaySslCertificate** cmdlet은 응용 프로그램 게이트웨이에 대 한 SSL 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="4219f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4219f-107">EXAMPLES</span></span>

### <span data-ttu-id="4219f-108">예제 1: 특정 SSL 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="4219f-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="4219f-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4219f-110">두 번째 명령은 $AppGW 이라는 변수에 저장 된 응용 프로그램 게이트웨이에서 Cert01 이라는 이름의 SSL 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="4219f-111">명령이 $Cert 이라는 변수에 인증서를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="4219f-112">예제 2: SSL 인증서 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="4219f-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="4219f-113">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4219f-114">이 두 번째 명령은 $AppGW 이라는 변수에 저장 된 응용 프로그램 게이트웨이에서 SSL 인증서 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="4219f-115">그런 다음 명령을 $Certs 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="4219f-116">변수</span><span class="sxs-lookup"><span data-stu-id="4219f-116">PARAMETERS</span></span>

### <span data-ttu-id="4219f-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4219f-117">-ApplicationGateway</span></span>
<span data-ttu-id="4219f-118">SSL 인증서를 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="4219f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4219f-119">-DefaultProfile</span></span>
<span data-ttu-id="4219f-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4219f-121">-이름</span><span class="sxs-lookup"><span data-stu-id="4219f-121">-Name</span></span>
<span data-ttu-id="4219f-122">이 cmdlet이 가져오는 SSL 인증서 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4219f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4219f-123">CommonParameters</span></span>
<span data-ttu-id="4219f-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4219f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4219f-125">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4219f-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4219f-126">입력</span><span class="sxs-lookup"><span data-stu-id="4219f-126">INPUTS</span></span>

### <span data-ttu-id="4219f-127">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4219f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4219f-128">출력</span><span class="sxs-lookup"><span data-stu-id="4219f-128">OUTPUTS</span></span>

### <span data-ttu-id="4219f-129">PSApplicationGatewaySslCertificate에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4219f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="4219f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="4219f-130">NOTES</span></span>

## <span data-ttu-id="4219f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4219f-131">RELATED LINKS</span></span>

[<span data-ttu-id="4219f-132">추가-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4219f-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4219f-133">새로운 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4219f-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4219f-134">제거-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4219f-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4219f-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4219f-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


