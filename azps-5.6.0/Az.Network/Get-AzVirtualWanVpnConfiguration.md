---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
ms.openlocfilehash: e5ada12a6fd55cc882ba5b9ba33c817f7eb4daab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972688"
---
# <span data-ttu-id="45360-101">Get-AzVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="45360-101">Get-AzVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="45360-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45360-102">SYNOPSIS</span></span>
<span data-ttu-id="45360-103">VpnConnections를 통해 이 WAN에 연결된 VpnSites의 하위 집합에 대한 VPN 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="45360-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="45360-104">고객이 지정한 저장소 Blob에 생성된 Vpn 구성을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="45360-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="45360-105">구문</span><span class="sxs-lookup"><span data-stu-id="45360-105">SYNTAX</span></span>

### <span data-ttu-id="45360-106">ByVirtualWanNameByVpnSiteObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="45360-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45360-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="45360-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45360-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="45360-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45360-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="45360-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45360-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="45360-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45360-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="45360-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45360-112">설명</span><span class="sxs-lookup"><span data-stu-id="45360-112">DESCRIPTION</span></span>
<span data-ttu-id="45360-113">VpnConnections를 통해 이 WAN에 연결된 VpnSites의 하위 집합에 대한 VPN 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="45360-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="45360-114">고객이 지정한 저장소 Blob에 생성된 Vpn 구성을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="45360-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="45360-115">예제</span><span class="sxs-lookup"><span data-stu-id="45360-115">EXAMPLES</span></span>

### <span data-ttu-id="45360-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="45360-116">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="45360-117">위의 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub 및 Azure의 "testRG" 리소스 그룹에서 미국 서부에 VpnSite를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="45360-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="45360-118">2개 확장 단위가 있는 Virtual Hub에서 VPN 게이트웨이가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="45360-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="45360-119">게이트웨이가 만들어지면 이 게이트웨이는 New-AzVpnConnection 사용하여 VpnSite에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="45360-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="45360-120">그런 다음 이 명령줄을 사용하여 구성을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="45360-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="45360-121">명령렛이 성공하면 다운로드 구성이 SignedSasUrl로 표시된 Blob에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="45360-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="45360-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="45360-122">PARAMETERS</span></span>

### <span data-ttu-id="45360-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45360-123">-DefaultProfile</span></span>
<span data-ttu-id="45360-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45360-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45360-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45360-125">-InputObject</span></span>
<span data-ttu-id="45360-126">수정할 VPN 사이트 개체</span><span class="sxs-lookup"><span data-stu-id="45360-126">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteObject, ByVirtualWanObjectByVpnSiteResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45360-127">-Name</span><span class="sxs-lookup"><span data-stu-id="45360-127">-Name</span></span>
<span data-ttu-id="45360-128">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="45360-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45360-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45360-129">-ResourceGroupName</span></span>
<span data-ttu-id="45360-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="45360-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45360-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45360-131">-ResourceId</span></span>
<span data-ttu-id="45360-132">가상 wan에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="45360-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45360-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="45360-133">-StorageSasUrl</span></span>
<span data-ttu-id="45360-134">구성이 생성될 저장소 위치에 대한 SAS URL입니다.</span><span class="sxs-lookup"><span data-stu-id="45360-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="45360-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="45360-135">-VpnSite</span></span>
<span data-ttu-id="45360-136">구성을 생성하는 VpnSite 리소스 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="45360-136">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite[]
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanObjectByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45360-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="45360-137">-VpnSiteId</span></span>
<span data-ttu-id="45360-138">구성을 생성하는 VpnSite 리소스 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="45360-138">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVirtualWanNameByVpnSiteResourceId, ByVirtualWanObjectByVpnSiteResourceId, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45360-139">-확인</span><span class="sxs-lookup"><span data-stu-id="45360-139">-Confirm</span></span>
<span data-ttu-id="45360-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="45360-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45360-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45360-141">-WhatIf</span></span>
<span data-ttu-id="45360-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="45360-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45360-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="45360-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45360-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45360-144">CommonParameters</span></span>
<span data-ttu-id="45360-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="45360-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45360-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45360-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45360-147">입력</span><span class="sxs-lookup"><span data-stu-id="45360-147">INPUTS</span></span>

### <span data-ttu-id="45360-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="45360-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="45360-149">System.String</span><span class="sxs-lookup"><span data-stu-id="45360-149">System.String</span></span>

## <span data-ttu-id="45360-150">출력</span><span class="sxs-lookup"><span data-stu-id="45360-150">OUTPUTS</span></span>

### <span data-ttu-id="45360-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="45360-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="45360-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="45360-152">NOTES</span></span>

## <span data-ttu-id="45360-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45360-153">RELATED LINKS</span></span>
