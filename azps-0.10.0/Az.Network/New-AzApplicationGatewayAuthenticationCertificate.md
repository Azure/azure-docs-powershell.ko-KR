---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8f3685fddf4796cd0ad500c261f157e8ac5b95f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875486"
---
# <span data-ttu-id="bd2d1-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd2d1-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bd2d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd2d1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd2d1-103">응용 프로그램 게이트웨이에 대 한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="bd2d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bd2d1-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd2d1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bd2d1-105">DESCRIPTION</span></span>
<span data-ttu-id="bd2d1-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 대 한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="bd2d1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bd2d1-107">EXAMPLES</span></span>

### <span data-ttu-id="bd2d1-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="bd2d1-108">1:</span></span>
```

```

## <span data-ttu-id="bd2d1-109">변수</span><span class="sxs-lookup"><span data-stu-id="bd2d1-109">PARAMETERS</span></span>

### <span data-ttu-id="bd2d1-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="bd2d1-110">-CertificateFile</span></span>
<span data-ttu-id="bd2d1-111">인증 인증서의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="bd2d1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd2d1-112">-DefaultProfile</span></span>
<span data-ttu-id="bd2d1-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd2d1-114">-이름</span><span class="sxs-lookup"><span data-stu-id="bd2d1-114">-Name</span></span>
<span data-ttu-id="bd2d1-115">인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="bd2d1-116">-확인</span><span class="sxs-lookup"><span data-stu-id="bd2d1-116">-Confirm</span></span>
<span data-ttu-id="bd2d1-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd2d1-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd2d1-118">-WhatIf</span></span>
<span data-ttu-id="bd2d1-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd2d1-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd2d1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd2d1-121">CommonParameters</span></span>
<span data-ttu-id="bd2d1-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd2d1-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd2d1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd2d1-124">입력</span><span class="sxs-lookup"><span data-stu-id="bd2d1-124">INPUTS</span></span>

### <span data-ttu-id="bd2d1-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bd2d1-125">System.String</span></span>

## <span data-ttu-id="bd2d1-126">출력</span><span class="sxs-lookup"><span data-stu-id="bd2d1-126">OUTPUTS</span></span>

### <span data-ttu-id="bd2d1-127">Microsoft. \*. m i m. 모델</span><span class="sxs-lookup"><span data-stu-id="bd2d1-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bd2d1-128">상속자</span><span class="sxs-lookup"><span data-stu-id="bd2d1-128">NOTES</span></span>
* <span data-ttu-id="bd2d1-129">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="bd2d1-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bd2d1-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd2d1-130">RELATED LINKS</span></span>

[<span data-ttu-id="bd2d1-131">추가-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd2d1-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bd2d1-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd2d1-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bd2d1-133">제거-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd2d1-133">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bd2d1-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd2d1-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


