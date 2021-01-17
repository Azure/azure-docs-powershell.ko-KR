---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9b5e618fc4b4be02614d872bfa5bcdabd2b0fec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343550"
---
# <span data-ttu-id="27526-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="27526-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="27526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27526-102">SYNOPSIS</span></span>
<span data-ttu-id="27526-103">애플리케이션 게이트웨이의 WAF 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="27526-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="27526-104">구문</span><span class="sxs-lookup"><span data-stu-id="27526-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27526-105">설명</span><span class="sxs-lookup"><span data-stu-id="27526-105">DESCRIPTION</span></span>
<span data-ttu-id="27526-106">**Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 애플리케이션 게이트웨이의 WAF(웹 애플리케이션 방화벽) 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="27526-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="27526-107">예제</span><span class="sxs-lookup"><span data-stu-id="27526-107">EXAMPLES</span></span>

### <span data-ttu-id="27526-108">예제 1: 애플리케이션 게이트웨이 웹 애플리케이션 방화벽 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="27526-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="27526-109">첫 번째 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이를 인용한 다음, 애플리케이션 $AppGw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="27526-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="27526-110">두 번째 명령은 애플리케이션 게이트웨이에 저장된 애플리케이션 게이트웨이에 대한 방화벽 구성을 $AppGw 방화벽 모드를 "검색"으로, RuleSetType을 "OWASP"로, RuleSetVersion을 "3.0"으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="27526-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="27526-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27526-111">PARAMETERS</span></span>

### <span data-ttu-id="27526-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27526-112">-ApplicationGateway</span></span>
<span data-ttu-id="27526-113">애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27526-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="27526-114">애플리케이션 게이트웨이 개체를 Get-AzApplicationGateway cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27526-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="27526-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27526-115">-DefaultProfile</span></span>
<span data-ttu-id="27526-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27526-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27526-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="27526-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="27526-118">비활성화된 규칙 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="27526-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="27526-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="27526-119">-Enabled</span></span>
<span data-ttu-id="27526-120">웹 애플리케이션 방화벽을 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="27526-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="27526-121">-제외</span><span class="sxs-lookup"><span data-stu-id="27526-121">-Exclusion</span></span>
<span data-ttu-id="27526-122">제외 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="27526-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="27526-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="27526-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="27526-124">최대 파일 업로드 제한(MB)</span><span class="sxs-lookup"><span data-stu-id="27526-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="27526-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="27526-125">-FirewallMode</span></span>
<span data-ttu-id="27526-126">웹 애플리케이션 방화벽 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27526-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="27526-127">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="27526-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27526-128">검색</span><span class="sxs-lookup"><span data-stu-id="27526-128">Detection</span></span>
- <span data-ttu-id="27526-129">방지</span><span class="sxs-lookup"><span data-stu-id="27526-129">Prevention</span></span>

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

### <span data-ttu-id="27526-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="27526-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="27526-131">최대 요청 본문 크기(KB).</span><span class="sxs-lookup"><span data-stu-id="27526-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="27526-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="27526-132">-RequestBodyCheck</span></span>
<span data-ttu-id="27526-133">요청 본문의 선택 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="27526-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="27526-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="27526-134">-RuleSetType</span></span>
<span data-ttu-id="27526-135">웹 애플리케이션 방화벽 규칙 집합의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="27526-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="27526-136">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="27526-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="27526-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="27526-137">OWASP</span></span>

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

### <span data-ttu-id="27526-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="27526-138">-RuleSetVersion</span></span>
<span data-ttu-id="27526-139">규칙 집합 형식의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="27526-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="27526-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27526-140">-Confirm</span></span>
<span data-ttu-id="27526-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="27526-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27526-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27526-142">-WhatIf</span></span>
<span data-ttu-id="27526-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="27526-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27526-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27526-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27526-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27526-145">CommonParameters</span></span>
<span data-ttu-id="27526-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27526-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27526-147">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="27526-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27526-148">입력</span><span class="sxs-lookup"><span data-stu-id="27526-148">INPUTS</span></span>

### <span data-ttu-id="27526-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27526-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="27526-150">출력</span><span class="sxs-lookup"><span data-stu-id="27526-150">OUTPUTS</span></span>

### <span data-ttu-id="27526-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27526-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="27526-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27526-152">NOTES</span></span>

## <span data-ttu-id="27526-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27526-153">RELATED LINKS</span></span>

[<span data-ttu-id="27526-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27526-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="27526-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="27526-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="27526-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="27526-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


