---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3c70fcd0e04b566ff1cd3297525d3ed2c9ed95ba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882813"
---
# <span data-ttu-id="be84e-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="be84e-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="be84e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be84e-102">SYNOPSIS</span></span>
<span data-ttu-id="be84e-103">Application gateway에 대 한 인증 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="be84e-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be84e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be84e-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be84e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be84e-105">DESCRIPTION</span></span>
<span data-ttu-id="be84e-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 대 한 인증 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="be84e-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="be84e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="be84e-107">EXAMPLES</span></span>

### <span data-ttu-id="be84e-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="be84e-108">1:</span></span>
```

```

## <span data-ttu-id="be84e-109">변수</span><span class="sxs-lookup"><span data-stu-id="be84e-109">PARAMETERS</span></span>

### <span data-ttu-id="be84e-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be84e-110">-ApplicationGateway</span></span>
<span data-ttu-id="be84e-111">이 cmdlet이 인증 인증서를 업데이트 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be84e-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="be84e-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="be84e-112">-CertificateFile</span></span>
<span data-ttu-id="be84e-113">이 cmdlet이 인증서를 업데이트 하는 인증 인증서 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be84e-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="be84e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be84e-114">-DefaultProfile</span></span>
<span data-ttu-id="be84e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be84e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be84e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="be84e-116">-Name</span></span>
<span data-ttu-id="be84e-117">이 cmdlet이 업데이트 하는 인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be84e-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="be84e-118">-확인</span><span class="sxs-lookup"><span data-stu-id="be84e-118">-Confirm</span></span>
<span data-ttu-id="be84e-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be84e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be84e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be84e-120">-WhatIf</span></span>
<span data-ttu-id="be84e-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be84e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be84e-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be84e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be84e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be84e-123">CommonParameters</span></span>
<span data-ttu-id="be84e-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be84e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be84e-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be84e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be84e-126">입력</span><span class="sxs-lookup"><span data-stu-id="be84e-126">INPUTS</span></span>

### <span data-ttu-id="be84e-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be84e-127">System.String</span></span>

## <span data-ttu-id="be84e-128">출력</span><span class="sxs-lookup"><span data-stu-id="be84e-128">OUTPUTS</span></span>

### <span data-ttu-id="be84e-129">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be84e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="be84e-130">상속자</span><span class="sxs-lookup"><span data-stu-id="be84e-130">NOTES</span></span>
* <span data-ttu-id="be84e-131">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="be84e-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="be84e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be84e-132">RELATED LINKS</span></span>

[<span data-ttu-id="be84e-133">추가-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="be84e-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="be84e-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="be84e-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="be84e-135">새로운 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="be84e-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="be84e-136">제거-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="be84e-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


