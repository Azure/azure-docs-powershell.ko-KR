---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3847c1026f8cea6f3c33db45215a7a3253e4c680
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881401"
---
# <span data-ttu-id="08bc4-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="08bc4-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="08bc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="08bc4-103">응용 프로그램 게이트웨이에 대 한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08bc4-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08bc4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08bc4-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08bc4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="08bc4-105">DESCRIPTION</span></span>
<span data-ttu-id="08bc4-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 대 한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08bc4-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="08bc4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="08bc4-107">EXAMPLES</span></span>

### <span data-ttu-id="08bc4-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="08bc4-108">1:</span></span>
```

```

## <span data-ttu-id="08bc4-109">변수</span><span class="sxs-lookup"><span data-stu-id="08bc4-109">PARAMETERS</span></span>

### <span data-ttu-id="08bc4-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="08bc4-110">-CertificateFile</span></span>
<span data-ttu-id="08bc4-111">인증 인증서의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08bc4-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="08bc4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08bc4-112">-DefaultProfile</span></span>
<span data-ttu-id="08bc4-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08bc4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08bc4-114">-이름</span><span class="sxs-lookup"><span data-stu-id="08bc4-114">-Name</span></span>
<span data-ttu-id="08bc4-115">인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08bc4-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="08bc4-116">-확인</span><span class="sxs-lookup"><span data-stu-id="08bc4-116">-Confirm</span></span>
<span data-ttu-id="08bc4-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08bc4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08bc4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08bc4-118">-WhatIf</span></span>
<span data-ttu-id="08bc4-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08bc4-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08bc4-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08bc4-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08bc4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bc4-121">CommonParameters</span></span>
<span data-ttu-id="08bc4-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08bc4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bc4-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08bc4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bc4-124">입력</span><span class="sxs-lookup"><span data-stu-id="08bc4-124">INPUTS</span></span>

### <span data-ttu-id="08bc4-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="08bc4-125">System.String</span></span>

## <span data-ttu-id="08bc4-126">출력</span><span class="sxs-lookup"><span data-stu-id="08bc4-126">OUTPUTS</span></span>

### <span data-ttu-id="08bc4-127">Microsoft. \*. m i m. 모델</span><span class="sxs-lookup"><span data-stu-id="08bc4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="08bc4-128">상속자</span><span class="sxs-lookup"><span data-stu-id="08bc4-128">NOTES</span></span>
* <span data-ttu-id="08bc4-129">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="08bc4-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="08bc4-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08bc4-130">RELATED LINKS</span></span>

[<span data-ttu-id="08bc4-131">추가-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="08bc4-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="08bc4-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="08bc4-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="08bc4-133">제거-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="08bc4-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="08bc4-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="08bc4-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


