---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bf4a87ebae55329e4594d11559fda0aee9047cbc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876589"
---
# <span data-ttu-id="b15ba-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b15ba-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="b15ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b15ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b15ba-103">응용 프로그램 게이트웨이의 WAF 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="b15ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b15ba-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b15ba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b15ba-105">DESCRIPTION</span></span>
<span data-ttu-id="b15ba-106">**AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 응용 프로그램 게이트웨이의 waf (웹 응용 프로그램 방화벽) 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="b15ba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b15ba-107">EXAMPLES</span></span>

### <span data-ttu-id="b15ba-108">예제 1: 응용 프로그램 게이트웨이 웹 응용 프로그램 방화벽 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="b15ba-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="b15ba-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b15ba-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에 대 한 방화벽 구성을 사용할 수 있도록 설정 하 고 방화벽 모드를 "검색", RuleSetType, "OWASP" 및 Rulesettype을 "3.0"로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="b15ba-111">변수</span><span class="sxs-lookup"><span data-stu-id="b15ba-111">PARAMETERS</span></span>

### <span data-ttu-id="b15ba-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b15ba-112">-ApplicationGateway</span></span>
<span data-ttu-id="b15ba-113">응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="b15ba-114">Get-AzApplicationGateway cmdlet을 사용 하 여 응용 프로그램 게이트웨이 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b15ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b15ba-115">-DefaultProfile</span></span>
<span data-ttu-id="b15ba-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15ba-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="b15ba-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="b15ba-118">비활성화 된 규칙 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15ba-119">-사용</span><span class="sxs-lookup"><span data-stu-id="b15ba-119">-Enabled</span></span>
<span data-ttu-id="b15ba-120">웹 응용 프로그램 방화벽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-120">Indicates whether the web application firewall is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15ba-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="b15ba-121">-FirewallMode</span></span>
<span data-ttu-id="b15ba-122">웹 응용 프로그램 방화벽 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="b15ba-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b15ba-124">기능과</span><span class="sxs-lookup"><span data-stu-id="b15ba-124">Detection</span></span>
- <span data-ttu-id="b15ba-125">공격</span><span class="sxs-lookup"><span data-stu-id="b15ba-125">Prevention</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15ba-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="b15ba-126">-RuleSetType</span></span>
<span data-ttu-id="b15ba-127">웹 응용 프로그램 방화벽 규칙 집합의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="b15ba-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="b15ba-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="b15ba-129">OWASP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15ba-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="b15ba-130">-RuleSetVersion</span></span>
<span data-ttu-id="b15ba-131">규칙 집합 유형의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-131">The version of the rule set type.</span></span>
<span data-ttu-id="b15ba-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="b15ba-133">3.0</span><span class="sxs-lookup"><span data-stu-id="b15ba-133">3.0</span></span>
- <span data-ttu-id="b15ba-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="b15ba-134">2.2.9</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15ba-135">-확인</span><span class="sxs-lookup"><span data-stu-id="b15ba-135">-Confirm</span></span>
<span data-ttu-id="b15ba-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15ba-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b15ba-137">-WhatIf</span></span>
<span data-ttu-id="b15ba-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b15ba-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15ba-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b15ba-140">CommonParameters</span></span>
<span data-ttu-id="b15ba-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b15ba-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b15ba-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b15ba-143">입력</span><span class="sxs-lookup"><span data-stu-id="b15ba-143">INPUTS</span></span>

### <span data-ttu-id="b15ba-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b15ba-144">PSApplicationGateway</span></span>
<span data-ttu-id="b15ba-145">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15ba-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="b15ba-146">출력</span><span class="sxs-lookup"><span data-stu-id="b15ba-146">OUTPUTS</span></span>

### <span data-ttu-id="b15ba-147">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b15ba-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b15ba-148">상속자</span><span class="sxs-lookup"><span data-stu-id="b15ba-148">NOTES</span></span>

## <span data-ttu-id="b15ba-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b15ba-149">RELATED LINKS</span></span>

[<span data-ttu-id="b15ba-150">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b15ba-150">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="b15ba-151">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b15ba-151">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="b15ba-152">새로운 AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b15ba-152">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


