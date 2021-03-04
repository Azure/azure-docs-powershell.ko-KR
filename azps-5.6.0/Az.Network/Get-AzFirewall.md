---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 56227c5c3df8f428e8d25329f8dbb9965ff502cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956955"
---
# <span data-ttu-id="2185d-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2185d-101">Get-AzFirewall</span></span>

## <span data-ttu-id="2185d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2185d-102">SYNOPSIS</span></span>
<span data-ttu-id="2185d-103">Azure 방화벽을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="2185d-104">구문</span><span class="sxs-lookup"><span data-stu-id="2185d-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2185d-105">설명</span><span class="sxs-lookup"><span data-stu-id="2185d-105">DESCRIPTION</span></span>
<span data-ttu-id="2185d-106">**Get-AzFirewall** cmdlet은 리소스 그룹에 하나 이상의 방화벽을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="2185d-107">예제</span><span class="sxs-lookup"><span data-stu-id="2185d-107">EXAMPLES</span></span>

### <span data-ttu-id="2185d-108">1: 리소스 그룹의 모든 방화벽 검색</span><span class="sxs-lookup"><span data-stu-id="2185d-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzFirewall -ResourceGroupName rgName

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="2185d-109">이 예제에서는 리소스 그룹 "rgName"의 모든 방화벽을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="2185d-110">2: 방화벽 이름 검색</span><span class="sxs-lookup"><span data-stu-id="2185d-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzFirewall -ResourceGroupName rgName -Name azFw

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="2185d-111">이 예제에서는 리소스 그룹 "rgName"에서 "azFw"라는 방화벽을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="2185d-112">3: 필터링을 사용하여 모든 방화벽 검색</span><span class="sxs-lookup"><span data-stu-id="2185d-112">3:  Retrieve all Firewalls with filtering</span></span>
```
Get-AzFirewall -Name azFw*

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="2185d-113">이 예제에서는 "azFw"로 시작하는 모든 방화벽을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="2185d-114">4: 방화벽을 검색한 다음 방화벽에 애플리케이션 규칙 컬렉션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="2185d-115">이 예제에서는 방화벽을 검색한 다음, AddApplicationRuleCollection 메서드를 호출하여 방화벽에 애플리케이션 규칙 컬렉션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="2185d-116">5: 방화벽을 검색한 다음 방화벽에 네트워크 규칙 컬렉션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "UDP" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="2185d-117">이 예제에서는 방화벽을 검색한 다음, AddNetworkRuleCollection 메서드를 호출하여 방화벽에 네트워크 규칙 컬렉션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="2185d-118">6: 방화벽을 검색한 다음 방화벽에서 이름으로 애플리케이션 규칙 컬렉션을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="2185d-119">이 예제에서는 방화벽을 검색한 다음 방화벽 개체에서 GetApplicationRuleCollectionByName 메서드를 호출하여 이름으로 규칙 컬렉션을 가져온다.</span><span class="sxs-lookup"><span data-stu-id="2185d-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="2185d-120">메서드 GetApplicationRuleCollectionByName의 규칙 컬렉션 이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="2185d-121">7: 방화벽을 검색한 다음 방화벽에서 이름으로 네트워크 규칙 컬렉션을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="2185d-122">이 예제에서는 방화벽을 검색한 다음 이름별 규칙 컬렉션을 가져온 다음 방화벽 개체에서 GetNetworkRuleCollectionByName을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="2185d-123">메서드 GetNetworkRuleCollectionByName의 규칙 컬렉션 이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="2185d-124">8: 방화벽을 검색한 다음 방화벽에서 이름으로 애플리케이션 규칙 컬렉션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="2185d-125">이 예제에서는 방화벽을 검색한 다음 방화벽 개체에서 RemoveApplicationRuleCollectionByName 메서드를 호출하여 이름별 규칙 컬렉션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="2185d-126">RemoveApplicationRuleCollectionByName 메서드에 대한 규칙 컬렉션 이름은 대소문자에 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="2185d-127">9: 방화벽을 검색한 다음 방화벽에서 이름으로 네트워크 규칙 컬렉션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="2185d-128">이 예제에서는 방화벽을 검색한 다음, 방화벽 개체에서 RemoveNetworkRuleCollectionByName 메서드를 호출하여 이름으로 규칙 컬렉션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="2185d-129">RemoveNetworkRuleCollectionByName 메서드에 대한 규칙 컬렉션 이름은 대소문자에 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="2185d-130">10: 방화벽을 검색한 다음 방화벽을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="2185d-131">이 예제에서는 방화벽을 검색하고 방화벽에 할당을 호출하여 방화벽과 연결된 구성(애플리케이션 및 네트워크 규칙 컬렉션)을 사용하여 방화벽 서비스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="2185d-132">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2185d-132">PARAMETERS</span></span>

### <span data-ttu-id="2185d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2185d-133">-DefaultProfile</span></span>
<span data-ttu-id="2185d-134">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2185d-135">-Name</span><span class="sxs-lookup"><span data-stu-id="2185d-135">-Name</span></span>
<span data-ttu-id="2185d-136">이 cmdlet이 얻을 방화벽의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2185d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2185d-137">-ResourceGroupName</span></span>
<span data-ttu-id="2185d-138">방화벽이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2185d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2185d-139">CommonParameters</span></span>
<span data-ttu-id="2185d-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2185d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2185d-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2185d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2185d-142">입력</span><span class="sxs-lookup"><span data-stu-id="2185d-142">INPUTS</span></span>

### <span data-ttu-id="2185d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2185d-143">System.String</span></span>

## <span data-ttu-id="2185d-144">출력</span><span class="sxs-lookup"><span data-stu-id="2185d-144">OUTPUTS</span></span>

### <span data-ttu-id="2185d-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2185d-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="2185d-146">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="2185d-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2185d-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2185d-147">NOTES</span></span>

## <span data-ttu-id="2185d-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2185d-148">RELATED LINKS</span></span>

[<span data-ttu-id="2185d-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2185d-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="2185d-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2185d-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="2185d-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2185d-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
