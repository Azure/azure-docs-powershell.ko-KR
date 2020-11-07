---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 4affc8cdfe860dc82fe5cb71c19d4ce73301ed19
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700376"
---
# <span data-ttu-id="aa5e1-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="aa5e1-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="aa5e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="aa5e1-103">응용 프로그램 게이트웨이에 대 한 SSL 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa5e1-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="aa5e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa5e1-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa5e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aa5e1-105">DESCRIPTION</span></span>
<span data-ttu-id="aa5e1-106">**AzApplicationGatewaySslPolicy** cmdlet은 application gateway에 대 한 SSL 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa5e1-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="aa5e1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aa5e1-107">EXAMPLES</span></span>

### <span data-ttu-id="aa5e1-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="aa5e1-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="aa5e1-109">이 명령은 사용자 지정 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa5e1-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="aa5e1-110">변수</span><span class="sxs-lookup"><span data-stu-id="aa5e1-110">PARAMETERS</span></span>

### <span data-ttu-id="aa5e1-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="aa5e1-111">-CipherSuite</span></span>
<span data-ttu-id="aa5e1-112">지정 된 순서로 응용 프로그램 게이트웨이에 사용할 Ssl 암호 그룹</span><span class="sxs-lookup"><span data-stu-id="aa5e1-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="aa5e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa5e1-113">-DefaultProfile</span></span>
<span data-ttu-id="aa5e1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5e1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa5e1-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="aa5e1-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="aa5e1-116">사용할 수 없는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5e1-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="aa5e1-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="aa5e1-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aa5e1-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="aa5e1-118">TLSv1_0</span></span> 
- <span data-ttu-id="aa5e1-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="aa5e1-119">TLSv1_1</span></span> 
- <span data-ttu-id="aa5e1-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="aa5e1-120">TLSv1_2</span></span>

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

### <span data-ttu-id="aa5e1-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="aa5e1-121">-MinProtocolVersion</span></span>
<span data-ttu-id="aa5e1-122">Application gateway에서 지원 되는 Ssl 프로토콜의 최소 버전</span><span class="sxs-lookup"><span data-stu-id="aa5e1-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="aa5e1-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="aa5e1-123">-PolicyName</span></span>
<span data-ttu-id="aa5e1-124">Ssl 미리 정의 된 정책 이름</span><span class="sxs-lookup"><span data-stu-id="aa5e1-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="aa5e1-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="aa5e1-125">-PolicyType</span></span>
<span data-ttu-id="aa5e1-126">Ssl 정책 유형</span><span class="sxs-lookup"><span data-stu-id="aa5e1-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="aa5e1-127">-확인</span><span class="sxs-lookup"><span data-stu-id="aa5e1-127">-Confirm</span></span>
<span data-ttu-id="aa5e1-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5e1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa5e1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa5e1-129">-WhatIf</span></span>
<span data-ttu-id="aa5e1-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa5e1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa5e1-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa5e1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa5e1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa5e1-132">CommonParameters</span></span>
<span data-ttu-id="aa5e1-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5e1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa5e1-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa5e1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa5e1-135">입력</span><span class="sxs-lookup"><span data-stu-id="aa5e1-135">INPUTS</span></span>

### <span data-ttu-id="aa5e1-136">않아야</span><span class="sxs-lookup"><span data-stu-id="aa5e1-136">None</span></span>

## <span data-ttu-id="aa5e1-137">출력</span><span class="sxs-lookup"><span data-stu-id="aa5e1-137">OUTPUTS</span></span>

### <span data-ttu-id="aa5e1-138">PSApplicationGatewaySslPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="aa5e1-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="aa5e1-139">상속자</span><span class="sxs-lookup"><span data-stu-id="aa5e1-139">NOTES</span></span>
* <span data-ttu-id="aa5e1-140">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="aa5e1-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="aa5e1-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa5e1-141">RELATED LINKS</span></span>

[<span data-ttu-id="aa5e1-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="aa5e1-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="aa5e1-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="aa5e1-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

