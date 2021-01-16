---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 516cd38257a8742f1bc23b3207b7e3c982d9eb36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357533"
---
# <span data-ttu-id="567f8-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="567f8-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="567f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="567f8-102">SYNOPSIS</span></span>
<span data-ttu-id="567f8-103">지점 및 사이트 연결을 위해 VirtualHub 아래에 새 P2SVpnGateway를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="567f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="567f8-104">SYNTAX</span></span>

### <span data-ttu-id="567f8-105">ByVirtualHubNameByVpnServerConfigurationObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="567f8-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="567f8-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="567f8-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="567f8-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="567f8-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="567f8-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="567f8-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="567f8-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="567f8-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="567f8-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="567f8-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="567f8-111">설명</span><span class="sxs-lookup"><span data-stu-id="567f8-111">DESCRIPTION</span></span>
<span data-ttu-id="567f8-112">**New-AzP2sVpnGateway** cmdlet을 사용하면 지점 및 사이트 클라이언트에서 Azure VirtualWan으로 지점 및 사이트 연결에 대한 VirtualHub 아래에 새 P2SVpnGateway를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-112">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="567f8-113">예제</span><span class="sxs-lookup"><span data-stu-id="567f8-113">EXAMPLES</span></span>

### <span data-ttu-id="567f8-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="567f8-114">Example 1</span></span>
```powershell
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1 -EnableInternetSecurityFlag

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "EnableInternetSecurity": True,
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="567f8-115">**New-AzP2sVpnGateway** cmdlet을 사용하면 지점 및 사이트 연결에 대한 VirtualHub 아래에 새 P2SVpnGateway를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-115">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="567f8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="567f8-116">PARAMETERS</span></span>

### <span data-ttu-id="567f8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="567f8-117">-AsJob</span></span>
<span data-ttu-id="567f8-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="567f8-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="567f8-119">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="567f8-119">-CustomDnsServer</span></span>
<span data-ttu-id="567f8-120">사용자 지정 Dns 서버 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-120">The list of Custom Dns Servers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567f8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567f8-121">-DefaultProfile</span></span>
<span data-ttu-id="567f8-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="567f8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="567f8-123">-Name</span></span>
<span data-ttu-id="567f8-124">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567f8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="567f8-125">-ResourceGroupName</span></span>
<span data-ttu-id="567f8-126">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-126">The resource name.</span></span>

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

### <span data-ttu-id="567f8-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="567f8-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="567f8-128">이 P2SVpnGateway 연결에 대한 인터넷 보안 플래그 사용</span><span class="sxs-lookup"><span data-stu-id="567f8-128">Enable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="567f8-129">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="567f8-129">-RoutingConfiguration</span></span>
<span data-ttu-id="567f8-130">이 연결에 대한 라우팅 구성</span><span class="sxs-lookup"><span data-stu-id="567f8-130">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="567f8-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="567f8-131">-Tag</span></span>
<span data-ttu-id="567f8-132">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567f8-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="567f8-133">-VirtualHub</span></span>
<span data-ttu-id="567f8-134">이 P2SVpnGateway의 VirtualHub를 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-134">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="567f8-135">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="567f8-135">-VirtualHubId</span></span>
<span data-ttu-id="567f8-136">이 P2SVpnGateway VirtualHub의 ID를 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-136">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567f8-137">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="567f8-137">-VirtualHubName</span></span>
<span data-ttu-id="567f8-138">이 P2SVpnGateway VirtualHub의 ID를 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-138">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567f8-139">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="567f8-139">-VpnClientAddressPool</span></span>
<span data-ttu-id="567f8-140">이 P2SVpnGateway P2SConnectionConfiguration에 대한 P2S VpnClient AddressPool입니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-140">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

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

### <span data-ttu-id="567f8-141">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="567f8-141">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="567f8-142">이 P2SVpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-142">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567f8-143">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="567f8-143">-VpnServerConfiguration</span></span>
<span data-ttu-id="567f8-144">이 P2SVpnGateway에 연결될 VpnServerConfiguration입니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-144">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="567f8-145">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="567f8-145">-VpnServerConfigurationId</span></span>
<span data-ttu-id="567f8-146">이 P2SVpnGateway가 연결되는 Vpn 서버 구성 개체의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-146">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567f8-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="567f8-147">-Confirm</span></span>
<span data-ttu-id="567f8-148">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="567f8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="567f8-149">-WhatIf</span></span>
<span data-ttu-id="567f8-150">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="567f8-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="567f8-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="567f8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567f8-152">CommonParameters</span></span>
<span data-ttu-id="567f8-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="567f8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567f8-154">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="567f8-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567f8-155">입력</span><span class="sxs-lookup"><span data-stu-id="567f8-155">INPUTS</span></span>

### <span data-ttu-id="567f8-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="567f8-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="567f8-157">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="567f8-157">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="567f8-158">출력</span><span class="sxs-lookup"><span data-stu-id="567f8-158">OUTPUTS</span></span>

### <span data-ttu-id="567f8-159">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="567f8-159">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="567f8-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="567f8-160">NOTES</span></span>

## <span data-ttu-id="567f8-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="567f8-161">RELATED LINKS</span></span>

[<span data-ttu-id="567f8-162">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="567f8-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
