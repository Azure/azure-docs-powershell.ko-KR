---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 42592e1d72303c98a27890e2ac7721d95c37f928
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967792"
---
# <span data-ttu-id="f4b8c-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f4b8c-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="f4b8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b8c-103">New-AzVirtualHubVnetConnection cmdlet은 Azure Virtual Hub에 가상 네트워크를 피어링하는 HubVirtualNetworkConnection 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="f4b8c-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4b8c-104">SYNTAX</span></span>

### <span data-ttu-id="f4b8c-105">ByVirtualHubNameByRemoteVirtualNetworkObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="f4b8c-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b8c-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f4b8c-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b8c-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="f4b8c-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b8c-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f4b8c-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4b8c-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="f4b8c-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b8c-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f4b8c-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4b8c-111">설명</span><span class="sxs-lookup"><span data-stu-id="f4b8c-111">DESCRIPTION</span></span>
<span data-ttu-id="f4b8c-112">New-AzVirtualHubVnetConnection cmdlet은 Azure Virtual Hub에 가상 네트워크를 피어링하는 HubVirtualNetworkConnection 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="f4b8c-113">예제</span><span class="sxs-lookup"><span data-stu-id="f4b8c-113">EXAMPLES</span></span>

### <span data-ttu-id="f4b8c-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="f4b8c-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="f4b8c-115">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 해당 리소스 그룹에 미국 중부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f4b8c-116">이후 가상 네트워크 연결이 만들어지며 가상 네트워크를 Virtual Hub에 피어링합니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="f4b8c-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="f4b8c-117">Example 2</span></span>

<span data-ttu-id="f4b8c-118">New-AzVirtualHubVnetConnection cmdlet은 Azure Virtual Hub에 가상 네트워크를 피어링하는 HubVirtualNetworkConnection 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="f4b8c-119">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="f4b8c-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="f4b8c-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="f4b8c-120">Example 3</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName $rgName -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> $routingconfig = New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork -RoutingConfiguration $routingconfig
```
<span data-ttu-id="f4b8c-121">위의 경우 새 라우팅 구성을 만들고 지정된 IP 주소로 다음 홉을 사용하여 라우팅 구성에서 정적 경로를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="f4b8c-122">그런 다음 이 라우팅 구성을 매개 변수로 New-AzVirtualHubVnetConnection 명령으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="f4b8c-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f4b8c-123">PARAMETERS</span></span>

### <span data-ttu-id="f4b8c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4b8c-124">-AsJob</span></span>
<span data-ttu-id="f4b8c-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f4b8c-125">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b8c-126">-DefaultProfile</span></span>
<span data-ttu-id="f4b8c-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4b8c-128">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f4b8c-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="f4b8c-129">이 연결에 대한 인터넷 보안 사용</span><span class="sxs-lookup"><span data-stu-id="f4b8c-129">Enable internet security for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-130">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="f4b8c-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="f4b8c-131">이 연결에 대한 인터넷 보안 사용</span><span class="sxs-lookup"><span data-stu-id="f4b8c-131">Enable internet security for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-132">-Name</span><span class="sxs-lookup"><span data-stu-id="f4b8c-132">-Name</span></span>
<span data-ttu-id="f4b8c-133">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f4b8c-134">-ParentObject</span></span>
<span data-ttu-id="f4b8c-135">상위 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-135">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-136">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f4b8c-136">-ParentResourceId</span></span>
<span data-ttu-id="f4b8c-137">상위 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-137">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f4b8c-138">-ParentResourceName</span></span>
<span data-ttu-id="f4b8c-139">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-139">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4b8c-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="f4b8c-141">이 허브 가상 네트워크 연결이 연결된 원격 가상 네트워크입니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-142">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f4b8c-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="f4b8c-143">이 허브 가상 네트워크 연결이 연결된 원격 가상 네트워크입니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4b8c-144">-ResourceGroupName</span></span>
<span data-ttu-id="f4b8c-145">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-145">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-146">-라우팅Configuration</span><span class="sxs-lookup"><span data-stu-id="f4b8c-146">-RoutingConfiguration</span></span>
<span data-ttu-id="f4b8c-147">이 연결에 대한 라우팅 구성</span><span class="sxs-lookup"><span data-stu-id="f4b8c-147">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-148">-확인</span><span class="sxs-lookup"><span data-stu-id="f4b8c-148">-Confirm</span></span>
<span data-ttu-id="f4b8c-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4b8c-150">-WhatIf</span></span>
<span data-ttu-id="f4b8c-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4b8c-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b8c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b8c-153">CommonParameters</span></span>
<span data-ttu-id="f4b8c-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4b8c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b8c-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4b8c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b8c-156">입력</span><span class="sxs-lookup"><span data-stu-id="f4b8c-156">INPUTS</span></span>

### <span data-ttu-id="f4b8c-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f4b8c-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="f4b8c-158">System.String</span><span class="sxs-lookup"><span data-stu-id="f4b8c-158">System.String</span></span>

## <span data-ttu-id="f4b8c-159">출력</span><span class="sxs-lookup"><span data-stu-id="f4b8c-159">OUTPUTS</span></span>

### <span data-ttu-id="f4b8c-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="f4b8c-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="f4b8c-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4b8c-161">NOTES</span></span>

## <span data-ttu-id="f4b8c-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4b8c-162">RELATED LINKS</span></span>

[<span data-ttu-id="f4b8c-163">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f4b8c-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="f4b8c-164">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f4b8c-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="f4b8c-165">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4b8c-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
