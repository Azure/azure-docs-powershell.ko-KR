---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b343ecbabd66f32be30f4aff1b0a44c7ddf186d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985852"
---
# <span data-ttu-id="0f0a2-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f0a2-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="0f0a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0a2-103">애플리케이션 게이트웨이 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="0f0a2-104">구문</span><span class="sxs-lookup"><span data-stu-id="0f0a2-104">SYNTAX</span></span>

### <span data-ttu-id="0f0a2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f0a2-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f0a2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0f0a2-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f0a2-107">설명</span><span class="sxs-lookup"><span data-stu-id="0f0a2-107">DESCRIPTION</span></span>
<span data-ttu-id="0f0a2-108">**New-AzApplicationGatewayPathRuleConfig** cmdlet은 애플리케이션 게이트웨이 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="0f0a2-109">이 cmdlet에서 만든 규칙은 URL 경로 맵 구성 설정 컬렉션에 추가한 다음 게이트웨이에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="0f0a2-110">경로 맵 구성 설정은 애플리케이션 게이트웨이 부하 분산에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="0f0a2-111">예제</span><span class="sxs-lookup"><span data-stu-id="0f0a2-111">EXAMPLES</span></span>

### <span data-ttu-id="0f0a2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0f0a2-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="0f0a2-113">이러한 명령은 새 애플리케이션 게이트웨이 경로 규칙을 만든 다음 **Add-AzApplicationGatewayUrlPathpConfig** cmdlet을 사용하여 해당 규칙을 애플리케이션 게이트웨이에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="0f0a2-114">이렇게 하여 첫 번째 명령은 게이트웨이 ContosoApplicationGateway에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="0f0a2-115">이 개체 참조는 이라는 변수에 $Gateway.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="0f0a2-116">다음 두 명령은 백던드 주소 풀 및 백end HTTP 설정 개체를 만듭니다. 경로 규칙 개체를 만들기 위해 이러한 개체($AddressPool 및 $HttpSettings)가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="0f0a2-117">네 번째 명령은 경로 규칙 개체를 만들고 이라는 변수에 $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="0f0a2-118">다섯 번째 명령은 **Add-AzApplicationGatewayUrlPathMapConfig를** 사용하여 구성 설정 및 해당 설정에 포함된 새 경로 규칙을 ContosoApplicationGateway에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="0f0a2-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="0f0a2-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="0f0a2-120">이 명령은 이름과 함께 경로 규칙을 만듭니다. "/base"로 경로, BackendAddressPool을 $AddressPool BackendAddressPool, $firewallPolicy BackendHttpSettings를 $HttpSettings.ngs 및 ContosoApplicationGateway에 대한 해당 설정에 포함된 새 경로 규칙으로 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="0f0a2-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0f0a2-121">PARAMETERS</span></span>

