---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 6d16703b7f0492bb2c37291e135cb1b9c836a572
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041774"
---
# <span data-ttu-id="6b7e9-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6b7e9-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="6b7e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b7e9-102">SYNOPSIS</span></span>
<span data-ttu-id="6b7e9-103">사이트 연결을 위한 VirtualHub 아래에 새 P2SVpnGateway를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="6b7e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b7e9-104">SYNTAX</span></span>

### <span data-ttu-id="6b7e9-105">ByVirtualHubNameByVpnServerConfigurationObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b7e9-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b7e9-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6b7e9-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b7e9-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="6b7e9-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b7e9-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6b7e9-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b7e9-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="6b7e9-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b7e9-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6b7e9-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b7e9-111">설명은</span><span class="sxs-lookup"><span data-stu-id="6b7e9-111">DESCRIPTION</span></span>
<span data-ttu-id="6b7e9-112">**AzP2sVpnGateway** cmdlet을 사용 하면 사이트 클라이언트에서 Azure virtualhub으로의 위치에 대 한 끝점에 대해 virtualhub에서 새 P2SVpnGateway를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-112">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="6b7e9-113">예제의</span><span class="sxs-lookup"><span data-stu-id="6b7e9-113">EXAMPLES</span></span>

### <span data-ttu-id="6b7e9-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b7e9-114">Example 1</span></span>
```powershell
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1

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
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="6b7e9-115">**AzP2sVpnGateway** cmdlet을 사용 하면 사이트 연결에 대 한 virtualhub 아래에 새 P2SVpnGateway를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-115">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="6b7e9-116">변수</span><span class="sxs-lookup"><span data-stu-id="6b7e9-116">PARAMETERS</span></span>

### <span data-ttu-id="6b7e9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b7e9-117">-AsJob</span></span>
<span data-ttu-id="6b7e9-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6b7e9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b7e9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b7e9-119">-DefaultProfile</span></span>
<span data-ttu-id="6b7e9-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b7e9-121">-이름</span><span class="sxs-lookup"><span data-stu-id="6b7e9-121">-Name</span></span>
<span data-ttu-id="6b7e9-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b7e9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b7e9-123">-ResourceGroupName</span></span>
<span data-ttu-id="6b7e9-124">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-124">The resource name.</span></span>

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

### <span data-ttu-id="6b7e9-125">태그</span><span class="sxs-lookup"><span data-stu-id="6b7e9-125">-Tag</span></span>
<span data-ttu-id="6b7e9-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b7e9-127">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="6b7e9-127">-VirtualHub</span></span>
<span data-ttu-id="6b7e9-128">이 P2SVpnGateway 연결 해야 하는 VirtualHub입니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-128">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b7e9-129">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="6b7e9-129">-VirtualHubId</span></span>
<span data-ttu-id="6b7e9-130">이 P2SVpnGateway와 연결 되어야 하는 VirtualHub의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-130">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b7e9-131">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="6b7e9-131">-VirtualHubName</span></span>
<span data-ttu-id="6b7e9-132">이 P2SVpnGateway와 연결 되어야 하는 VirtualHub의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-132">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b7e9-133">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="6b7e9-133">-VpnClientAddressPool</span></span>
<span data-ttu-id="6b7e9-134">P2S VpnClient AddressPool (이 P2SVpnGateway P2SConnectionConfiguration).</span><span class="sxs-lookup"><span data-stu-id="6b7e9-134">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b7e9-135">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="6b7e9-135">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="6b7e9-136">이 P2SVpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-136">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b7e9-137">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b7e9-137">-VpnServerConfiguration</span></span>
<span data-ttu-id="6b7e9-138">이 P2SVpnGateway에 첨부할 VpnServerConfiguration입니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-138">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b7e9-139">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6b7e9-139">-VpnServerConfigurationId</span></span>
<span data-ttu-id="6b7e9-140">이 P2SVpnGateway이 첨부 될 Vpn 서버 구성 개체의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-140">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b7e9-141">-확인</span><span class="sxs-lookup"><span data-stu-id="6b7e9-141">-Confirm</span></span>
<span data-ttu-id="6b7e9-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b7e9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b7e9-143">-WhatIf</span></span>
<span data-ttu-id="6b7e9-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b7e9-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b7e9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b7e9-146">CommonParameters</span></span>
<span data-ttu-id="6b7e9-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b7e9-148">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b7e9-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b7e9-149">입력</span><span class="sxs-lookup"><span data-stu-id="6b7e9-149">INPUTS</span></span>

### <span data-ttu-id="6b7e9-150">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6b7e9-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="6b7e9-151">PSVpnServerConfiguration. \*. \* \*.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-151">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="6b7e9-152">출력</span><span class="sxs-lookup"><span data-stu-id="6b7e9-152">OUTPUTS</span></span>

### <span data-ttu-id="6b7e9-153">PSP2SVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-153">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="6b7e9-154">상속자</span><span class="sxs-lookup"><span data-stu-id="6b7e9-154">NOTES</span></span>

## <span data-ttu-id="6b7e9-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b7e9-155">RELATED LINKS</span></span>
