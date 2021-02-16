---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 94fbc1e9a4ae8b7befe6961a9648174770458583
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400215"
---
# <span data-ttu-id="20f5a-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="20f5a-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="20f5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="20f5a-103">애플리케이션 게이트웨이 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="20f5a-104">구문</span><span class="sxs-lookup"><span data-stu-id="20f5a-104">SYNTAX</span></span>

### <span data-ttu-id="20f5a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="20f5a-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20f5a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="20f5a-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20f5a-107">설명</span><span class="sxs-lookup"><span data-stu-id="20f5a-107">DESCRIPTION</span></span>
<span data-ttu-id="20f5a-108">**New-AzApplicationGatewayPathRuleConfig** cmdlet은 애플리케이션 게이트웨이 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="20f5a-109">이 cmdlet에서 만든 규칙은 URL 경로 맵 구성 설정의 컬렉션에 추가한 다음 게이트웨이에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="20f5a-110">경로 맵 구성 설정은 애플리케이션 게이트웨이 부하 분산에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="20f5a-111">예제</span><span class="sxs-lookup"><span data-stu-id="20f5a-111">EXAMPLES</span></span>

### <span data-ttu-id="20f5a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="20f5a-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="20f5a-113">이러한 명령은 새 애플리케이션 게이트웨이 경로 규칙을 만든 다음 **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet을 사용하여 애플리케이션 게이트웨이에 해당 규칙을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="20f5a-114">이를 위해 첫 번째 명령은 ContosoApplicationGateway 게이트웨이에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="20f5a-115">이 개체 참조는 $Gateway.</span><span class="sxs-lookup"><span data-stu-id="20f5a-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="20f5a-116">다음 두 명령은 백end 주소 풀 및 백end HTTP 설정 개체를 만듭니다. 경로 규칙 개체를 만들기 위해 이러한 개체($AddressPool 및 $HttpSettings 변수에 저장)가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="20f5a-117">네 번째 명령은 경로 규칙 개체를 만들고 경로 규칙이라는 변수에 $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="20f5a-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="20f5a-118">다섯 번째 명령은 **Add-AzApplicationGatewayUrlPathMapConfig를** 사용하여 구성 설정 및 해당 설정 내에 포함된 새 경로 규칙을 ContosoApplicationGateway에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="20f5a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20f5a-119">PARAMETERS</span></span>