### <span data-ttu-id="0f0a2-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f0a2-122">-BackendAddressPool</span></span>
<span data-ttu-id="0f0a2-123">게이트웨이 경로 규칙 구성 설정에 추가할 백드 주소 풀 설정의 컬렉션에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="0f0a2-124">이와 유사한 New-AzApplicationGatewayBackendAddressPool cmdlet 및 구문을 사용하여 이 개체 참조를 만들 수 있습니다. `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="0f0a2-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="0f0a2-125">이전 명령은 주소 풀에 두 개의 IP 주소(192.16.1.1 및 192.168.1.2)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="0f0a2-126">IP 주소는 따옴표로 묶고 콤마를 사용하여 구분됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="0f0a2-127">그러면 결과 변수인 $AddressPool *DefaultBackendAddressPool* 매개 변수의 매개 변수 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="0f0a2-128">백던드 주소 풀은 백end 서버의 IP 주소를 나타내고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="0f0a2-129">이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="0f0a2-130">이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendAddressPoolId* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="0f0a2-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0f0a2-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="0f0a2-132">게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백드 주소 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="0f0a2-133">주소 풀 아이디는 Get-AzApplicationGatewayBackendAddressPool cmdlet을 사용하여 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="0f0a2-134">ID가 있는 후 *DefaultBackendAddressPool 매개 변수 대신 DefaultBackendAddressPool* 매개 변수를 사용할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="0f0a2-135">예: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" 백end 주소 풀은 백end 서버의 IP 주소를 나타내고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="0f0a2-136">이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="0f0a2-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0f0a2-137">-BackendHttpSettings</span></span>
<span data-ttu-id="0f0a2-138">게이트웨이 경로 규칙 구성 설정에 추가할 백end HTTP 설정 컬렉션에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="0f0a2-139">이와 유사한 New-AzApplicationGatewayBackendHttpSettings cmdlet 및 구문을 사용하여 이 개체 참조를 만들 수 있습니다. $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" 결과 변수, $HttpSettings *기본BackendAddressPool* 매개 변수에 대한 매개 변수 값으로 사용할 수 있습니다. -DefaultBackendHttpSettings $HttpSettings 백end HTTP 설정은 백end 풀에 대한 포트, 프로토콜 및 쿠키 기반 연결성과 같은 속성을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="0f0a2-140">이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendHttpSettingsId* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="0f0a2-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="0f0a2-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="0f0a2-142">게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백END HTTP 설정 컬렉션의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="0f0a2-143">HTTP 설정 아이디는 Get-AzApplicationGatewayBackendHttpSettings cmdlet을 사용하여 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="0f0a2-144">ID가 있는 후 *DefaultBackendHttpSettings 매개 변수 대신 DefaultBackendHttpSettings 매개* 변수를 사용할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="0f0a2-145">예: -DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" 백end HTTP 설정은 포트, 프로토콜, 백end 풀에 대한 쿠키 기반의 에피니티를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="0f0a2-146">이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendHttpSettings* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="0f0a2-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0f0a2-147">-FirewallPolicy</span></span>
<span data-ttu-id="0f0a2-148">최상위 방화벽 정책에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="0f0a2-149">개체 참조는 cmdlet을 사용하여 New-AzApplicationGatewayWebApplicationFirewallPolicy 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="0f0a2-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" 위의 명령줄을 사용하여 만든 방화벽 정책을 경로 규칙 수준에서 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="0f0a2-151">위의 명령은 기본 정책 설정 및 관리되는 규칙을 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="0f0a2-152">사용자는 기본 값 대신 각각 New-AzApplicationGatewayFirewallPolicySettings 사용하여 PolicySettings, ManagedRules를 New-AzApplicationGatewayFirewallPolicySettings New-AzApplicationGatewayFirewallPolicyManagedRules 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0a2-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="0f0a2-153">-FirewallPolicyId</span></span>
<span data-ttu-id="0f0a2-154">기존 최상위 웹 애플리케이션 방화벽 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="0f0a2-155">방화벽 정책 신분은 cmdlet을 사용하여 Get-AzApplicationGatewayWebApplicationFirewallPolicy 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="0f0a2-156">ID가 있는 후 FirewallPolicy 매개 변수 대신 *FirewallPolicyId* 매개 변수를 *사용할 수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="0f0a2-157">예를 들어 -FirewallPolicyId "/subscriptions/<구독-id>/resourceGroups/<리소스 그룹 id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="0f0a2-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0a2-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0a2-158">-DefaultProfile</span></span>
<span data-ttu-id="0f0a2-159">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f0a2-160">-Name</span><span class="sxs-lookup"><span data-stu-id="0f0a2-160">-Name</span></span>
<span data-ttu-id="0f0a2-161">이 cmdlet이 만드는 경로 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0f0a2-162">-Paths</span><span class="sxs-lookup"><span data-stu-id="0f0a2-162">-Paths</span></span>
<span data-ttu-id="0f0a2-163">하나 이상의 애플리케이션 게이트웨이 경로 규칙을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="0f0a2-164">-리디렉션 구성</span><span class="sxs-lookup"><span data-stu-id="0f0a2-164">-RedirectConfiguration</span></span>
<span data-ttu-id="0f0a2-165">애플리케이션 게이트웨이 리디렉션 구성</span><span class="sxs-lookup"><span data-stu-id="0f0a2-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="0f0a2-166">-리디렉션ConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0f0a2-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="0f0a2-167">애플리케이션 게이트웨이 리디렉션 구성의 ID</span><span class="sxs-lookup"><span data-stu-id="0f0a2-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="0f0a2-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0f0a2-168">-RewriteRuleSet</span></span>
<span data-ttu-id="0f0a2-169">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0f0a2-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="0f0a2-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="0f0a2-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="0f0a2-171">애플리케이션 게이트웨이 RewriteRuleSet의 ID</span><span class="sxs-lookup"><span data-stu-id="0f0a2-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="0f0a2-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0a2-172">CommonParameters</span></span>
<span data-ttu-id="0f0a2-173">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0a2-174">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0a2-175">입력</span><span class="sxs-lookup"><span data-stu-id="0f0a2-175">INPUTS</span></span>

### <span data-ttu-id="0f0a2-176">없음</span><span class="sxs-lookup"><span data-stu-id="0f0a2-176">None</span></span>

## <span data-ttu-id="0f0a2-177">출력</span><span class="sxs-lookup"><span data-stu-id="0f0a2-177">OUTPUTS</span></span>

### <span data-ttu-id="0f0a2-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="0f0a2-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="0f0a2-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0f0a2-179">NOTES</span></span>

## <span data-ttu-id="0f0a2-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f0a2-180">RELATED LINKS</span></span>

[<span data-ttu-id="0f0a2-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0f0a2-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0f0a2-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f0a2-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="0f0a2-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0f0a2-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0f0a2-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f0a2-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0f0a2-185">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0f0a2-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="0f0a2-186">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f0a2-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="0f0a2-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0f0a2-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0f0a2-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0f0a2-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0f0a2-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0f0a2-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


