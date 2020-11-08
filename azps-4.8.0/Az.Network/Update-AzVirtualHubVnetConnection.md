---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 0c07686b59f89bfee656701e14a7c938f49eeb86
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214305"
---
# <span data-ttu-id="b376b-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b376b-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="b376b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b376b-102">SYNOPSIS</span></span>
<span data-ttu-id="b376b-103">기존 HubVirtualNetworkConnection를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="b376b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b376b-104">SYNTAX</span></span>

### <span data-ttu-id="b376b-105">ByHubVirtualNetworkConnectionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b376b-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b376b-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b376b-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b376b-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="b376b-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b376b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b376b-108">DESCRIPTION</span></span>
<span data-ttu-id="b376b-109">기존 HubVirtualNetworkConnection를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="b376b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b376b-110">EXAMPLES</span></span>

### <span data-ttu-id="b376b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b376b-111">Example 1</span></span>
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

<span data-ttu-id="b376b-112">Azure에서 해당 리소스 그룹의 중앙 US에 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="b376b-113">가상 네트워크 연결만 생성 됩니다 가상 허브에 대 한 가상 네트워크 연결도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="b376b-114">그런 다음이 가상 네트워크 연결이 인터넷 보안을 사용 하도록 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="b376b-115">변수</span><span class="sxs-lookup"><span data-stu-id="b376b-115">PARAMETERS</span></span>

### <span data-ttu-id="b376b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b376b-116">-AsJob</span></span>
<span data-ttu-id="b376b-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b376b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b376b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b376b-118">-DefaultProfile</span></span>
<span data-ttu-id="b376b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b376b-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="b376b-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="b376b-121">이 연결에 인터넷 보안을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-121">Enable internet security for this connection.</span></span>

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

### <span data-ttu-id="b376b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b376b-122">-InputObject</span></span>
<span data-ttu-id="b376b-123">수정할 hubvirtualnetworkconnection 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-123">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="b376b-124">-이름</span><span class="sxs-lookup"><span data-stu-id="b376b-124">-Name</span></span>
<span data-ttu-id="b376b-125">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-125">The resource name.</span></span>

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

### <span data-ttu-id="b376b-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b376b-126">-ParentResourceName</span></span>
<span data-ttu-id="b376b-127">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-127">The parent resource name.</span></span>

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

### <span data-ttu-id="b376b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b376b-128">-ResourceGroupName</span></span>
<span data-ttu-id="b376b-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-129">The resource group name.</span></span>

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

### <span data-ttu-id="b376b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b376b-130">-ResourceId</span></span>
<span data-ttu-id="b376b-131">수정할 hubvirtualnetworkconnection 리소스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="b376b-132">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b376b-132">-RoutingConfiguration</span></span>
<span data-ttu-id="b376b-133">이 연결에 대 한 라우팅 구성</span><span class="sxs-lookup"><span data-stu-id="b376b-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="b376b-134">-확인</span><span class="sxs-lookup"><span data-stu-id="b376b-134">-Confirm</span></span>
<span data-ttu-id="b376b-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b376b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b376b-136">-WhatIf</span></span>
<span data-ttu-id="b376b-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b376b-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b376b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b376b-139">CommonParameters</span></span>
<span data-ttu-id="b376b-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b376b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b376b-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b376b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b376b-142">입력</span><span class="sxs-lookup"><span data-stu-id="b376b-142">INPUTS</span></span>

### <span data-ttu-id="b376b-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b376b-143">System.String</span></span>

### <span data-ttu-id="b376b-144">PSHubVirtualNetworkConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b376b-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="b376b-145">출력</span><span class="sxs-lookup"><span data-stu-id="b376b-145">OUTPUTS</span></span>

### <span data-ttu-id="b376b-146">PSHubVirtualNetworkConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b376b-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="b376b-147">상속자</span><span class="sxs-lookup"><span data-stu-id="b376b-147">NOTES</span></span>

## <span data-ttu-id="b376b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b376b-148">RELATED LINKS</span></span>

[<span data-ttu-id="b376b-149">새로운 AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b376b-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
