---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: c5de4de61a1a0d2aeb14d8a360500b928a28fdcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011904"
---
# <span data-ttu-id="3bce1-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3bce1-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="3bce1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bce1-102">SYNOPSIS</span></span>
<span data-ttu-id="3bce1-103">가상 허브에서 Virtual Network 연결을 얻거나 가상 허브의 모든 가상 네트워크 연결을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="3bce1-104">구문</span><span class="sxs-lookup"><span data-stu-id="3bce1-104">SYNTAX</span></span>

### <span data-ttu-id="3bce1-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="3bce1-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bce1-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="3bce1-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bce1-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="3bce1-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bce1-108">설명</span><span class="sxs-lookup"><span data-stu-id="3bce1-108">DESCRIPTION</span></span>
<span data-ttu-id="3bce1-109">가상 허브에서 Virtual Network 연결을 얻거나 가상 허브의 모든 가상 네트워크 연결을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="3bce1-110">예제</span><span class="sxs-lookup"><span data-stu-id="3bce1-110">EXAMPLES</span></span>

### <span data-ttu-id="3bce1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3bce1-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

<span data-ttu-id="3bce1-112">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 해당 리소스 그룹에 미국 중부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="3bce1-113">이후 가상 네트워크 연결이 만들어지며 가상 네트워크를 Virtual Hub에 피어링합니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="3bce1-114">허브 가상 네트워크 연결을 만든 후 해당 리소스 그룹 이름, 허브 이름 및 연결 이름을 사용하여 허브 가상 네트워크 연결을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="3bce1-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="3bce1-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

<span data-ttu-id="3bce1-116">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 해당 리소스 그룹에 미국 중부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="3bce1-117">이후 가상 네트워크 연결이 만들어지며 가상 네트워크를 Virtual Hub에 피어링합니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="3bce1-118">허브 가상 네트워크 연결을 만든 후 리소스 그룹 이름 및 허브 이름을 사용하여 모든 허브 가상 네트워크 연결을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="3bce1-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="3bce1-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

<span data-ttu-id="3bce1-120">이 cmdlet은 리소스 그룹 이름 및 허브 이름을 사용하여 "테스트"로 시작하는 모든 허브 가상 네트워크 연결을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="3bce1-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3bce1-121">PARAMETERS</span></span>

### <span data-ttu-id="3bce1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bce1-122">-DefaultProfile</span></span>
<span data-ttu-id="3bce1-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bce1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3bce1-124">-Name</span></span>
<span data-ttu-id="3bce1-125">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="3bce1-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3bce1-126">-ParentObject</span></span>
<span data-ttu-id="3bce1-127">상위 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-127">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bce1-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3bce1-128">-ParentResourceId</span></span>
<span data-ttu-id="3bce1-129">부모 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-129">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bce1-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="3bce1-130">-ParentResourceName</span></span>
<span data-ttu-id="3bce1-131">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bce1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bce1-132">-ResourceGroupName</span></span>
<span data-ttu-id="3bce1-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bce1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bce1-134">CommonParameters</span></span>
<span data-ttu-id="3bce1-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3bce1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bce1-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bce1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bce1-137">입력</span><span class="sxs-lookup"><span data-stu-id="3bce1-137">INPUTS</span></span>

### <span data-ttu-id="3bce1-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3bce1-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="3bce1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3bce1-139">System.String</span></span>

## <span data-ttu-id="3bce1-140">출력</span><span class="sxs-lookup"><span data-stu-id="3bce1-140">OUTPUTS</span></span>

### <span data-ttu-id="3bce1-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="3bce1-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="3bce1-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3bce1-142">NOTES</span></span>

## <span data-ttu-id="3bce1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3bce1-143">RELATED LINKS</span></span>

[<span data-ttu-id="3bce1-144">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3bce1-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="3bce1-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3bce1-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
