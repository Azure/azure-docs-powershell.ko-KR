---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 317fd5bf8306416ad4cbef3d1fb64d56d556ed1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530480"
---
# <span data-ttu-id="9d1e0-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9d1e0-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="9d1e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="9d1e0-103">응용 프로그램 게이트웨이에 인증 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1e0-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d1e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9d1e0-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d1e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9d1e0-105">DESCRIPTION</span></span>
<span data-ttu-id="9d1e0-106">**Add-AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 인증 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1e0-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="9d1e0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9d1e0-107">EXAMPLES</span></span>

## <span data-ttu-id="9d1e0-108">변수</span><span class="sxs-lookup"><span data-stu-id="9d1e0-108">PARAMETERS</span></span>

### <span data-ttu-id="9d1e0-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d1e0-109">-ApplicationGateway</span></span>
<span data-ttu-id="9d1e0-110">이 cmdlet이 인증 인증서를 추가 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1e0-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="9d1e0-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9d1e0-111">-CertificateFile</span></span>
<span data-ttu-id="9d1e0-112">이 cmdlet이 추가 하는 인증 인증서의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1e0-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9d1e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d1e0-113">-DefaultProfile</span></span>
<span data-ttu-id="9d1e0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9d1e0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d1e0-115">-이름</span><span class="sxs-lookup"><span data-stu-id="9d1e0-115">-Name</span></span>
<span data-ttu-id="9d1e0-116">이 cmdlet이 응용 프로그램 게이트웨이에 추가 하는 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1e0-116">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="9d1e0-117">-확인</span><span class="sxs-lookup"><span data-stu-id="9d1e0-117">-Confirm</span></span>
<span data-ttu-id="9d1e0-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1e0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d1e0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d1e0-119">-WhatIf</span></span>
<span data-ttu-id="9d1e0-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9d1e0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d1e0-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d1e0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d1e0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d1e0-122">CommonParameters</span></span>
<span data-ttu-id="9d1e0-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1e0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d1e0-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d1e0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d1e0-125">입력</span><span class="sxs-lookup"><span data-stu-id="9d1e0-125">INPUTS</span></span>

### <span data-ttu-id="9d1e0-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9d1e0-126">System.String</span></span>

## <span data-ttu-id="9d1e0-127">출력</span><span class="sxs-lookup"><span data-stu-id="9d1e0-127">OUTPUTS</span></span>

### <span data-ttu-id="9d1e0-128">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d1e0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d1e0-129">상속자</span><span class="sxs-lookup"><span data-stu-id="9d1e0-129">NOTES</span></span>
* <span data-ttu-id="9d1e0-130">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="9d1e0-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9d1e0-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d1e0-131">RELATED LINKS</span></span>

[<span data-ttu-id="9d1e0-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9d1e0-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9d1e0-133">새로운 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9d1e0-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9d1e0-134">제거-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9d1e0-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9d1e0-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9d1e0-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


