---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214877"
---
# <span data-ttu-id="db177-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db177-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="db177-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db177-102">SYNOPSIS</span></span>
<span data-ttu-id="db177-103">응용 프로그램 게이트웨이 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db177-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="db177-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db177-104">SYNTAX</span></span>

### <span data-ttu-id="db177-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="db177-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db177-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="db177-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db177-107">설명은</span><span class="sxs-lookup"><span data-stu-id="db177-107">DESCRIPTION</span></span>
<span data-ttu-id="db177-108">**새 AzApplicationGatewayPathRuleConfig** cmdlet은 응용 프로그램 게이트웨이 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db177-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="db177-109">이 cmdlet에서 만든 규칙을 URL 경로 맵 구성 설정 컬렉션에 추가 하 고 게이트웨이에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="db177-110">경로 맵 구성 설정은 응용 프로그램 게이트웨이 부하 분산에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db177-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="db177-111">예제의</span><span class="sxs-lookup"><span data-stu-id="db177-111">EXAMPLES</span></span>

### <span data-ttu-id="db177-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="db177-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="db177-113">이러한 명령은 새 응용 프로그램 게이트웨이 경로 규칙을 만든 다음 **추가-AzApplicationGatewayUrlPathMapConfig** cmdlet을 사용 하 여 해당 규칙을 응용 프로그램 게이트웨이에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="db177-114">이렇게 하려면 첫 번째 명령은 게이트웨이 ContosoApplicationGateway에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db177-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="db177-115">이 개체 참조는 $Gateway 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db177-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="db177-116">다음 두 명령은 백 엔드 주소 풀 및 백 엔드 HTTP 설정 개체를 만듭니다. 경로 규칙 개체를 만들기 위해서는 이러한 개체 (변수 $AddressPool 및 $HttpSettings에 저장)가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="db177-117">네 번째 명령은 path 규칙 개체를 만들고 $PathRuleConfig 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db177-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="db177-118">다섯 번째 명령은 **AzApplicationGatewayUrlPathMapConfig 추가** 를 사용 하 여 구성 설정 및 해당 설정에 포함 된 새 경로 규칙을 ContosoApplicationGateway에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="db177-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="db177-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="db177-120">이러한 명령은 이름이 "base" 인 경로 규칙을 만들고, 경로를 "$AddressPool BackendAddressPool"로 "/base"로 사용 하 고, $HttpSettings BackendHttpSettings와 $firewallPolicy FirewallPolicy로, 그리고 해당 설정 내에 포함 된 새 경로 규칙을 ContosoApplicationGateway에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="db177-121">변수</span><span class="sxs-lookup"><span data-stu-id="db177-121">PARAMETERS</span></span>

