---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaypathruleconfig
schema: 2.0.0
ms.openlocfilehash: 95865de8e99ad09a755329b742f69ebe1e935d72
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880389"
---
# <span data-ttu-id="e6c31-101">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6c31-101">New-AzureRmApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="e6c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6c31-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c31-103">응용 프로그램 게이트웨이 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-103">Creates an application gateway path rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6c31-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6c31-104">SYNTAX</span></span>

### <span data-ttu-id="e6c31-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6c31-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6c31-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e6c31-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6c31-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e6c31-107">DESCRIPTION</span></span>
<span data-ttu-id="e6c31-108">**새 AzureRmApplicationGatewayPathRuleConfig** cmdlet은 응용 프로그램 게이트웨이 경로 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-108">The **New-AzureRmApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="e6c31-109">이 cmdlet에서 만든 규칙을 URL 경로 맵 구성 설정 컬렉션에 추가 하 고 게이트웨이에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="e6c31-110">경로 맵 구성 설정은 응용 프로그램 게이트웨이 부하 분산에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="e6c31-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e6c31-111">EXAMPLES</span></span>

### <span data-ttu-id="e6c31-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e6c31-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="e6c31-113">이러한 명령은 새 응용 프로그램 게이트웨이 경로 규칙을 만든 다음 **추가-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet을 사용 하 여 해당 규칙을 응용 프로그램 게이트웨이에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-113">These commands create a new application gateway path rule and then use the **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="e6c31-114">이렇게 하려면 첫 번째 명령은 게이트웨이 ContosoApplicationGateway에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="e6c31-115">이 개체 참조는 $Gateway 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="e6c31-116">다음 두 명령은 백 엔드 주소 풀 및 백 엔드 HTTP 설정 개체를 만듭니다. 경로 규칙 개체를 만들기 위해서는 이러한 개체 (변수 $AddressPool 및 $HttpSettings에 저장)가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="e6c31-117">네 번째 명령은 path 규칙 개체를 만들고 $PathRuleConfig 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="e6c31-118">다섯 번째 명령은 **AzureRmApplicationGatewayUrlPathMapConfig 추가** 를 사용 하 여 구성 설정 및 해당 설정에 포함 된 새 경로 규칙을 ContosoApplicationGateway에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-118">The fifth command uses **Add-AzureRmApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="e6c31-119">변수</span><span class="sxs-lookup"><span data-stu-id="e6c31-119">PARAMETERS</span></span>

### <span data-ttu-id="e6c31-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e6c31-120">-BackendAddressPool</span></span>
<span data-ttu-id="e6c31-121">게이트웨이 경로 규칙 구성 설정에 추가할 백 엔드 주소 풀 설정 컬렉션에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="e6c31-122">다음과 같은 New-AzureRmApplicationGatewayBackendAddressPool cmdlet 및 구문을 사용 하 여이 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-122">You can create this object reference by using the New-AzureRmApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="e6c31-123">앞의 명령은 두 개의 IP 주소 (192.16.1.1 및 192.168.1.2)를 주소 풀에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="e6c31-124">IP 주소는 인용 부호로 묶여 있고 쉼표로 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="e6c31-125">결과 변수인 $AddressPool는 *DefaultBackendAddressPool* 매개 변수의 매개 변수 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="e6c31-126">백 엔드 주소 풀은 백 엔드 서버의 IP 주소를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="e6c31-127">이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="e6c31-128">이 매개 변수를 사용 하는 경우 동일한 명령에서 *DefaultBackendAddressPoolId* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c31-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e6c31-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="e6c31-130">게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백엔드 주소 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="e6c31-131">주소 풀 Id는 Get-AzureRmApplicationGatewayBackendAddressPool cmdlet을 사용 하 여 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-131">Address pool IDs can be returned by using the Get-AzureRmApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="e6c31-132">ID를 설정한 후에는 *DefaultBackendAddressPool* 매개 변수 대신 *DefaultBackendAddressPoolId* 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="e6c31-133">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-133">For instance:</span></span>

