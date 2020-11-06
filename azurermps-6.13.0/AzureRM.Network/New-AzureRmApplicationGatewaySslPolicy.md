---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 140bfd84d2758badc45a902e4ed14e027c5bca3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537584"
---
# <span data-ttu-id="3f23e-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3f23e-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="3f23e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f23e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f23e-103">응용 프로그램 게이트웨이에 대 한 SSL 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f23e-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f23e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f23e-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f23e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3f23e-105">DESCRIPTION</span></span>
<span data-ttu-id="3f23e-106">**AzureRmApplicationGatewaySslPolicy** cmdlet은 application gateway에 대 한 SSL 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f23e-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="3f23e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3f23e-107">EXAMPLES</span></span>

### <span data-ttu-id="3f23e-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="3f23e-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="3f23e-109">이 명령은 사용자 지정 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f23e-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="3f23e-110">변수</span><span class="sxs-lookup"><span data-stu-id="3f23e-110">PARAMETERS</span></span>

### <span data-ttu-id="3f23e-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="3f23e-111">-CipherSuite</span></span>
<span data-ttu-id="3f23e-112">지정 된 순서로 응용 프로그램 게이트웨이에 사용할 Ssl 암호 그룹</span><span class="sxs-lookup"><span data-stu-id="3f23e-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f23e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f23e-113">-DefaultProfile</span></span>
<span data-ttu-id="3f23e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f23e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f23e-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="3f23e-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="3f23e-116">사용할 수 없는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f23e-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="3f23e-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3f23e-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3f23e-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="3f23e-118">TLSv1_0</span></span> 
- <span data-ttu-id="3f23e-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="3f23e-119">TLSv1_1</span></span> 
- <span data-ttu-id="3f23e-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="3f23e-120">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f23e-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="3f23e-121">-MinProtocolVersion</span></span>
<span data-ttu-id="3f23e-122">Application gateway에서 지원 되는 Ssl 프로토콜의 최소 버전</span><span class="sxs-lookup"><span data-stu-id="3f23e-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="3f23e-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="3f23e-123">-PolicyName</span></span>
<span data-ttu-id="3f23e-124">Ssl 미리 정의 된 정책 이름</span><span class="sxs-lookup"><span data-stu-id="3f23e-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="3f23e-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="3f23e-125">-PolicyType</span></span>
<span data-ttu-id="3f23e-126">Ssl 정책 유형</span><span class="sxs-lookup"><span data-stu-id="3f23e-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="3f23e-127">-확인</span><span class="sxs-lookup"><span data-stu-id="3f23e-127">-Confirm</span></span>
<span data-ttu-id="3f23e-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f23e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f23e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f23e-129">-WhatIf</span></span>
<span data-ttu-id="3f23e-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f23e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f23e-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f23e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f23e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f23e-132">CommonParameters</span></span>
<span data-ttu-id="3f23e-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f23e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f23e-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f23e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f23e-135">입력</span><span class="sxs-lookup"><span data-stu-id="3f23e-135">INPUTS</span></span>

### <span data-ttu-id="3f23e-136">않아야</span><span class="sxs-lookup"><span data-stu-id="3f23e-136">None</span></span>

## <span data-ttu-id="3f23e-137">출력</span><span class="sxs-lookup"><span data-stu-id="3f23e-137">OUTPUTS</span></span>

### <span data-ttu-id="3f23e-138">PSApplicationGatewaySslPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="3f23e-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="3f23e-139">상속자</span><span class="sxs-lookup"><span data-stu-id="3f23e-139">NOTES</span></span>
* <span data-ttu-id="3f23e-140">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="3f23e-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3f23e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f23e-141">RELATED LINKS</span></span>

[<span data-ttu-id="3f23e-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3f23e-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="3f23e-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3f23e-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


