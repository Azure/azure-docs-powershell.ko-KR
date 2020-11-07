---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 62c73fe60e147ca34083851db50c3830198dd60e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875621"
---
# <span data-ttu-id="b99c3-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b99c3-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b99c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b99c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b99c3-103">응용 프로그램 게이트웨이에 대 한 SSL 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="b99c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b99c3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b99c3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b99c3-105">DESCRIPTION</span></span>
<span data-ttu-id="b99c3-106">**Get-AzApplicationGatewaySslCertificate** cmdlet은 응용 프로그램 게이트웨이에 대 한 SSL 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="b99c3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b99c3-107">EXAMPLES</span></span>

### <span data-ttu-id="b99c3-108">예제 1: 특정 SSL 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="b99c3-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="b99c3-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b99c3-110">두 번째 명령은 $AppGW 이라는 변수에 저장 된 응용 프로그램 게이트웨이에서 Cert01 이라는 이름의 SSL 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="b99c3-111">명령이 $Cert 이라는 변수에 인증서를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="b99c3-112">예제 2: SSL 인증서 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="b99c3-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="b99c3-113">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b99c3-114">이 두 번째 명령은 $AppGW 이라는 변수에 저장 된 응용 프로그램 게이트웨이에서 SSL 인증서 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="b99c3-115">그런 다음 명령을 $Certs 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="b99c3-116">변수</span><span class="sxs-lookup"><span data-stu-id="b99c3-116">PARAMETERS</span></span>

### <span data-ttu-id="b99c3-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b99c3-117">-ApplicationGateway</span></span>
<span data-ttu-id="b99c3-118">SSL 인증서를 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="b99c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b99c3-119">-DefaultProfile</span></span>
<span data-ttu-id="b99c3-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b99c3-121">-이름</span><span class="sxs-lookup"><span data-stu-id="b99c3-121">-Name</span></span>
<span data-ttu-id="b99c3-122">이 cmdlet이 가져오는 SSL 인증서 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99c3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b99c3-123">CommonParameters</span></span>
<span data-ttu-id="b99c3-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b99c3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b99c3-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b99c3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b99c3-126">입력</span><span class="sxs-lookup"><span data-stu-id="b99c3-126">INPUTS</span></span>

### <span data-ttu-id="b99c3-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b99c3-127">System.String</span></span>

## <span data-ttu-id="b99c3-128">출력</span><span class="sxs-lookup"><span data-stu-id="b99c3-128">OUTPUTS</span></span>

### <span data-ttu-id="b99c3-129">PSApplicationGatewaySslCertificate에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b99c3-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b99c3-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b99c3-130">NOTES</span></span>

## <span data-ttu-id="b99c3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b99c3-131">RELATED LINKS</span></span>

[<span data-ttu-id="b99c3-132">추가-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b99c3-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b99c3-133">새로운 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b99c3-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b99c3-134">제거-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b99c3-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b99c3-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b99c3-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


