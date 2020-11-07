---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: aedcfa4134212ef1583a91a8b902ca8395dbbfe5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700035"
---
# <span data-ttu-id="7c63c-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7c63c-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="7c63c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c63c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c63c-103">응용 프로그램 게이트웨이의 SSL 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="7c63c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c63c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-DisabledSslProtocols <String[]>]
 [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c63c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c63c-105">DESCRIPTION</span></span>
<span data-ttu-id="7c63c-106">**Set-AzApplicationGatewaySslPolicy** cmdlet은 응용 프로그램 게이트웨이의 SSL 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="7c63c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c63c-107">EXAMPLES</span></span>

### <span data-ttu-id="7c63c-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="7c63c-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="7c63c-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7c63c-110">이 두 번째 명령은 ssl 정책을 미리 정의 된 정책 형식 및 정책 이름 AppGwSslPolicy20170401 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="7c63c-111">변수</span><span class="sxs-lookup"><span data-stu-id="7c63c-111">PARAMETERS</span></span>

### <span data-ttu-id="7c63c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c63c-112">-ApplicationGateway</span></span>
<span data-ttu-id="7c63c-113">이 cmdlet이 수정 하는 SSL 정책의 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7c63c-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="7c63c-114">-CipherSuite</span></span>
<span data-ttu-id="7c63c-115">지정 된 순서로 응용 프로그램 게이트웨이에 사용할 Ssl 암호 그룹</span><span class="sxs-lookup"><span data-stu-id="7c63c-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="7c63c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c63c-116">-DefaultProfile</span></span>
<span data-ttu-id="7c63c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c63c-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="7c63c-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="7c63c-119">사용할 수 없는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="7c63c-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c63c-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="7c63c-121">TLSv1_0</span></span> 
- <span data-ttu-id="7c63c-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="7c63c-122">TLSv1_1</span></span> 
- <span data-ttu-id="7c63c-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="7c63c-123">TLSv1_2</span></span>

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

### <span data-ttu-id="7c63c-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="7c63c-124">-MinProtocolVersion</span></span>
<span data-ttu-id="7c63c-125">Application gateway에서 지원 되는 Ssl 프로토콜의 최소 버전</span><span class="sxs-lookup"><span data-stu-id="7c63c-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="7c63c-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="7c63c-126">-PolicyName</span></span>
<span data-ttu-id="7c63c-127">Ssl 미리 정의 된 정책 이름</span><span class="sxs-lookup"><span data-stu-id="7c63c-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="7c63c-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="7c63c-128">-PolicyType</span></span>
<span data-ttu-id="7c63c-129">Ssl 정책 유형</span><span class="sxs-lookup"><span data-stu-id="7c63c-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="7c63c-130">-확인</span><span class="sxs-lookup"><span data-stu-id="7c63c-130">-Confirm</span></span>
<span data-ttu-id="7c63c-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c63c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c63c-132">-WhatIf</span></span>
<span data-ttu-id="7c63c-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c63c-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c63c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c63c-135">CommonParameters</span></span>
<span data-ttu-id="7c63c-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c63c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c63c-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c63c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c63c-138">입력</span><span class="sxs-lookup"><span data-stu-id="7c63c-138">INPUTS</span></span>

### <span data-ttu-id="7c63c-139">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c63c-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7c63c-140">출력</span><span class="sxs-lookup"><span data-stu-id="7c63c-140">OUTPUTS</span></span>

### <span data-ttu-id="7c63c-141">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c63c-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7c63c-142">상속자</span><span class="sxs-lookup"><span data-stu-id="7c63c-142">NOTES</span></span>
* <span data-ttu-id="7c63c-143">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="7c63c-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7c63c-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c63c-144">RELATED LINKS</span></span>

[<span data-ttu-id="7c63c-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7c63c-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="7c63c-146">새로운 AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7c63c-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)