### <span data-ttu-id="20f5a-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="20f5a-120">-BackendAddressPool</span></span>
<span data-ttu-id="20f5a-121">게이트웨이 경로 규칙 구성 설정에 추가할 백안 주소 풀 설정의 컬렉션에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="20f5a-122">이 개체 참조는 이와 유사한 New-AzApplicationGatewayBackendAddressPool cmdlet 및 구문을 사용하여 만들 수 있습니다. `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="20f5a-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="20f5a-123">이전 명령은 주소 풀에 두 개의 IP 주소(192.16.1.1 및 192.168.1.2)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="20f5a-124">IP 주소는 따옴표로 묶고 콤마를 사용하여 구분됩니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="20f5a-125">그러면 결과 변수인 $AddressPool *DefaultBackendAddressPool* 매개 변수에 대한 매개 변수 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="20f5a-126">백end 주소 풀은 백end 서버의 IP 주소를 나타 내는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="20f5a-127">이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="20f5a-128">이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendAddressPoolId* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="20f5a-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="20f5a-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="20f5a-130">게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백드 주소 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="20f5a-131">주소 풀 IDD는 Get-AzApplicationGatewayBackendAddressPool 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="20f5a-132">ID가 있는 후 *DefaultBackendAddressPool 매개 변수 대신 DefaultBackendAddressPoolId* 매개 변수를 사용할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="20f5a-133">예: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" 백end 주소 풀은 백end 서버의 IP 주소를 나타남</span><span class="sxs-lookup"><span data-stu-id="20f5a-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="20f5a-134">이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="20f5a-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="20f5a-135">-BackendHttpSettings</span></span>
<span data-ttu-id="20f5a-136">게이트웨이 경로 규칙 구성 설정에 추가할 백end HTTP 설정 컬렉션에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="20f5a-137">New-AzApplicationGatewayBackendHttpSettings cmdlet 및 이와 유사한 구문을 사용하여 이 개체 참조를 만들 수 있습니다. $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" 결과 변수 $HttpSettings *DefaultBackendAddressPool* 매개 변수에 대한 매개 변수 값으로 사용할 수 있습니다. -DefaultBackendHttpSettings $HttpSettings 백 $HttpSettings HTTP 설정은 백end 풀에 대한 포트, 프로토콜 및 쿠키 기반 속성과 같은 속성을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="20f5a-138">이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendHttpSettingsId 매개* 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="20f5a-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="20f5a-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="20f5a-140">게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백end HTTP 설정 컬렉션의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="20f5a-141">HTTP 설정은 Get-AzApplicationGatewayBackendHttpSettings cmdlet을 사용하여 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="20f5a-142">ID가 있는 후 *DefaultBackendHttpSettings 매개 변수 대신 DefaultBackendHttpSettingsId* 매개 변수를 사용할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="20f5a-143">예: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" 백end HTTP 설정은 포트, 프로토콜 등의 속성을 구성합니다. 백end 풀에 대한 쿠키 기반의 취미입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="20f5a-144">이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendHttpSettings 매개* 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="20f5a-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f5a-145">-DefaultProfile</span></span>
<span data-ttu-id="20f5a-146">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20f5a-147">-Name</span><span class="sxs-lookup"><span data-stu-id="20f5a-147">-Name</span></span>
<span data-ttu-id="20f5a-148">이 cmdlet에서 만드는 경로 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="20f5a-149">-Paths</span><span class="sxs-lookup"><span data-stu-id="20f5a-149">-Paths</span></span>
<span data-ttu-id="20f5a-150">하나 이상의 애플리케이션 게이트웨이 경로 규칙을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="20f5a-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="20f5a-151">-RedirectConfiguration</span></span>
<span data-ttu-id="20f5a-152">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="20f5a-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="20f5a-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="20f5a-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="20f5a-154">Application Gateway RedirectConfiguration의 ID</span><span class="sxs-lookup"><span data-stu-id="20f5a-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="20f5a-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20f5a-155">-RewriteRuleSet</span></span>
<span data-ttu-id="20f5a-156">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20f5a-156">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="20f5a-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="20f5a-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="20f5a-158">Application Gateway RewriteRuleSet의 ID</span><span class="sxs-lookup"><span data-stu-id="20f5a-158">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="20f5a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f5a-159">CommonParameters</span></span>
<span data-ttu-id="20f5a-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f5a-161">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="20f5a-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f5a-162">입력</span><span class="sxs-lookup"><span data-stu-id="20f5a-162">INPUTS</span></span>

### <span data-ttu-id="20f5a-163">없음</span><span class="sxs-lookup"><span data-stu-id="20f5a-163">None</span></span>

## <span data-ttu-id="20f5a-164">출력</span><span class="sxs-lookup"><span data-stu-id="20f5a-164">OUTPUTS</span></span>

### <span data-ttu-id="20f5a-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="20f5a-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="20f5a-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="20f5a-166">NOTES</span></span>

## <span data-ttu-id="20f5a-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20f5a-167">RELATED LINKS</span></span>

[<span data-ttu-id="20f5a-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="20f5a-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="20f5a-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20f5a-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="20f5a-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="20f5a-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="20f5a-171">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="20f5a-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)


[<span data-ttu-id="20f5a-172">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="20f5a-172">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="20f5a-173">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="20f5a-173">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="20f5a-174">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="20f5a-174">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="20f5a-175">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="20f5a-175">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


