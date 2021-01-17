---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 0f186de1ad548be0c566c6fac2b8d1505885bfe0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379261"
---
# <span data-ttu-id="414d7-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="414d7-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="414d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="414d7-102">SYNOPSIS</span></span>
<span data-ttu-id="414d7-103">애플리케이션 게이트웨이에 대한 WAF 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="414d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="414d7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="414d7-105">설명</span><span class="sxs-lookup"><span data-stu-id="414d7-105">DESCRIPTION</span></span>
<span data-ttu-id="414d7-106">**New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 WAF(웹 애플리케이션 방화벽) 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="414d7-107">예제</span><span class="sxs-lookup"><span data-stu-id="414d7-107">EXAMPLES</span></span>

### <span data-ttu-id="414d7-108">예제 1: 애플리케이션 게이트웨이에 대한 웹 애플리케이션 방화벽 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="414d7-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="414d7-109">첫 번째 명령은 규칙 942130 및 규칙 942140이 비활성화된 "REQUEST-942-APPLICATION-ATTACK-SQLI"라는 규칙 그룹에 대해 사용하지 않도록 설정된 규칙 그룹 구성을 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="414d7-110">두 번째 명령은 "REQUEST-921-PROTOCOL-ATTACK"라는 규칙 그룹에 대해 비활성화된 다른 규칙 그룹 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="414d7-111">규칙은 특별히 전달되지 않습니다. 따라서 규칙 그룹의 모든 규칙이 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="414d7-112">그런 다음, 마지막 명령은 $disabledRuleGroup 1 및 $disabledRuleGroup 2에서 구성된 방화벽 규칙이 비활성화된 WAF 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="414d7-113">새 WAF 구성은 새 WAF 변수에 $firewallConfig 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="414d7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="414d7-114">PARAMETERS</span></span>

### <span data-ttu-id="414d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="414d7-115">-DefaultProfile</span></span>
<span data-ttu-id="414d7-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="414d7-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="414d7-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="414d7-118">비활성화된 규칙 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="414d7-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="414d7-119">-Enabled</span></span>
<span data-ttu-id="414d7-120">WAF를 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="414d7-121">-제외</span><span class="sxs-lookup"><span data-stu-id="414d7-121">-Exclusion</span></span>
<span data-ttu-id="414d7-122">제외 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="414d7-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="414d7-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="414d7-124">최대 파일 업로드 제한(MB)</span><span class="sxs-lookup"><span data-stu-id="414d7-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="414d7-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="414d7-125">-FirewallMode</span></span>
<span data-ttu-id="414d7-126">웹 애플리케이션 방화벽 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="414d7-127">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="414d7-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="414d7-128">검색</span><span class="sxs-lookup"><span data-stu-id="414d7-128">Detection</span></span>
- <span data-ttu-id="414d7-129">방지</span><span class="sxs-lookup"><span data-stu-id="414d7-129">Prevention</span></span>

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

### <span data-ttu-id="414d7-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="414d7-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="414d7-131">최대 요청 본문 크기(KB).</span><span class="sxs-lookup"><span data-stu-id="414d7-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="414d7-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="414d7-132">-RequestBodyCheck</span></span>
<span data-ttu-id="414d7-133">요청 본문의 선택 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="414d7-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="414d7-134">-RuleSetType</span></span>
<span data-ttu-id="414d7-135">웹 애플리케이션 방화벽 규칙 집합의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="414d7-136">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="414d7-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="414d7-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="414d7-137">OWASP</span></span>

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

### <span data-ttu-id="414d7-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="414d7-138">-RuleSetVersion</span></span>
<span data-ttu-id="414d7-139">규칙 집합 형식의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-139">The version of the rule set type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="414d7-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="414d7-140">-Confirm</span></span>
<span data-ttu-id="414d7-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="414d7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="414d7-142">-WhatIf</span></span>
<span data-ttu-id="414d7-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="414d7-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="414d7-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="414d7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="414d7-145">CommonParameters</span></span>
<span data-ttu-id="414d7-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="414d7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="414d7-147">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="414d7-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="414d7-148">입력</span><span class="sxs-lookup"><span data-stu-id="414d7-148">INPUTS</span></span>

### <span data-ttu-id="414d7-149">없음</span><span class="sxs-lookup"><span data-stu-id="414d7-149">None</span></span>

## <span data-ttu-id="414d7-150">출력</span><span class="sxs-lookup"><span data-stu-id="414d7-150">OUTPUTS</span></span>

### <span data-ttu-id="414d7-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="414d7-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="414d7-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="414d7-152">NOTES</span></span>

## <span data-ttu-id="414d7-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="414d7-153">RELATED LINKS</span></span>

[<span data-ttu-id="414d7-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="414d7-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="414d7-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="414d7-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


