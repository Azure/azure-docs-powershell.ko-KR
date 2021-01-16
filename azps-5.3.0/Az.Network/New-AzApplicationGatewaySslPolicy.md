---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: cf2f2ef91fa217b1710eeb100f4e3e6c2ce6fb9d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491072"
---
# <span data-ttu-id="bfc3e-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bfc3e-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="bfc3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfc3e-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc3e-103">애플리케이션 게이트웨이에 대한 SSL 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3e-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="bfc3e-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfc3e-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfc3e-105">설명</span><span class="sxs-lookup"><span data-stu-id="bfc3e-105">DESCRIPTION</span></span>
<span data-ttu-id="bfc3e-106">**New-AzApplicationGatewaySslPolicy** cmdlet은 애플리케이션 게이트웨이에 대한 SSL 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3e-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="bfc3e-107">예제</span><span class="sxs-lookup"><span data-stu-id="bfc3e-107">EXAMPLES</span></span>

### <span data-ttu-id="bfc3e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bfc3e-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="bfc3e-109">이 명령은 사용자 지정 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3e-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="bfc3e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfc3e-110">PARAMETERS</span></span>

### <span data-ttu-id="bfc3e-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="bfc3e-111">-CipherSuite</span></span>
<span data-ttu-id="bfc3e-112">애플리케이션 게이트웨이에 지정된 순서로 사용할 Ssl 암호 제품군</span><span class="sxs-lookup"><span data-stu-id="bfc3e-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc3e-113">-DefaultProfile</span></span>
<span data-ttu-id="bfc3e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfc3e-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="bfc3e-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="bfc3e-116">사용할 수 있는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3e-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="bfc3e-117">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="bfc3e-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bfc3e-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="bfc3e-118">TLSv1_0</span></span> 
- <span data-ttu-id="bfc3e-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="bfc3e-119">TLSv1_1</span></span> 
- <span data-ttu-id="bfc3e-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="bfc3e-120">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc3e-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="bfc3e-121">-MinProtocolVersion</span></span>
<span data-ttu-id="bfc3e-122">애플리케이션 게이트웨이에서 지원되는 Ssl 프로토콜의 최소 버전</span><span class="sxs-lookup"><span data-stu-id="bfc3e-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc3e-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="bfc3e-123">-PolicyName</span></span>
<span data-ttu-id="bfc3e-124">Ssl 미리 정의된 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="bfc3e-124">Name of Ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc3e-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="bfc3e-125">-PolicyType</span></span>
<span data-ttu-id="bfc3e-126">Ssl 정책의 유형</span><span class="sxs-lookup"><span data-stu-id="bfc3e-126">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc3e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfc3e-127">-Confirm</span></span>
<span data-ttu-id="bfc3e-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfc3e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfc3e-129">-WhatIf</span></span>
<span data-ttu-id="bfc3e-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bfc3e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfc3e-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfc3e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc3e-132">CommonParameters</span></span>
<span data-ttu-id="bfc3e-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc3e-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bfc3e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc3e-135">입력</span><span class="sxs-lookup"><span data-stu-id="bfc3e-135">INPUTS</span></span>

### <span data-ttu-id="bfc3e-136">없음</span><span class="sxs-lookup"><span data-stu-id="bfc3e-136">None</span></span>

## <span data-ttu-id="bfc3e-137">출력</span><span class="sxs-lookup"><span data-stu-id="bfc3e-137">OUTPUTS</span></span>

### <span data-ttu-id="bfc3e-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bfc3e-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="bfc3e-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bfc3e-139">NOTES</span></span>
* <span data-ttu-id="bfc3e-140">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="bfc3e-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bfc3e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfc3e-141">RELATED LINKS</span></span>

[<span data-ttu-id="bfc3e-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bfc3e-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="bfc3e-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bfc3e-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


