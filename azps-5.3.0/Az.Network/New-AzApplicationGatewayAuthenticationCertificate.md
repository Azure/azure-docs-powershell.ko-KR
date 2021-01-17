---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c43fe72f8f3669b7e6e123a7f1d606771b161084
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379548"
---
# <span data-ttu-id="d541a-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d541a-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d541a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d541a-102">SYNOPSIS</span></span>
<span data-ttu-id="d541a-103">애플리케이션 게이트웨이에 대한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d541a-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="d541a-104">구문</span><span class="sxs-lookup"><span data-stu-id="d541a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d541a-105">설명</span><span class="sxs-lookup"><span data-stu-id="d541a-105">DESCRIPTION</span></span>
<span data-ttu-id="d541a-106">**New-AzApplicationGatewayAuthenticationCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d541a-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="d541a-107">예제</span><span class="sxs-lookup"><span data-stu-id="d541a-107">EXAMPLES</span></span>

### <span data-ttu-id="d541a-108">예제 1: 인증 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="d541a-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="d541a-109">첫 번째 명령은 cert01이라는 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d541a-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="d541a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d541a-110">PARAMETERS</span></span>

### <span data-ttu-id="d541a-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d541a-111">-CertificateFile</span></span>
<span data-ttu-id="d541a-112">인증 인증서의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d541a-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="d541a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d541a-113">-DefaultProfile</span></span>
<span data-ttu-id="d541a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d541a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d541a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d541a-115">-Name</span></span>
<span data-ttu-id="d541a-116">인증 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d541a-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="d541a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d541a-117">-Confirm</span></span>
<span data-ttu-id="d541a-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d541a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d541a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d541a-119">-WhatIf</span></span>
<span data-ttu-id="d541a-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d541a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d541a-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d541a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d541a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d541a-122">CommonParameters</span></span>
<span data-ttu-id="d541a-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d541a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d541a-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d541a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d541a-125">입력</span><span class="sxs-lookup"><span data-stu-id="d541a-125">INPUTS</span></span>

### <span data-ttu-id="d541a-126">없음</span><span class="sxs-lookup"><span data-stu-id="d541a-126">None</span></span>

## <span data-ttu-id="d541a-127">출력</span><span class="sxs-lookup"><span data-stu-id="d541a-127">OUTPUTS</span></span>

### <span data-ttu-id="d541a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d541a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d541a-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d541a-129">NOTES</span></span>
* <span data-ttu-id="d541a-130">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="d541a-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d541a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d541a-131">RELATED LINKS</span></span>

[<span data-ttu-id="d541a-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d541a-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d541a-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d541a-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d541a-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d541a-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d541a-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d541a-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


