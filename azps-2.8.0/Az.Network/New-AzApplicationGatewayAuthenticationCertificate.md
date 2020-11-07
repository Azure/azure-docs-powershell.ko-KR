---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 7e1c5c301b13f37086f4b6fc96e7254230684d10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870566"
---
# <span data-ttu-id="e5717-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e5717-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="e5717-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5717-102">SYNOPSIS</span></span>
<span data-ttu-id="e5717-103">응용 프로그램 게이트웨이에 대 한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5717-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="e5717-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5717-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5717-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e5717-105">DESCRIPTION</span></span>
<span data-ttu-id="e5717-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에 대 한 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5717-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e5717-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e5717-107">EXAMPLES</span></span>

### <span data-ttu-id="e5717-108">예제 1: 인증 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="e5717-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="e5717-109">첫 번째 명령은 cert01 이라는 인증 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5717-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="e5717-110">변수</span><span class="sxs-lookup"><span data-stu-id="e5717-110">PARAMETERS</span></span>

### <span data-ttu-id="e5717-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e5717-111">-CertificateFile</span></span>
<span data-ttu-id="e5717-112">인증 인증서의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5717-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="e5717-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5717-113">-DefaultProfile</span></span>
<span data-ttu-id="e5717-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5717-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5717-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e5717-115">-Name</span></span>
<span data-ttu-id="e5717-116">인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5717-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="e5717-117">-확인</span><span class="sxs-lookup"><span data-stu-id="e5717-117">-Confirm</span></span>
<span data-ttu-id="e5717-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5717-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5717-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5717-119">-WhatIf</span></span>
<span data-ttu-id="e5717-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5717-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5717-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5717-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5717-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5717-122">CommonParameters</span></span>
<span data-ttu-id="e5717-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5717-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5717-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5717-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5717-125">입력</span><span class="sxs-lookup"><span data-stu-id="e5717-125">INPUTS</span></span>

### <span data-ttu-id="e5717-126">않아야</span><span class="sxs-lookup"><span data-stu-id="e5717-126">None</span></span>

## <span data-ttu-id="e5717-127">출력</span><span class="sxs-lookup"><span data-stu-id="e5717-127">OUTPUTS</span></span>

### <span data-ttu-id="e5717-128">Microsoft. \*. m i m. 모델</span><span class="sxs-lookup"><span data-stu-id="e5717-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="e5717-129">상속자</span><span class="sxs-lookup"><span data-stu-id="e5717-129">NOTES</span></span>
* <span data-ttu-id="e5717-130">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="e5717-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e5717-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5717-131">RELATED LINKS</span></span>

[<span data-ttu-id="e5717-132">추가-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e5717-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e5717-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e5717-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e5717-134">제거-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e5717-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e5717-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e5717-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