<span data-ttu-id="e6c31-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="e6c31-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="e6c31-135">백 엔드 주소 풀은 백 엔드 서버의 IP 주소를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="e6c31-136">이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c31-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e6c31-137">-BackendHttpSettings</span></span>
<span data-ttu-id="e6c31-138">게이트웨이 경로 규칙 구성 설정에 추가할 백 엔드 HTTP 설정 컬렉션에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="e6c31-139">다음과 같은 New-AzureRmApplicationGatewayBackendHttpSettings cmdlet 및 구문을 사용 하 여이 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-139">You can create this object reference by using the New-AzureRmApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="e6c31-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-Name "ContosoHttpSetings"-포트 80-프로토콜 "Http"-CookieBasedAffinity "Disabled"</span><span class="sxs-lookup"><span data-stu-id="e6c31-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="e6c31-141">그런 다음 *DefaultBackendAddressPool* 매개 변수에 대 한 매개 변수 값으로 결과 변수 $HttpSettings를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="e6c31-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="e6c31-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="e6c31-143">백 엔드 HTTP 설정은 포트, 프로토콜 및 백 엔드 풀에 대 한 쿠키 기반 선호도와 같은 속성을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="e6c31-144">이 매개 변수를 사용 하는 경우 동일한 명령에서 *DefaultBackendHttpSettingsId* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c31-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e6c31-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="e6c31-146">게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백 엔드 HTTP 설정 컬렉션의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="e6c31-147">HTTP 설정 Id는 Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet을 사용 하 여 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-147">HTTP setting IDs can be returned by using the Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="e6c31-148">ID를 설정한 후에는 *DefaultBackendHttpSettings* 매개 변수 대신 *DefaultBackendHttpSettingsId* 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="e6c31-149">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-149">For instance:</span></span>

<span data-ttu-id="e6c31-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="e6c31-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="e6c31-151">백 엔드 HTTP 설정은 포트, 프로토콜 및 백 엔드 풀에 대 한 쿠키 기반 선호도와 같은 속성을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="e6c31-152">이 매개 변수를 사용 하는 경우 동일한 명령에서 *DefaultBackendHttpSettings* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c31-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c31-153">-DefaultProfile</span></span>
<span data-ttu-id="e6c31-154">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6c31-155">-이름</span><span class="sxs-lookup"><span data-stu-id="e6c31-155">-Name</span></span>
<span data-ttu-id="e6c31-156">이 cmdlet이 만드는 경로 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-156">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c31-157">-경로</span><span class="sxs-lookup"><span data-stu-id="e6c31-157">-Paths</span></span>
<span data-ttu-id="e6c31-158">하나 이상의 응용 프로그램 게이트웨이 경로 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-158">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c31-159">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6c31-159">-RedirectConfiguration</span></span>
<span data-ttu-id="e6c31-160">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6c31-160">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c31-161">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e6c31-161">-RedirectConfigurationId</span></span>
<span data-ttu-id="e6c31-162">응용 프로그램 게이트웨이 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-162">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c31-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c31-163">CommonParameters</span></span>
<span data-ttu-id="e6c31-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c31-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6c31-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c31-166">입력</span><span class="sxs-lookup"><span data-stu-id="e6c31-166">INPUTS</span></span>

###  
<span data-ttu-id="e6c31-167">**New-AzureRmApplicationGatewayPathRuleConfig** 는 파이프라인 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c31-167">**New-AzureRmApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="e6c31-168">출력</span><span class="sxs-lookup"><span data-stu-id="e6c31-168">OUTPUTS</span></span>

###  
<span data-ttu-id="e6c31-169">AzureRmApplicationGatewayPathRuleConfig- **PSApplicationGatewayPathRule** 개체의 새 인스턴스를 만듭니다 **(새)** .</span><span class="sxs-lookup"><span data-stu-id="e6c31-169">**New-AzureRmApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="e6c31-170">상속자</span><span class="sxs-lookup"><span data-stu-id="e6c31-170">NOTES</span></span>

## <span data-ttu-id="e6c31-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6c31-171">RELATED LINKS</span></span>

[<span data-ttu-id="e6c31-172">추가-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e6c31-172">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e6c31-173">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6c31-173">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="e6c31-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e6c31-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e6c31-175">새로운 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e6c31-175">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e6c31-176">새로운 AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e6c31-176">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="e6c31-177">새로운 AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6c31-177">New-AzureRmApplicationGatewayPathRuleConfig</span></span>](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="e6c31-178">새로운 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e6c31-178">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e6c31-179">제거-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e6c31-179">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e6c31-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e6c31-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


