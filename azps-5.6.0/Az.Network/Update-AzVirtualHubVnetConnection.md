---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 1454e3ba3fc3a7e229e064a32146ebddddc19392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951584"
---
# <span data-ttu-id="d370a-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d370a-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="d370a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d370a-102">SYNOPSIS</span></span>
<span data-ttu-id="d370a-103">기존 HubVirtualNetworkConnection을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="d370a-104">구문</span><span class="sxs-lookup"><span data-stu-id="d370a-104">SYNTAX</span></span>

### <span data-ttu-id="d370a-105">ByHubVirtualNetworkConnectionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d370a-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d370a-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="d370a-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d370a-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="d370a-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d370a-108">설명</span><span class="sxs-lookup"><span data-stu-id="d370a-108">DESCRIPTION</span></span>
<span data-ttu-id="d370a-109">기존 HubVirtualNetworkConnection을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="d370a-110">예제</span><span class="sxs-lookup"><span data-stu-id="d370a-110">EXAMPLES</span></span>

### <span data-ttu-id="d370a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d370a-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
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

<span data-ttu-id="d370a-112">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 해당 리소스 그룹에 미국 중부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="d370a-113">가상 네트워크 연결도 만들어지며 가상 네트워크는 Virtual Hub에 피어링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="d370a-114">그런 다음 이 가상 네트워크 연결이 인터넷 보안을 사용하도록 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="d370a-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d370a-115">PARAMETERS</span></span>

### <span data-ttu-id="d370a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d370a-116">-AsJob</span></span>
<span data-ttu-id="d370a-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d370a-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d370a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d370a-118">-DefaultProfile</span></span>
<span data-ttu-id="d370a-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d370a-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d370a-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="d370a-121">이 연결에 대해 인터넷 보안을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-121">Enable internet security for this connection.</span></span>

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

### <span data-ttu-id="d370a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d370a-122">-InputObject</span></span>
<span data-ttu-id="d370a-123">수정할 hubvirtualnetworkconnection 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d370a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d370a-124">-Name</span></span>
<span data-ttu-id="d370a-125">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d370a-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d370a-126">-ParentResourceName</span></span>
<span data-ttu-id="d370a-127">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d370a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d370a-128">-ResourceGroupName</span></span>
<span data-ttu-id="d370a-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d370a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d370a-130">-ResourceId</span></span>
<span data-ttu-id="d370a-131">수정할 hubvirtualnetworkconnection 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d370a-132">-라우팅Configuration</span><span class="sxs-lookup"><span data-stu-id="d370a-132">-RoutingConfiguration</span></span>
<span data-ttu-id="d370a-133">이 연결에 대한 라우팅 구성</span><span class="sxs-lookup"><span data-stu-id="d370a-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="d370a-134">-확인</span><span class="sxs-lookup"><span data-stu-id="d370a-134">-Confirm</span></span>
<span data-ttu-id="d370a-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d370a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d370a-136">-WhatIf</span></span>
<span data-ttu-id="d370a-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d370a-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d370a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d370a-139">CommonParameters</span></span>
<span data-ttu-id="d370a-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d370a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d370a-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d370a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d370a-142">입력</span><span class="sxs-lookup"><span data-stu-id="d370a-142">INPUTS</span></span>

### <span data-ttu-id="d370a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d370a-143">System.String</span></span>

### <span data-ttu-id="d370a-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="d370a-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="d370a-145">출력</span><span class="sxs-lookup"><span data-stu-id="d370a-145">OUTPUTS</span></span>

### <span data-ttu-id="d370a-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="d370a-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="d370a-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d370a-147">NOTES</span></span>

## <span data-ttu-id="d370a-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d370a-148">RELATED LINKS</span></span>

[<span data-ttu-id="d370a-149">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d370a-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
