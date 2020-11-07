---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e94ca1bbed8e37643b301e5a5cb2ca3acc78d264
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869586"
---
# <span data-ttu-id="24cd8-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="24cd8-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="24cd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="24cd8-103">Application gateway의 신뢰할 수 있는 루트 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="24cd8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24cd8-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24cd8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="24cd8-106">**AzApplicationGatewayTrustedRootCertificate** Cmdlet은 응용 프로그램 게이트웨이의 기존 신뢰할 수 있는 루트 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="24cd8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="24cd8-107">EXAMPLES</span></span>

### <span data-ttu-id="24cd8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="24cd8-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="24cd8-109">위 예제 시나리오에서는 루트 인증서가 롤백될 때 기존 신뢰할 수 있는 루트 인증서를 업데이트 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="24cd8-110">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $gw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="24cd8-111">두 번째 명령은 새 루트 인증서를 사용 하 여 기존 신뢰할 수 있는 루트 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="24cd8-112">세 번째 명령은 Azure의 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="24cd8-113">변수</span><span class="sxs-lookup"><span data-stu-id="24cd8-113">PARAMETERS</span></span>

### <span data-ttu-id="24cd8-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24cd8-114">-ApplicationGateway</span></span>
<span data-ttu-id="24cd8-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24cd8-115">The applicationGateway</span></span>

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

### <span data-ttu-id="24cd8-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="24cd8-116">-CertificateFile</span></span>
<span data-ttu-id="24cd8-117">인증서 CER 파일 경로</span><span class="sxs-lookup"><span data-stu-id="24cd8-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="24cd8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cd8-118">-DefaultProfile</span></span>
<span data-ttu-id="24cd8-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24cd8-120">-이름</span><span class="sxs-lookup"><span data-stu-id="24cd8-120">-Name</span></span>
<span data-ttu-id="24cd8-121">(이)가 게 된 루트 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="24cd8-122">-확인</span><span class="sxs-lookup"><span data-stu-id="24cd8-122">-Confirm</span></span>
<span data-ttu-id="24cd8-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24cd8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24cd8-124">-WhatIf</span></span>
<span data-ttu-id="24cd8-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24cd8-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24cd8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cd8-127">CommonParameters</span></span>
<span data-ttu-id="24cd8-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24cd8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cd8-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24cd8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cd8-130">입력</span><span class="sxs-lookup"><span data-stu-id="24cd8-130">INPUTS</span></span>

### <span data-ttu-id="24cd8-131">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24cd8-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24cd8-132">출력</span><span class="sxs-lookup"><span data-stu-id="24cd8-132">OUTPUTS</span></span>

### <span data-ttu-id="24cd8-133">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24cd8-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24cd8-134">상속자</span><span class="sxs-lookup"><span data-stu-id="24cd8-134">NOTES</span></span>

## <span data-ttu-id="24cd8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24cd8-135">RELATED LINKS</span></span>

[<span data-ttu-id="24cd8-136">추가-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="24cd8-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="24cd8-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="24cd8-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="24cd8-138">새로운 AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="24cd8-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="24cd8-139">제거-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="24cd8-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
