---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8b19edba06f41d4e1e7cf3c95dd1a52fa00f09e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534291"
---
# <span data-ttu-id="f0f6c-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0f6c-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f0f6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="f0f6c-103">응용 프로그램 게이트웨이에 인증 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f6c-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0f6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0f6c-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0f6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f0f6c-105">DESCRIPTION</span></span>
<span data-ttu-id="f0f6c-106">**Add-AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 인증 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f6c-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="f0f6c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f0f6c-107">EXAMPLES</span></span>

## <span data-ttu-id="f0f6c-108">변수</span><span class="sxs-lookup"><span data-stu-id="f0f6c-108">PARAMETERS</span></span>

### <span data-ttu-id="f0f6c-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0f6c-109">-ApplicationGateway</span></span>
<span data-ttu-id="f0f6c-110">이 cmdlet이 인증 인증서를 추가 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f6c-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="f0f6c-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f0f6c-111">-CertificateFile</span></span>
<span data-ttu-id="f0f6c-112">이 cmdlet이 추가 하는 인증 인증서의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f6c-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f0f6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0f6c-113">-DefaultProfile</span></span>
<span data-ttu-id="f0f6c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0f6c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0f6c-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f0f6c-115">-Name</span></span>
<span data-ttu-id="f0f6c-116">이 cmdlet이 응용 프로그램 게이트웨이에 추가 하는 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f6c-116">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="f0f6c-117">-확인</span><span class="sxs-lookup"><span data-stu-id="f0f6c-117">-Confirm</span></span>
<span data-ttu-id="f0f6c-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f6c-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0f6c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0f6c-119">-WhatIf</span></span>
<span data-ttu-id="f0f6c-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0f6c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0f6c-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0f6c-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0f6c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0f6c-122">CommonParameters</span></span>
<span data-ttu-id="f0f6c-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f6c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0f6c-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0f6c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0f6c-125">입력</span><span class="sxs-lookup"><span data-stu-id="f0f6c-125">INPUTS</span></span>

### <span data-ttu-id="f0f6c-126">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0f6c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="f0f6c-127">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f0f6c-127">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="f0f6c-128">출력</span><span class="sxs-lookup"><span data-stu-id="f0f6c-128">OUTPUTS</span></span>

### <span data-ttu-id="f0f6c-129">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0f6c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f0f6c-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f0f6c-130">NOTES</span></span>
* <span data-ttu-id="f0f6c-131">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="f0f6c-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f0f6c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0f6c-132">RELATED LINKS</span></span>

[<span data-ttu-id="f0f6c-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0f6c-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f0f6c-134">새로운 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0f6c-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f0f6c-135">제거-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0f6c-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f0f6c-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0f6c-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


