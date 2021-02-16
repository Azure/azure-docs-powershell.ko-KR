---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202861"
---
# <span data-ttu-id="e3619-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e3619-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="e3619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3619-102">SYNOPSIS</span></span>
<span data-ttu-id="e3619-103">애플리케이션 게이트웨이에 대한 신뢰할 수 있는 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3619-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="e3619-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3619-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3619-105">설명</span><span class="sxs-lookup"><span data-stu-id="e3619-105">DESCRIPTION</span></span>
<span data-ttu-id="e3619-106">**New-AzApplicationGatewayTrustedRootCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 신뢰할 수 있는 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3619-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e3619-107">예제</span><span class="sxs-lookup"><span data-stu-id="e3619-107">EXAMPLES</span></span>

### <span data-ttu-id="e3619-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3619-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="e3619-109">이 명령은 목록 "trc1"이라는 신뢰할 수 있는 루트 인증서를 만들고 결과를 $trc.</span><span class="sxs-lookup"><span data-stu-id="e3619-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="e3619-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3619-110">PARAMETERS</span></span>

### <span data-ttu-id="e3619-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e3619-111">-CertificateFile</span></span>
<span data-ttu-id="e3619-112">인증서 CER 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="e3619-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="e3619-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3619-113">-DefaultProfile</span></span>
<span data-ttu-id="e3619-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3619-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3619-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e3619-115">-Name</span></span>
<span data-ttu-id="e3619-116">TrustedRoot 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="e3619-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="e3619-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3619-117">-Confirm</span></span>
<span data-ttu-id="e3619-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3619-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3619-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3619-119">-WhatIf</span></span>
<span data-ttu-id="e3619-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e3619-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3619-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3619-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3619-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3619-122">CommonParameters</span></span>
<span data-ttu-id="e3619-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3619-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3619-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e3619-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3619-125">입력</span><span class="sxs-lookup"><span data-stu-id="e3619-125">INPUTS</span></span>

### <span data-ttu-id="e3619-126">없음</span><span class="sxs-lookup"><span data-stu-id="e3619-126">None</span></span>

## <span data-ttu-id="e3619-127">출력</span><span class="sxs-lookup"><span data-stu-id="e3619-127">OUTPUTS</span></span>

### <span data-ttu-id="e3619-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e3619-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="e3619-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3619-129">NOTES</span></span>

## <span data-ttu-id="e3619-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3619-130">RELATED LINKS</span></span>

[<span data-ttu-id="e3619-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e3619-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e3619-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e3619-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e3619-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e3619-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e3619-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e3619-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