### <span data-ttu-id="db177-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="db177-122">-BackendAddressPool</span></span>
<span data-ttu-id="db177-123">게이트웨이 경로 규칙 구성 설정에 추가할 백 엔드 주소 풀 설정 컬렉션에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="db177-124">다음과 같은 New-AzApplicationGatewayBackendAddressPool cmdlet 및 구문을 사용 하 여이 개체 참조를 만들 수 있습니다. `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="db177-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="db177-125">앞의 명령은 두 개의 IP 주소 (192.16.1.1 및 192.168.1.2)를 주소 풀에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="db177-126">IP 주소는 인용 부호로 묶여 있고 쉼표로 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db177-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="db177-127">결과 변수인 $AddressPool는 *DefaultBackendAddressPool* 매개 변수의 매개 변수 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="db177-128">백 엔드 주소 풀은 백 엔드 서버의 IP 주소를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db177-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="db177-129">이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="db177-130">이 매개 변수를 사용 하는 경우 동일한 명령에서 *DefaultBackendAddressPoolId* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="db177-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="db177-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="db177-132">게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백엔드 주소 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="db177-133">주소 풀 Id는 Get-AzApplicationGatewayBackendAddressPool cmdlet을 사용 하 여 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="db177-134">ID를 설정한 후에는 *DefaultBackendAddressPool* 매개 변수 대신 *DefaultBackendAddressPoolId* 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="db177-135">예를 들어:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" 백 엔드 주소 풀은 백 엔드 서버의 IP 주소를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db177-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="db177-136">이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="db177-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="db177-137">-BackendHttpSettings</span></span>
<span data-ttu-id="db177-138">게이트웨이 경로 규칙 구성 설정에 추가할 백 엔드 HTTP 설정 컬렉션에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="db177-139">다음과 같은 New-AzApplicationGatewayBackendHttpSettings cmdlet 및 구문을 사용 하 여이 개체 참조를 만들 수 있습니다. $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSettings"--포트 80-프로토콜 "Http"-CookieBasedAffinity "사용 안 함" 결과 변수 $HttpSettings는 *DefaultBackendAddressPool* 매개 변수의 매개 변수 값으로 사용할 수 있습니다.-DefaultBackendHttpSettings $HttpSettings 백 엔드 Http 설정에 대해 포트, 프로토콜 및 쿠키 기반 선호도와 같은 속성을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="db177-140">이 매개 변수를 사용 하는 경우 동일한 명령에서 *DefaultBackendHttpSettingsId* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="db177-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="db177-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="db177-142">게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백 엔드 HTTP 설정 컬렉션의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="db177-143">HTTP 설정 Id는 Get-AzApplicationGatewayBackendHttpSettings cmdlet을 사용 하 여 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="db177-144">ID를 설정한 후에는 *DefaultBackendHttpSettings* 매개 변수 대신 *DefaultBackendHttpSettingsId* 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="db177-145">예를 들어,-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" 백 엔드 HTTP 설정은 포트, 프로토콜 및 백 엔드 풀에 대 한 쿠키 기반 선호도와 같은 속성을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="db177-146">이 매개 변수를 사용 하는 경우 동일한 명령에서 *DefaultBackendHttpSettings* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="db177-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="db177-147">-FirewallPolicy</span></span>
<span data-ttu-id="db177-148">최상위 수준의 방화벽 정책에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="db177-149">New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet을 사용 하 여 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="db177-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" 위를 사용 하 여 만든 방화벽 정책은 경로 규칙 수준에서 참조 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="db177-151">위의 명령으로 기본 정책 설정 및 관리 되는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db177-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="db177-152">기본값 대신 사용자는 각각 New-AzApplicationGatewayFirewallPolicySettings 및 New-AzApplicationGatewayFirewallPolicyManagedRules을 사용 하 여 PolicySettings, ManagedRules를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db177-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="db177-153">-FirewallPolicyId</span></span>
<span data-ttu-id="db177-154">기존 상위 수준 웹 응용 프로그램 방화벽 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="db177-155">방화벽 정책 Id는 Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet을 사용 하 여 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="db177-156">ID를 설정한 후에는 *FirewallPolicy* 매개 변수 대신 *FirewallPolicyId* 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db177-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="db177-157">예를 들어-FirewallPolicyId "/subscriptions/<구독 id>/Resourcegroup/<리소스 그룹-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="db177-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db177-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db177-158">-DefaultProfile</span></span>
<span data-ttu-id="db177-159">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db177-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db177-160">-이름</span><span class="sxs-lookup"><span data-stu-id="db177-160">-Name</span></span>
<span data-ttu-id="db177-161">이 cmdlet이 만드는 경로 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="db177-162">-경로</span><span class="sxs-lookup"><span data-stu-id="db177-162">-Paths</span></span>
<span data-ttu-id="db177-163">하나 이상의 응용 프로그램 게이트웨이 경로 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="db177-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="db177-164">-RedirectConfiguration</span></span>
<span data-ttu-id="db177-165">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="db177-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="db177-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="db177-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="db177-167">응용 프로그램 게이트웨이 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="db177-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="db177-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="db177-168">-RewriteRuleSet</span></span>
<span data-ttu-id="db177-169">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="db177-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="db177-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="db177-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="db177-171">응용 프로그램 게이트웨이 RewriteRuleSet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="db177-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="db177-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db177-172">CommonParameters</span></span>
<span data-ttu-id="db177-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db177-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db177-174">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db177-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db177-175">입력</span><span class="sxs-lookup"><span data-stu-id="db177-175">INPUTS</span></span>

### <span data-ttu-id="db177-176">않아야</span><span class="sxs-lookup"><span data-stu-id="db177-176">None</span></span>

## <span data-ttu-id="db177-177">출력</span><span class="sxs-lookup"><span data-stu-id="db177-177">OUTPUTS</span></span>

### <span data-ttu-id="db177-178">PSApplicationGatewayPathRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="db177-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="db177-179">상속자</span><span class="sxs-lookup"><span data-stu-id="db177-179">NOTES</span></span>

## <span data-ttu-id="db177-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db177-180">RELATED LINKS</span></span>

[<span data-ttu-id="db177-181">추가-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="db177-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="db177-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db177-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="db177-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="db177-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="db177-184">새로운 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="db177-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="db177-185">새로운 AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="db177-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="db177-186">새로운 AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db177-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="db177-187">새로운 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="db177-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="db177-188">제거-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="db177-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="db177-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="db177-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


