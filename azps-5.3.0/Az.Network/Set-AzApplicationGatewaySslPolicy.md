---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 06b8f7bdaea4ebf11ff901fbe53be94f74c9bba7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495162"
---
# <span data-ttu-id="154e2-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="154e2-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="154e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="154e2-102">SYNOPSIS</span></span>
<span data-ttu-id="154e2-103">애플리케이션 게이트웨이의 SSL 정책을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="154e2-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="154e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="154e2-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-DisabledSslProtocols <String[]>]
 [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="154e2-105">설명</span><span class="sxs-lookup"><span data-stu-id="154e2-105">DESCRIPTION</span></span>
<span data-ttu-id="154e2-106">**Set-AzApplicationGatewaySslPolicy** cmdlet은 애플리케이션 게이트웨이의 SSL 정책을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="154e2-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="154e2-107">예제</span><span class="sxs-lookup"><span data-stu-id="154e2-107">EXAMPLES</span></span>

### <span data-ttu-id="154e2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="154e2-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="154e2-109">첫 번째 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="154e2-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="154e2-110">이 두 번째 명령은 ssl 정책을 정책 유형 미리 정의 및 정책 이름 AppGwSslPolicy20170401로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="154e2-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="154e2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="154e2-111">PARAMETERS</span></span>

### <span data-ttu-id="154e2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="154e2-112">-ApplicationGateway</span></span>
<span data-ttu-id="154e2-113">이 cmdlet이 수정하는 SSL 정책의 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="154e2-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="154e2-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="154e2-114">-CipherSuite</span></span>
<span data-ttu-id="154e2-115">애플리케이션 게이트웨이에 지정된 순서로 사용할 Ssl 암호 제품군</span><span class="sxs-lookup"><span data-stu-id="154e2-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="154e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="154e2-116">-DefaultProfile</span></span>
<span data-ttu-id="154e2-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="154e2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="154e2-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="154e2-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="154e2-119">사용할 수 있는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="154e2-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="154e2-120">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="154e2-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="154e2-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="154e2-121">TLSv1_0</span></span> 
- <span data-ttu-id="154e2-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="154e2-122">TLSv1_1</span></span> 
- <span data-ttu-id="154e2-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="154e2-123">TLSv1_2</span></span>

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

### <span data-ttu-id="154e2-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="154e2-124">-MinProtocolVersion</span></span>
<span data-ttu-id="154e2-125">애플리케이션 게이트웨이에서 지원되는 Ssl 프로토콜의 최소 버전</span><span class="sxs-lookup"><span data-stu-id="154e2-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="154e2-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="154e2-126">-PolicyName</span></span>
<span data-ttu-id="154e2-127">Ssl 미리 정의된 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="154e2-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="154e2-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="154e2-128">-PolicyType</span></span>
<span data-ttu-id="154e2-129">Ssl 정책의 유형</span><span class="sxs-lookup"><span data-stu-id="154e2-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="154e2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="154e2-130">-Confirm</span></span>
<span data-ttu-id="154e2-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="154e2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="154e2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="154e2-132">-WhatIf</span></span>
<span data-ttu-id="154e2-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="154e2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="154e2-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="154e2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="154e2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154e2-135">CommonParameters</span></span>
<span data-ttu-id="154e2-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="154e2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154e2-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="154e2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154e2-138">입력</span><span class="sxs-lookup"><span data-stu-id="154e2-138">INPUTS</span></span>

### <span data-ttu-id="154e2-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="154e2-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="154e2-140">출력</span><span class="sxs-lookup"><span data-stu-id="154e2-140">OUTPUTS</span></span>

### <span data-ttu-id="154e2-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="154e2-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="154e2-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="154e2-142">NOTES</span></span>
* <span data-ttu-id="154e2-143">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="154e2-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="154e2-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="154e2-144">RELATED LINKS</span></span>

[<span data-ttu-id="154e2-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="154e2-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="154e2-146">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="154e2-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)


