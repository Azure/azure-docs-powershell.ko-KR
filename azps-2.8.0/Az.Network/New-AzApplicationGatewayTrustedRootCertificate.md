---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 473e759e43c59c48b9e47706ac55b388379b6d6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870494"
---
# <span data-ttu-id="8ad6e-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8ad6e-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="8ad6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ad6e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad6e-103">응용 프로그램 게이트웨이에 대해 신뢰할 수 있는 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ad6e-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="8ad6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ad6e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ad6e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ad6e-105">DESCRIPTION</span></span>
<span data-ttu-id="8ad6e-106">**AzApplicationGatewayTrustedRootCertificate** Cmdlet은 Azure application gateway에 대해 신뢰할 수 있는 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ad6e-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="8ad6e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8ad6e-107">EXAMPLES</span></span>

### <span data-ttu-id="8ad6e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ad6e-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="8ad6e-109">이 명령은 "trc1" 이라는 신뢰할 수 있는 루트 인증서를 만들고 결과를 $trc 이름이 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad6e-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="8ad6e-110">변수</span><span class="sxs-lookup"><span data-stu-id="8ad6e-110">PARAMETERS</span></span>

### <span data-ttu-id="8ad6e-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8ad6e-111">-CertificateFile</span></span>
<span data-ttu-id="8ad6e-112">인증서 CER 파일 경로</span><span class="sxs-lookup"><span data-stu-id="8ad6e-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="8ad6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad6e-113">-DefaultProfile</span></span>
<span data-ttu-id="8ad6e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad6e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ad6e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8ad6e-115">-Name</span></span>
<span data-ttu-id="8ad6e-116">(이)가 게 된 루트 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad6e-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="8ad6e-117">-확인</span><span class="sxs-lookup"><span data-stu-id="8ad6e-117">-Confirm</span></span>
<span data-ttu-id="8ad6e-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad6e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ad6e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ad6e-119">-WhatIf</span></span>
<span data-ttu-id="8ad6e-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ad6e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ad6e-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ad6e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ad6e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad6e-122">CommonParameters</span></span>
<span data-ttu-id="8ad6e-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad6e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad6e-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ad6e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad6e-125">입력</span><span class="sxs-lookup"><span data-stu-id="8ad6e-125">INPUTS</span></span>

### <span data-ttu-id="8ad6e-126">않아야</span><span class="sxs-lookup"><span data-stu-id="8ad6e-126">None</span></span>

## <span data-ttu-id="8ad6e-127">출력</span><span class="sxs-lookup"><span data-stu-id="8ad6e-127">OUTPUTS</span></span>

### <span data-ttu-id="8ad6e-128">Microsoft. 네트워크. Psapplication게이트웨이를 위한 Rootcertificate</span><span class="sxs-lookup"><span data-stu-id="8ad6e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="8ad6e-129">상속자</span><span class="sxs-lookup"><span data-stu-id="8ad6e-129">NOTES</span></span>

## <span data-ttu-id="8ad6e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ad6e-130">RELATED LINKS</span></span>

[<span data-ttu-id="8ad6e-131">추가-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8ad6e-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8ad6e-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8ad6e-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8ad6e-133">제거-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8ad6e-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8ad6e-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8ad6e-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
