---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: 9118109de6262fd6214c80c41f2eafd415c440db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354134"
---
# <span data-ttu-id="904c7-101">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="904c7-101">Get-AzApplicationGateway</span></span>

## <span data-ttu-id="904c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="904c7-102">SYNOPSIS</span></span>
<span data-ttu-id="904c7-103">애플리케이션 게이트웨이를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="904c7-103">Gets an application gateway.</span></span>

## <span data-ttu-id="904c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="904c7-104">SYNTAX</span></span>

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="904c7-105">설명</span><span class="sxs-lookup"><span data-stu-id="904c7-105">DESCRIPTION</span></span>
<span data-ttu-id="904c7-106">**Get-AzApplicationGateway** cmdlet은 애플리케이션 게이트웨이를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="904c7-106">The **Get-AzApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="904c7-107">예제</span><span class="sxs-lookup"><span data-stu-id="904c7-107">EXAMPLES</span></span>

### <span data-ttu-id="904c7-108">예제 1: 지정된 애플리케이션 게이트웨이를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="904c7-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
ForceFirewallPolicyAssociation      :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="904c7-109">이 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="904c7-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="904c7-110">예제 2: 리소스 그룹의 애플리케이션 게이트웨이 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="904c7-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -ResourceGroupName "ResourceGroup01"

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
ForceFirewallPolicyAssociation      :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="904c7-111">이 명령은 ResourceGroup01이라는 리소스 그룹에 있는 모든 애플리케이션 게이트웨이의 목록을 $AppGwList 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="904c7-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="904c7-112">예제 3: 구독에서 애플리케이션 게이트웨이 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="904c7-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
ForceFirewallPolicyAssociation      :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="904c7-113">이 명령은 구독에 있는 모든 애플리케이션 게이트웨이의 목록을 $AppGwList 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="904c7-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="904c7-114">예제 4: 필터링을 사용하여 구독의 애플리케이션 게이트웨이 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="904c7-114">Example 4: Get a list of application gateways in a subscription using filtering</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -Name ApplicationGateway*

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
ForceFirewallPolicyAssociation      :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="904c7-115">이 명령은 "ApplicationGateway01"으로 시작하는 구독의 모든 애플리케이션 게이트웨이 목록을 $AppGwList 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="904c7-115">This command gets a list of all the application gateways in the subscription that start with "ApplicationGateway01" and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="904c7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="904c7-116">PARAMETERS</span></span>

### <span data-ttu-id="904c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="904c7-117">-DefaultProfile</span></span>
<span data-ttu-id="904c7-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="904c7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="904c7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="904c7-119">-Name</span></span>
<span data-ttu-id="904c7-120">이 cmdlet이 얻을 애플리케이션 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="904c7-120">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="904c7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="904c7-121">-ResourceGroupName</span></span>
<span data-ttu-id="904c7-122">애플리케이션 게이트웨이를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="904c7-122">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="904c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="904c7-123">CommonParameters</span></span>
<span data-ttu-id="904c7-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="904c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="904c7-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="904c7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="904c7-126">입력</span><span class="sxs-lookup"><span data-stu-id="904c7-126">INPUTS</span></span>

### <span data-ttu-id="904c7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="904c7-127">System.String</span></span>

## <span data-ttu-id="904c7-128">출력</span><span class="sxs-lookup"><span data-stu-id="904c7-128">OUTPUTS</span></span>

### <span data-ttu-id="904c7-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="904c7-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="904c7-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="904c7-130">NOTES</span></span>

## <span data-ttu-id="904c7-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="904c7-131">RELATED LINKS</span></span>

[<span data-ttu-id="904c7-132">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="904c7-132">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


