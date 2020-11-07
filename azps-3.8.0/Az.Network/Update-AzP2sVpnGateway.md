---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 39fb3223b1a80b831874bbd833d6d0c97aace53f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877442"
---
# <span data-ttu-id="cd53e-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cd53e-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="cd53e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd53e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd53e-103">사이트 연결에 대 한 VirtualHub의 기존 P2SVpnGateway를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="cd53e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd53e-104">SYNTAX</span></span>

### <span data-ttu-id="cd53e-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (기본값)</span><span class="sxs-lookup"><span data-stu-id="cd53e-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd53e-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="cd53e-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd53e-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="cd53e-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd53e-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="cd53e-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd53e-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="cd53e-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd53e-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="cd53e-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd53e-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="cd53e-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd53e-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="cd53e-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd53e-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="cd53e-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd53e-114">설명은</span><span class="sxs-lookup"><span data-stu-id="cd53e-114">DESCRIPTION</span></span>
<span data-ttu-id="cd53e-115">**AzP2sVpnGateway** cmdlet을 사용 하 여 새 VpnClientAddressPool 또는 새 VpnServerConfiguration 또는 VpnGatewayScaleUnit 변경으로 virtualhub의 기존 P2SVpnGateway을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="cd53e-116">예제의</span><span class="sxs-lookup"><span data-stu-id="cd53e-116">EXAMPLES</span></span>

### <span data-ttu-id="cd53e-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd53e-117">Example 1</span></span>
```powershell
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1 
PS C:\> $vpnClientAddressSpaces[0] = "101.10.0.0/16"
PS C:\> Update-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VpnClientAddressPool $vpnClientAddressSpaces                                    

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/NilamdWestUsVirtualH
                                 ub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/NilamdWe
                                 stUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "101.10.0.0/16"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"d7debc2f-ccbb-4f00-bddc-42c99b52fda3\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="cd53e-118">**AzP2sVpnGateway** cmdlet을 사용 하면 새 VpnClientAddressPool를 사용 하 여 virtualhub의 기존 P2SVpnGateway를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="cd53e-119">사이트 클라이언트가이 P2SVpnGateway에 연결 되 면이 VpnClientAddressPool의 ip 주소 중 하나가 해당 클라이언트에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

## <span data-ttu-id="cd53e-120">변수</span><span class="sxs-lookup"><span data-stu-id="cd53e-120">PARAMETERS</span></span>

### <span data-ttu-id="cd53e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd53e-121">-AsJob</span></span>
<span data-ttu-id="cd53e-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cd53e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd53e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd53e-123">-DefaultProfile</span></span>
<span data-ttu-id="cd53e-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd53e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd53e-125">-InputObject</span></span>
<span data-ttu-id="cd53e-126">수정할 p2s vpn 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="cd53e-126">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd53e-127">-이름</span><span class="sxs-lookup"><span data-stu-id="cd53e-127">-Name</span></span>
<span data-ttu-id="cd53e-128">P2S vpn 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-128">The P2S vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases: ResourceName, P2SVpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd53e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd53e-129">-ResourceGroupName</span></span>
<span data-ttu-id="cd53e-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd53e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd53e-131">-ResourceId</span></span>
<span data-ttu-id="cd53e-132">수정할 P2SVpnGateway의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-132">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd53e-133">태그</span><span class="sxs-lookup"><span data-stu-id="cd53e-133">-Tag</span></span>
<span data-ttu-id="cd53e-134">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cd53e-135">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="cd53e-135">-VpnClientAddressPool</span></span>
<span data-ttu-id="cd53e-136">P2S VpnClient AddressPool (이 P2SVpnGateway P2SConnectionConfiguration).</span><span class="sxs-lookup"><span data-stu-id="cd53e-136">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd53e-137">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="cd53e-137">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="cd53e-138">이 P2SVpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-138">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd53e-139">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd53e-139">-VpnServerConfiguration</span></span>
<span data-ttu-id="cd53e-140">이 P2SVpnGateway에 첨부할 VpnServerConfiguration입니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-140">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd53e-141">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="cd53e-141">-VpnServerConfigurationId</span></span>
<span data-ttu-id="cd53e-142">이 P2SVpnGateway이 첨부 될 Vpn 서버 구성 개체의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-142">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationResourceId, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd53e-143">-확인</span><span class="sxs-lookup"><span data-stu-id="cd53e-143">-Confirm</span></span>
<span data-ttu-id="cd53e-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd53e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd53e-145">-WhatIf</span></span>
<span data-ttu-id="cd53e-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd53e-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd53e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd53e-148">CommonParameters</span></span>
<span data-ttu-id="cd53e-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd53e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd53e-150">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd53e-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd53e-151">입력</span><span class="sxs-lookup"><span data-stu-id="cd53e-151">INPUTS</span></span>

### <span data-ttu-id="cd53e-152">PSP2SVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cd53e-152">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="cd53e-153">PSVpnServerConfiguration. \*. \* \*.</span><span class="sxs-lookup"><span data-stu-id="cd53e-153">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="cd53e-154">출력</span><span class="sxs-lookup"><span data-stu-id="cd53e-154">OUTPUTS</span></span>

### <span data-ttu-id="cd53e-155">PSP2SVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cd53e-155">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="cd53e-156">상속자</span><span class="sxs-lookup"><span data-stu-id="cd53e-156">NOTES</span></span>

## <span data-ttu-id="cd53e-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd53e-157">RELATED LINKS</span></span>
