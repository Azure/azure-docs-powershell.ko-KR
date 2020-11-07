---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: a5f60588a0db848d0b96aa0611b8647142db2b06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700028"
---
# <span data-ttu-id="11c54-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="11c54-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="11c54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11c54-102">SYNOPSIS</span></span>
<span data-ttu-id="11c54-103">응용 프로그램 게이트웨이의 WAF 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="11c54-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11c54-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11c54-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11c54-105">DESCRIPTION</span></span>
<span data-ttu-id="11c54-106">**AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 응용 프로그램 게이트웨이의 waf (웹 응용 프로그램 방화벽) 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="11c54-107">예제의</span><span class="sxs-lookup"><span data-stu-id="11c54-107">EXAMPLES</span></span>

### <span data-ttu-id="11c54-108">예제 1: 응용 프로그램 게이트웨이 웹 응용 프로그램 방화벽 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="11c54-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="11c54-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="11c54-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에 대 한 방화벽 구성을 사용할 수 있도록 설정 하 고 방화벽 모드를 "검색", RuleSetType, "OWASP" 및 Rulesettype을 "3.0"로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="11c54-111">변수</span><span class="sxs-lookup"><span data-stu-id="11c54-111">PARAMETERS</span></span>

### <span data-ttu-id="11c54-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11c54-112">-ApplicationGateway</span></span>
<span data-ttu-id="11c54-113">응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="11c54-114">Get-AzApplicationGateway cmdlet을 사용 하 여 응용 프로그램 게이트웨이 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="11c54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c54-115">-DefaultProfile</span></span>
<span data-ttu-id="11c54-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11c54-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="11c54-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="11c54-118">비활성화 된 규칙 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-118">The disabled rule groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup[]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c54-119">-사용</span><span class="sxs-lookup"><span data-stu-id="11c54-119">-Enabled</span></span>
<span data-ttu-id="11c54-120">웹 응용 프로그램 방화벽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-120">Indicates whether the web application firewall is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c54-121">-제외</span><span class="sxs-lookup"><span data-stu-id="11c54-121">-Exclusion</span></span>
<span data-ttu-id="11c54-122">제외 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-122">The exclusion lists.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c54-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="11c54-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="11c54-124">최대 파일 업로드 제한 (MB)입니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-124">Max file upload limit in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c54-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="11c54-125">-FirewallMode</span></span>
<span data-ttu-id="11c54-126">웹 응용 프로그램 방화벽 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="11c54-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11c54-128">기능과</span><span class="sxs-lookup"><span data-stu-id="11c54-128">Detection</span></span>
- <span data-ttu-id="11c54-129">공격</span><span class="sxs-lookup"><span data-stu-id="11c54-129">Prevention</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c54-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="11c54-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="11c54-131">최대 요청 본문 크기 (KB)입니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-131">Max request body size in KB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c54-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="11c54-132">-RequestBodyCheck</span></span>
<span data-ttu-id="11c54-133">요청 본문의 확인 여부</span><span class="sxs-lookup"><span data-stu-id="11c54-133">Whether request body is checked or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c54-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="11c54-134">-RuleSetType</span></span>
<span data-ttu-id="11c54-135">웹 응용 프로그램 방화벽 규칙 집합의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="11c54-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="11c54-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="11c54-137">OWASP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c54-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="11c54-138">-RuleSetVersion</span></span>
<span data-ttu-id="11c54-139">규칙 집합 유형의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-139">The version of the rule set type.</span></span>
<span data-ttu-id="11c54-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="11c54-141">3.0</span><span class="sxs-lookup"><span data-stu-id="11c54-141">3.0</span></span>
- <span data-ttu-id="11c54-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="11c54-142">2.2.9</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c54-143">-확인</span><span class="sxs-lookup"><span data-stu-id="11c54-143">-Confirm</span></span>
<span data-ttu-id="11c54-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11c54-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11c54-145">-WhatIf</span></span>
<span data-ttu-id="11c54-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11c54-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11c54-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c54-148">CommonParameters</span></span>
<span data-ttu-id="11c54-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c54-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c54-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11c54-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c54-151">입력</span><span class="sxs-lookup"><span data-stu-id="11c54-151">INPUTS</span></span>

### <span data-ttu-id="11c54-152">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11c54-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11c54-153">출력</span><span class="sxs-lookup"><span data-stu-id="11c54-153">OUTPUTS</span></span>

### <span data-ttu-id="11c54-154">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11c54-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11c54-155">상속자</span><span class="sxs-lookup"><span data-stu-id="11c54-155">NOTES</span></span>

## <span data-ttu-id="11c54-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11c54-156">RELATED LINKS</span></span>

[<span data-ttu-id="11c54-157">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11c54-157">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="11c54-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="11c54-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="11c54-159">새로운 AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="11c54-159">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


