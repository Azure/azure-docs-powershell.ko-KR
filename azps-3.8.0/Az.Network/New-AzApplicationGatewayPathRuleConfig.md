---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: f06dbac5e7c7a67acc38c5357351905fab0ed141
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402561"
---
# <span data-ttu-id="8ecae-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ecae-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="8ecae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ecae-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecae-103">애플리케이션 게이트웨이 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="8ecae-104">구문</span><span class="sxs-lookup"><span data-stu-id="8ecae-104">SYNTAX</span></span>

### <span data-ttu-id="8ecae-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8ecae-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ecae-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8ecae-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ecae-107">설명</span><span class="sxs-lookup"><span data-stu-id="8ecae-107">DESCRIPTION</span></span>
<span data-ttu-id="8ecae-108">**New-AzApplicationGatewayPathRuleConfig** cmdlet은 애플리케이션 게이트웨이 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="8ecae-109">이 cmdlet에서 만든 규칙은 URL 경로 맵 구성 설정의 컬렉션에 추가한 다음 게이트웨이에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="8ecae-110">경로 맵 구성 설정은 애플리케이션 게이트웨이 부하 분산에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="8ecae-111">예제</span><span class="sxs-lookup"><span data-stu-id="8ecae-111">EXAMPLES</span></span>

### <span data-ttu-id="8ecae-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ecae-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="8ecae-113">이러한 명령은 새 애플리케이션 게이트웨이 경로 규칙을 만든 다음 **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet을 사용하여 애플리케이션 게이트웨이에 해당 규칙을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="8ecae-114">이를 위해 첫 번째 명령은 ContosoApplicationGateway 게이트웨이에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="8ecae-115">이 개체 참조는 $Gateway.</span><span class="sxs-lookup"><span data-stu-id="8ecae-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="8ecae-116">다음 두 명령은 백end 주소 풀 및 백end HTTP 설정 개체를 만듭니다. 경로 규칙 개체를 만들기 위해 이러한 개체($AddressPool 및 $HttpSettings 변수에 저장)가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="8ecae-117">네 번째 명령은 경로 규칙 개체를 만들고 경로 규칙이라는 변수에 $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8ecae-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="8ecae-118">다섯 번째 명령은 **Add-AzApplicationGatewayUrlPathMapConfig를** 사용하여 구성 설정 및 해당 설정 내에 포함된 새 경로 규칙을 ContosoApplicationGateway에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="8ecae-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="8ecae-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="8ecae-120">이 명령은 "base"로, 경로는 "/base"로, BackendAddressPool은 $AddressPool, BackendHttpSettings는 $HttpSettings, FirewallPolicy는 $firewallPolicy.ngs로, ContosoApplicationGateway에 대한 해당 설정 내에 포함된 새 경로 규칙으로 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="8ecae-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ecae-121">PARAMETERS</span></span>

