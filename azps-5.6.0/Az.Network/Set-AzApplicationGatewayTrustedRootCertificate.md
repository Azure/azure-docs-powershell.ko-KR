---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 839f2a647c4a06ddd1bdebe9b95fac0fdbdd91dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995311"
---
# <span data-ttu-id="8e20b-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e20b-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="8e20b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e20b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e20b-103">애플리케이션 게이트웨이의 신뢰할 수 있는 루트 인증서를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8e20b-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="8e20b-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e20b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e20b-105">설명</span><span class="sxs-lookup"><span data-stu-id="8e20b-105">DESCRIPTION</span></span>
<span data-ttu-id="8e20b-106">**Set-AzApplicationGatewayTrustedRootCertificate** cmdlet은 Application Gateway의 기존 신뢰할 수 있는 루트 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e20b-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="8e20b-107">예제</span><span class="sxs-lookup"><span data-stu-id="8e20b-107">EXAMPLES</span></span>

### <span data-ttu-id="8e20b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e20b-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="8e20b-109">위의 예제 시나리오에서는 루트 인증서가 롤링될 때 기존 신뢰할 수 있는 루트 인증서를 업데이트하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e20b-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="8e20b-110">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 $gw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="8e20b-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="8e20b-111">두 번째 명령은 새 루트 인증서를 사용하여 기존 신뢰할 수 있는 루트 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e20b-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="8e20b-112">세 번째 명령은 Azure에서 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8e20b-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="8e20b-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e20b-113">PARAMETERS</span></span>

### <span data-ttu-id="8e20b-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e20b-114">-ApplicationGateway</span></span>
<span data-ttu-id="8e20b-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e20b-115">The applicationGateway</span></span>

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

### <span data-ttu-id="8e20b-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8e20b-116">-CertificateFile</span></span>
<span data-ttu-id="8e20b-117">인증서 CER 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="8e20b-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="8e20b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e20b-118">-DefaultProfile</span></span>
<span data-ttu-id="8e20b-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e20b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e20b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8e20b-120">-Name</span></span>
<span data-ttu-id="8e20b-121">TrustedRoot 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="8e20b-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="8e20b-122">-확인</span><span class="sxs-lookup"><span data-stu-id="8e20b-122">-Confirm</span></span>
<span data-ttu-id="8e20b-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e20b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e20b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e20b-124">-WhatIf</span></span>
<span data-ttu-id="8e20b-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e20b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e20b-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e20b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e20b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e20b-127">CommonParameters</span></span>
<span data-ttu-id="8e20b-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e20b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e20b-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8e20b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e20b-130">입력</span><span class="sxs-lookup"><span data-stu-id="8e20b-130">INPUTS</span></span>

### <span data-ttu-id="8e20b-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e20b-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e20b-132">출력</span><span class="sxs-lookup"><span data-stu-id="8e20b-132">OUTPUTS</span></span>

### <span data-ttu-id="8e20b-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e20b-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e20b-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e20b-134">NOTES</span></span>

## <span data-ttu-id="8e20b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e20b-135">RELATED LINKS</span></span>

[<span data-ttu-id="8e20b-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e20b-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8e20b-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e20b-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8e20b-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e20b-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8e20b-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e20b-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
