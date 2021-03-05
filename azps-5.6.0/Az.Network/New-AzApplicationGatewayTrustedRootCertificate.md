---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: bacdca3f26e18f3dc41ac19990e48f9e6bb63c1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970491"
---
# <span data-ttu-id="fbbb8-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbbb8-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="fbbb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbbb8-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbb8-103">애플리케이션 게이트웨이에 대한 신뢰할 수 있는 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fbbb8-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="fbbb8-104">구문</span><span class="sxs-lookup"><span data-stu-id="fbbb8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbbb8-105">설명</span><span class="sxs-lookup"><span data-stu-id="fbbb8-105">DESCRIPTION</span></span>
<span data-ttu-id="fbbb8-106">**New-AzApplicationGatewayTrustedRootCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 신뢰할 수 있는 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fbbb8-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="fbbb8-107">예제</span><span class="sxs-lookup"><span data-stu-id="fbbb8-107">EXAMPLES</span></span>

### <span data-ttu-id="fbbb8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fbbb8-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="fbbb8-109">이 명령은 목록 "trc1"이라는 신뢰할 수 있는 루트 인증서를 만들고 결과를 $trc.</span><span class="sxs-lookup"><span data-stu-id="fbbb8-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="fbbb8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fbbb8-110">PARAMETERS</span></span>

### <span data-ttu-id="fbbb8-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fbbb8-111">-CertificateFile</span></span>
<span data-ttu-id="fbbb8-112">인증서 CER 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="fbbb8-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="fbbb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbb8-113">-DefaultProfile</span></span>
<span data-ttu-id="fbbb8-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fbbb8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbbb8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fbbb8-115">-Name</span></span>
<span data-ttu-id="fbbb8-116">TrustedRoot 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="fbbb8-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="fbbb8-117">-확인</span><span class="sxs-lookup"><span data-stu-id="fbbb8-117">-Confirm</span></span>
<span data-ttu-id="fbbb8-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbbb8-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbbb8-119">-WhatIf</span></span>
<span data-ttu-id="fbbb8-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fbbb8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbbb8-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbbb8-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbb8-122">CommonParameters</span></span>
<span data-ttu-id="fbbb8-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fbbb8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbb8-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fbbb8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbb8-125">입력</span><span class="sxs-lookup"><span data-stu-id="fbbb8-125">INPUTS</span></span>

### <span data-ttu-id="fbbb8-126">없음</span><span class="sxs-lookup"><span data-stu-id="fbbb8-126">None</span></span>

## <span data-ttu-id="fbbb8-127">출력</span><span class="sxs-lookup"><span data-stu-id="fbbb8-127">OUTPUTS</span></span>

### <span data-ttu-id="fbbb8-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbbb8-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="fbbb8-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fbbb8-129">NOTES</span></span>

## <span data-ttu-id="fbbb8-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbbb8-130">RELATED LINKS</span></span>

[<span data-ttu-id="fbbb8-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbbb8-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="fbbb8-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbbb8-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="fbbb8-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbbb8-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="fbbb8-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbbb8-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
