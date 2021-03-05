---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c4c2c2041c6bf21aa6bf8b13055d0dac5ffbc64a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010416"
---
# <span data-ttu-id="5252f-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5252f-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5252f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5252f-102">SYNOPSIS</span></span>
<span data-ttu-id="5252f-103">애플리케이션 게이트웨이에 대한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5252f-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="5252f-104">구문</span><span class="sxs-lookup"><span data-stu-id="5252f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5252f-105">설명</span><span class="sxs-lookup"><span data-stu-id="5252f-105">DESCRIPTION</span></span>
<span data-ttu-id="5252f-106">**New-AzApplicationGatewayAuthenticationCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5252f-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5252f-107">예제</span><span class="sxs-lookup"><span data-stu-id="5252f-107">EXAMPLES</span></span>

### <span data-ttu-id="5252f-108">예제 1: 인증 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="5252f-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="5252f-109">첫 번째 명령은 cert01이라는 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5252f-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="5252f-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5252f-110">PARAMETERS</span></span>

### <span data-ttu-id="5252f-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5252f-111">-CertificateFile</span></span>
<span data-ttu-id="5252f-112">인증 인증서의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5252f-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="5252f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5252f-113">-DefaultProfile</span></span>
<span data-ttu-id="5252f-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5252f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5252f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5252f-115">-Name</span></span>
<span data-ttu-id="5252f-116">인증 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5252f-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="5252f-117">-확인</span><span class="sxs-lookup"><span data-stu-id="5252f-117">-Confirm</span></span>
<span data-ttu-id="5252f-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5252f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5252f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5252f-119">-WhatIf</span></span>
<span data-ttu-id="5252f-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5252f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5252f-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5252f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5252f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5252f-122">CommonParameters</span></span>
<span data-ttu-id="5252f-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5252f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5252f-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5252f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5252f-125">입력</span><span class="sxs-lookup"><span data-stu-id="5252f-125">INPUTS</span></span>

### <span data-ttu-id="5252f-126">없음</span><span class="sxs-lookup"><span data-stu-id="5252f-126">None</span></span>

## <span data-ttu-id="5252f-127">출력</span><span class="sxs-lookup"><span data-stu-id="5252f-127">OUTPUTS</span></span>

### <span data-ttu-id="5252f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5252f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5252f-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5252f-129">NOTES</span></span>
* <span data-ttu-id="5252f-130">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="5252f-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5252f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5252f-131">RELATED LINKS</span></span>

[<span data-ttu-id="5252f-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5252f-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5252f-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5252f-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5252f-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5252f-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5252f-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5252f-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


