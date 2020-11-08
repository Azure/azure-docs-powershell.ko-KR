---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 71fff2d475c5cf3045be8aa4c628776b0dd42dc7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214149"
---
# <span data-ttu-id="bf6fa-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bf6fa-101">Get-AzFirewall</span></span>

## <span data-ttu-id="bf6fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="bf6fa-103">Azure 방화벽을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="bf6fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf6fa-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf6fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bf6fa-105">DESCRIPTION</span></span>
<span data-ttu-id="bf6fa-106">**AzFirewall** cmdlet은 리소스 그룹에 하나 이상의 방화벽을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="bf6fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bf6fa-107">EXAMPLES</span></span>

### <span data-ttu-id="bf6fa-108">1: 리소스 그룹의 모든 방화벽 검색</span><span class="sxs-lookup"><span data-stu-id="bf6fa-108">1:  Retrieve all Firewalls in a resource group</span></span>
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

<span data-ttu-id="bf6fa-109">이 예제에서는 "rgName" 리소스 그룹의 모든 방화벽을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="bf6fa-110">2: 이름으로 방화벽 검색</span><span class="sxs-lookup"><span data-stu-id="bf6fa-110">2:  Retrieve a Firewall by name</span></span>
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

<span data-ttu-id="bf6fa-111">이 예제에서는 "azFw" 이라고 하는 "rgName" 리소스 그룹의 방화벽을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="bf6fa-112">3: 필터링을 사용 하 여 모든 방화벽 검색</span><span class="sxs-lookup"><span data-stu-id="bf6fa-112">3:  Retrieve all Firewalls with filtering</span></span>
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

<span data-ttu-id="bf6fa-113">이 예제에서는 "azFw"로 시작 하는 모든 방화벽을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="bf6fa-114">4: 방화벽을 검색 한 다음 응용 프로그램 규칙 컬렉션을 방화벽에 추가</span><span class="sxs-lookup"><span data-stu-id="bf6fa-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="bf6fa-115">이 예제에서는 방화벽을 검색 한 다음 메서드 AddApplicationRuleCollection를 호출 하 여 방화벽에 응용 프로그램 규칙 컬렉션을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="bf6fa-116">5: 방화벽을 검색 한 다음 네트워크 규칙 컬렉션을 방화벽에 추가</span><span class="sxs-lookup"><span data-stu-id="bf6fa-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "UDP" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="bf6fa-117">이 예제에서는 방화벽을 검색 한 다음 메서드 AddNetworkRuleCollection를 호출 하 여 네트워크 규칙 컬렉션을 방화벽에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="bf6fa-118">6: 방화벽을 검색 한 다음 방화벽에서 이름으로 응용 프로그램 규칙 컬렉션 검색</span><span class="sxs-lookup"><span data-stu-id="bf6fa-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="bf6fa-119">이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 가져옵니다. 방화벽 개체의 GetApplicationRuleCollectionByName 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="bf6fa-120">메서드 GetApplicationRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="bf6fa-121">7: 방화벽을 검색 한 다음 방화벽에서 이름별로 네트워크 규칙 컬렉션 검색</span><span class="sxs-lookup"><span data-stu-id="bf6fa-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="bf6fa-122">이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 가져옵니다. 방화벽 개체의 GetNetworkRuleCollectionByName 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="bf6fa-123">메서드 GetNetworkRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="bf6fa-124">8: 방화벽을 검색 한 다음 방화벽에서 이름으로 응용 프로그램 규칙 컬렉션 제거</span><span class="sxs-lookup"><span data-stu-id="bf6fa-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="bf6fa-125">이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 제거 하 고 방화벽 개체의 RemoveApplicationRuleCollectionByName 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="bf6fa-126">메서드 RemoveApplicationRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="bf6fa-127">9: 방화벽을 검색 한 다음 방화벽에서 이름으로 네트워크 규칙 컬렉션 제거</span><span class="sxs-lookup"><span data-stu-id="bf6fa-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="bf6fa-128">이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 제거 하 고 방화벽 개체의 RemoveNetworkRuleCollectionByName 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="bf6fa-129">메서드 RemoveNetworkRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="bf6fa-130">10: 방화벽을 검색 한 다음 방화벽을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="bf6fa-131">이 예제에서는 방화벽을 검색 하 고 방화벽에 할당을 호출 하 여 방화벽과 연결 된 구성 (응용 프로그램 및 네트워크 규칙 컬렉션)을 사용 하 여 방화벽 서비스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="bf6fa-132">변수</span><span class="sxs-lookup"><span data-stu-id="bf6fa-132">PARAMETERS</span></span>

### <span data-ttu-id="bf6fa-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf6fa-133">-DefaultProfile</span></span>
<span data-ttu-id="bf6fa-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf6fa-135">-이름</span><span class="sxs-lookup"><span data-stu-id="bf6fa-135">-Name</span></span>
<span data-ttu-id="bf6fa-136">이 cmdlet이 가져오는 방화벽의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bf6fa-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf6fa-137">-ResourceGroupName</span></span>
<span data-ttu-id="bf6fa-138">방화벽이 속해 있는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

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

### <span data-ttu-id="bf6fa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf6fa-139">CommonParameters</span></span>
<span data-ttu-id="bf6fa-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf6fa-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf6fa-142">입력</span><span class="sxs-lookup"><span data-stu-id="bf6fa-142">INPUTS</span></span>

### <span data-ttu-id="bf6fa-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf6fa-143">System.String</span></span>

## <span data-ttu-id="bf6fa-144">출력</span><span class="sxs-lookup"><span data-stu-id="bf6fa-144">OUTPUTS</span></span>

### <span data-ttu-id="bf6fa-145">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="bf6fa-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="bf6fa-146">System.webserver. t e 1 [[Microsoft Azure.. 모델] PSAzureFirewall, Microsoft Azure를. PowerShell. e 1. t i t = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bf6fa-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bf6fa-147">상속자</span><span class="sxs-lookup"><span data-stu-id="bf6fa-147">NOTES</span></span>

## <span data-ttu-id="bf6fa-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf6fa-148">RELATED LINKS</span></span>

[<span data-ttu-id="bf6fa-149">새로운 AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bf6fa-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="bf6fa-150">제거-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bf6fa-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="bf6fa-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bf6fa-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
