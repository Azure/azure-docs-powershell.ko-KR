---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: f4087782e247e574cd49634e148b6852e9fb8dc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493198"
---
# <span data-ttu-id="6fd34-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6fd34-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="6fd34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fd34-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd34-103">New-AzVirtualHubVnetConnection cmdlet은 Virtual Network를 Azure Virtual Hub에 피어링하는 HubVirtualNetworkConnection 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="6fd34-104">구문</span><span class="sxs-lookup"><span data-stu-id="6fd34-104">SYNTAX</span></span>

### <span data-ttu-id="6fd34-105">ByVirtualHubNameByRemoteVirtualNetworkObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="6fd34-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd34-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd34-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd34-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="6fd34-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd34-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd34-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fd34-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="6fd34-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd34-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd34-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fd34-111">설명</span><span class="sxs-lookup"><span data-stu-id="6fd34-111">DESCRIPTION</span></span>
<span data-ttu-id="6fd34-112">New-AzVirtualHubVnetConnection cmdlet은 Virtual Network를 Azure Virtual Hub에 피어링하는 HubVirtualNetworkConnection 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="6fd34-113">예제</span><span class="sxs-lookup"><span data-stu-id="6fd34-113">EXAMPLES</span></span>

### <span data-ttu-id="6fd34-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="6fd34-114">Example 1</span></span>

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

<span data-ttu-id="6fd34-115">위의 리소스 그룹인 Virtual WAN, Virtual Network, Azure의 해당 리소스 그룹에 미국 중부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="6fd34-116">가상 네트워크 연결을 만든 후 Virtual Network를 가상 허브에 피어링합니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="6fd34-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="6fd34-117">Example 2</span></span>

<span data-ttu-id="6fd34-118">New-AzVirtualHubVnetConnection cmdlet은 Virtual Network를 Azure Virtual Hub에 피어링하는 HubVirtualNetworkConnection 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="6fd34-119">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="6fd34-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="6fd34-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="6fd34-120">Example 3</span></span>
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
<span data-ttu-id="6fd34-121">위의 설명은 새 라우팅 구성을 만들고 다음 홉을 지정된 IP 주소로 사용하여 라우팅 구성에 정적 경로를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="6fd34-122">그런 다음 이 라우팅 구성을 New-AzVirtualHubVnetConnection -RoutingConfiguration 매개 변수로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="6fd34-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fd34-123">PARAMETERS</span></span>

### <span data-ttu-id="6fd34-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fd34-124">-AsJob</span></span>
<span data-ttu-id="6fd34-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6fd34-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fd34-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd34-126">-DefaultProfile</span></span>
<span data-ttu-id="6fd34-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd34-128">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6fd34-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="6fd34-129">이 연결에 대해 인터넷 보안 사용</span><span class="sxs-lookup"><span data-stu-id="6fd34-129">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="6fd34-130">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="6fd34-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="6fd34-131">이 연결에 대해 인터넷 보안 사용</span><span class="sxs-lookup"><span data-stu-id="6fd34-131">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="6fd34-132">-Name</span><span class="sxs-lookup"><span data-stu-id="6fd34-132">-Name</span></span>
<span data-ttu-id="6fd34-133">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-133">The resource name.</span></span>

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

### <span data-ttu-id="6fd34-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6fd34-134">-ParentObject</span></span>
<span data-ttu-id="6fd34-135">부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-135">The parent resource.</span></span>

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

### <span data-ttu-id="6fd34-136">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd34-136">-ParentResourceId</span></span>
<span data-ttu-id="6fd34-137">부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-137">The parent resource.</span></span>

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

### <span data-ttu-id="6fd34-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6fd34-138">-ParentResourceName</span></span>
<span data-ttu-id="6fd34-139">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-139">The resource group name.</span></span>

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

### <span data-ttu-id="6fd34-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6fd34-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="6fd34-141">이 허브 가상 네트워크 연결이 연결된 원격 가상 네트워크입니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="6fd34-142">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6fd34-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="6fd34-143">이 허브 가상 네트워크 연결이 연결된 원격 가상 네트워크입니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="6fd34-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd34-144">-ResourceGroupName</span></span>
<span data-ttu-id="6fd34-145">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-145">The resource group name.</span></span>

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

### <span data-ttu-id="6fd34-146">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fd34-146">-RoutingConfiguration</span></span>
<span data-ttu-id="6fd34-147">이 연결에 대한 라우팅 구성</span><span class="sxs-lookup"><span data-stu-id="6fd34-147">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="6fd34-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fd34-148">-Confirm</span></span>
<span data-ttu-id="6fd34-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd34-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd34-150">-WhatIf</span></span>
<span data-ttu-id="6fd34-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6fd34-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fd34-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd34-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd34-153">CommonParameters</span></span>
<span data-ttu-id="6fd34-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6fd34-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd34-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6fd34-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd34-156">입력</span><span class="sxs-lookup"><span data-stu-id="6fd34-156">INPUTS</span></span>

### <span data-ttu-id="6fd34-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6fd34-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="6fd34-158">System.String</span><span class="sxs-lookup"><span data-stu-id="6fd34-158">System.String</span></span>

## <span data-ttu-id="6fd34-159">출력</span><span class="sxs-lookup"><span data-stu-id="6fd34-159">OUTPUTS</span></span>

### <span data-ttu-id="6fd34-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="6fd34-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="6fd34-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6fd34-161">NOTES</span></span>

## <span data-ttu-id="6fd34-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fd34-162">RELATED LINKS</span></span>

[<span data-ttu-id="6fd34-163">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6fd34-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="6fd34-164">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6fd34-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="6fd34-165">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fd34-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
