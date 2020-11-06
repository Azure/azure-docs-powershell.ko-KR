---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bdc2821c8499c5a95acd180c9bbfa28568cc5034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529513"
---
# <span data-ttu-id="f431b-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f431b-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f431b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f431b-102">SYNOPSIS</span></span>
<span data-ttu-id="f431b-103">응용 프로그램 게이트웨이에 대 한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f431b-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f431b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f431b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f431b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f431b-105">DESCRIPTION</span></span>
<span data-ttu-id="f431b-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 대 한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f431b-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="f431b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f431b-107">EXAMPLES</span></span>

## <span data-ttu-id="f431b-108">변수</span><span class="sxs-lookup"><span data-stu-id="f431b-108">PARAMETERS</span></span>

### <span data-ttu-id="f431b-109">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f431b-109">-CertificateFile</span></span>
<span data-ttu-id="f431b-110">인증 인증서의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f431b-110">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="f431b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f431b-111">-DefaultProfile</span></span>
<span data-ttu-id="f431b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f431b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f431b-113">-이름</span><span class="sxs-lookup"><span data-stu-id="f431b-113">-Name</span></span>
<span data-ttu-id="f431b-114">인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f431b-114">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="f431b-115">-확인</span><span class="sxs-lookup"><span data-stu-id="f431b-115">-Confirm</span></span>
<span data-ttu-id="f431b-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f431b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f431b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f431b-117">-WhatIf</span></span>
<span data-ttu-id="f431b-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f431b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f431b-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f431b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f431b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f431b-120">CommonParameters</span></span>
<span data-ttu-id="f431b-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f431b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f431b-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f431b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f431b-123">입력</span><span class="sxs-lookup"><span data-stu-id="f431b-123">INPUTS</span></span>

### <span data-ttu-id="f431b-124">않아야</span><span class="sxs-lookup"><span data-stu-id="f431b-124">None</span></span>

## <span data-ttu-id="f431b-125">출력</span><span class="sxs-lookup"><span data-stu-id="f431b-125">OUTPUTS</span></span>

### <span data-ttu-id="f431b-126">Microsoft. \*. m i m. 모델</span><span class="sxs-lookup"><span data-stu-id="f431b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f431b-127">상속자</span><span class="sxs-lookup"><span data-stu-id="f431b-127">NOTES</span></span>
* <span data-ttu-id="f431b-128">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="f431b-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f431b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f431b-129">RELATED LINKS</span></span>

[<span data-ttu-id="f431b-130">추가-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f431b-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f431b-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f431b-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f431b-132">제거-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f431b-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f431b-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f431b-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