### <span data-ttu-id="8ecae-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8ecae-122">-BackendAddressPool</span></span>
<span data-ttu-id="8ecae-123">게이트웨이 경로 규칙 구성 설정에 추가할 백안 주소 풀 설정의 컬렉션에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="8ecae-124">이 개체 참조는 이와 유사한 New-AzApplicationGatewayBackendAddressPool cmdlet 및 구문을 사용하여 만들 수 있습니다. `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="8ecae-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="8ecae-125">이전 명령은 주소 풀에 두 개의 IP 주소(192.16.1.1 및 192.168.1.2)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="8ecae-126">IP 주소는 따옴표로 묶고 콤마를 사용하여 구분됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="8ecae-127">그러면 결과 변수인 $AddressPool *DefaultBackendAddressPool* 매개 변수에 대한 매개 변수 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="8ecae-128">백end 주소 풀은 백end 서버의 IP 주소를 나타 내는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="8ecae-129">이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="8ecae-130">이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendAddressPoolId* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecae-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8ecae-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="8ecae-132">게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백드 주소 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="8ecae-133">주소 풀 IDD는 Get-AzApplicationGatewayBackendAddressPool 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="8ecae-134">ID가 있는 후 *DefaultBackendAddressPool 매개 변수 대신 DefaultBackendAddressPoolId* 매개 변수를 사용할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="8ecae-135">예: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" 백end 주소 풀은 백end 서버의 IP 주소를 나타남</span><span class="sxs-lookup"><span data-stu-id="8ecae-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="8ecae-136">이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecae-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8ecae-137">-BackendHttpSettings</span></span>
<span data-ttu-id="8ecae-138">게이트웨이 경로 규칙 구성 설정에 추가할 백end HTTP 설정 컬렉션에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="8ecae-139">New-AzApplicationGatewayBackendHttpSettings cmdlet과 비슷한 구문을 사용하여 이 개체 참조를 만들 수 있습니다. $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" 결과 변수 $HttpSettings *DefaultBackendAddressPool* 매개 변수에 대한 매개 변수 값으로 사용할 수 있습니다. -DefaultBackendHttpSettings $HttpSettings 백 $HttpSettings HTTP 설정은 백end 풀에 대한 포트, 프로토콜 및 쿠키 기반 속성과 같은 속성을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="8ecae-140">이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendHttpSettingsId 매개* 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecae-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="8ecae-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="8ecae-142">게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백end HTTP 설정 컬렉션의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="8ecae-143">HTTP 설정은 Get-AzApplicationGatewayBackendHttpSettings cmdlet을 사용하여 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="8ecae-144">ID가 있는 후 *DefaultBackendHttpSettings 매개 변수 대신 DefaultBackendHttpSettingsId* 매개 변수를 사용할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="8ecae-145">예: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" 백end HTTP 설정은 포트, 프로토콜 등의 속성을 구성합니다. 백end 풀에 대한 쿠키 기반의 취미입니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="8ecae-146">이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendHttpSettings 매개* 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecae-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecae-147">-FirewallPolicy</span></span>
<span data-ttu-id="8ecae-148">최상위 방화벽 정책에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="8ecae-149">개체 참조는 cmdlet을 사용하여 New-AzApplicationGatewayWebApplicationFirewallPolicy 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="8ecae-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" 위의 commandlet을 사용하여 만든 방화벽 정책을 경로 규칙 수준에서 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="8ecae-151">위의 명령은 기본 정책 설정 및 관리 규칙을 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="8ecae-152">사용자는 기본값 대신 각각 정책 및 데이터 형식을 사용하여 PolicySettings, ManagedRules를 New-AzApplicationGatewayFirewallPolicySettings New-AzApplicationGatewayFirewallPolicyManagedRules 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecae-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8ecae-153">-FirewallPolicyId</span></span>
<span data-ttu-id="8ecae-154">기존 최상위 웹 애플리케이션 방화벽 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="8ecae-155">Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet을 사용하여 방화벽 정책 Get-AzApplicationGatewayWebApplicationFirewallPolicy 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="8ecae-156">ID가 있는 경우 *FirewallPolicy* 매개 변수 대신 *FirewallPolicyId* 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="8ecae-157">예: -FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="8ecae-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecae-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecae-158">-DefaultProfile</span></span>
<span data-ttu-id="8ecae-159">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ecae-160">-Name</span><span class="sxs-lookup"><span data-stu-id="8ecae-160">-Name</span></span>
<span data-ttu-id="8ecae-161">이 cmdlet에서 만드는 경로 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8ecae-162">-Paths</span><span class="sxs-lookup"><span data-stu-id="8ecae-162">-Paths</span></span>
<span data-ttu-id="8ecae-163">하나 이상의 애플리케이션 게이트웨이 경로 규칙을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-163">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecae-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecae-164">-RedirectConfiguration</span></span>
<span data-ttu-id="8ecae-165">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecae-165">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecae-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8ecae-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="8ecae-167">Application Gateway RedirectConfiguration의 ID</span><span class="sxs-lookup"><span data-stu-id="8ecae-167">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecae-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecae-168">-RewriteRuleSet</span></span>
<span data-ttu-id="8ecae-169">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecae-169">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecae-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="8ecae-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="8ecae-171">Application Gateway RewriteRuleSet의 ID</span><span class="sxs-lookup"><span data-stu-id="8ecae-171">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecae-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecae-172">CommonParameters</span></span>
<span data-ttu-id="8ecae-173">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecae-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecae-174">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8ecae-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecae-175">입력</span><span class="sxs-lookup"><span data-stu-id="8ecae-175">INPUTS</span></span>

### <span data-ttu-id="8ecae-176">없음</span><span class="sxs-lookup"><span data-stu-id="8ecae-176">None</span></span>

## <span data-ttu-id="8ecae-177">출력</span><span class="sxs-lookup"><span data-stu-id="8ecae-177">OUTPUTS</span></span>

### <span data-ttu-id="8ecae-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="8ecae-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="8ecae-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8ecae-179">NOTES</span></span>

## <span data-ttu-id="8ecae-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ecae-180">RELATED LINKS</span></span>

[<span data-ttu-id="8ecae-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8ecae-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8ecae-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ecae-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="8ecae-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8ecae-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8ecae-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8ecae-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)


[<span data-ttu-id="8ecae-185">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ecae-185">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="8ecae-186">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8ecae-186">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8ecae-187">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8ecae-187">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8ecae-188">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8ecae-188">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


