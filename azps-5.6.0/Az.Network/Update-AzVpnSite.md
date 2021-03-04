---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: bd9b0b2a61edf70dfb4cebf392bb64fa742c0417
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951435"
---
# <span data-ttu-id="cad47-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="cad47-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="cad47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cad47-102">SYNOPSIS</span></span>
<span data-ttu-id="cad47-103">VPN 사이트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-103">Updates a VPN site.</span></span>

## <span data-ttu-id="cad47-104">구문</span><span class="sxs-lookup"><span data-stu-id="cad47-104">SYNTAX</span></span>

### <span data-ttu-id="cad47-105">ByVpnSiteNameNoVirtualWanUpdate(기본값)</span><span class="sxs-lookup"><span data-stu-id="cad47-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad47-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="cad47-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad47-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="cad47-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cad47-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="cad47-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cad47-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="cad47-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad47-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="cad47-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cad47-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="cad47-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cad47-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="cad47-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad47-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="cad47-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad47-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="cad47-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad47-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="cad47-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cad47-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="cad47-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cad47-117">설명</span><span class="sxs-lookup"><span data-stu-id="cad47-117">DESCRIPTION</span></span>
<span data-ttu-id="cad47-118">**Update-AzVpnSite** cmdlet은 VPN 사이트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="cad47-119">예제</span><span class="sxs-lookup"><span data-stu-id="cad47-119">EXAMPLES</span></span>

### <span data-ttu-id="cad47-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="cad47-120">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 2.3.4.5
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="cad47-121">위의 리소스 그룹은 Azure에서 "testRG" 리소스 그룹에서 미국 서부의 Virtual WAN을 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="cad47-122">그런 다음, VpnSite를 만들어 고객 분기를 나타내고 Virtual WAN에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="cad47-123">사이트가 만들어지면 사이트 ipAddress는 Set-AzVpnSite 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="cad47-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cad47-124">PARAMETERS</span></span>

### <span data-ttu-id="cad47-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="cad47-125">-AddressSpace</span></span>
<span data-ttu-id="cad47-126">가상 네트워크의 주소 도두사입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="cad47-127">이 또는 AddressSpaceObject를 사용하지만 둘 다 사용하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-127">Use this or AddressSpaceObject but not both.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cad47-128">-AsJob</span></span>
<span data-ttu-id="cad47-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cad47-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cad47-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="cad47-130">-BgpAsn</span></span>
<span data-ttu-id="cad47-131">이 VpnSite에 대한 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="cad47-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="cad47-133">이 VpnSite에 대한 BGP 피어링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="cad47-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="cad47-135">이 VpnSite에 대한 BGP 피어링 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad47-136">-DefaultProfile</span></span>
<span data-ttu-id="cad47-137">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cad47-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="cad47-138">-DeviceModel</span></span>
<span data-ttu-id="cad47-139">원격 VPN 장치의 디바이스 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-139">The device model of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="cad47-140">-DeviceVendor</span></span>
<span data-ttu-id="cad47-141">원격 VPN 디바이스의 디바이스 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-141">The device vendor of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cad47-142">-InputObject</span></span>
<span data-ttu-id="cad47-143">수정할 VPN 사이트 개체</span><span class="sxs-lookup"><span data-stu-id="cad47-143">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObjectByVirtualWanName, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteObjectNoVirtualWanUpdate
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="cad47-144">-IpAddress</span></span>
<span data-ttu-id="cad47-145">로컬 네트워크 게이트웨이의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-145">IP address of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="cad47-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="cad47-147">원격 VPN 장치의 디바이스 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-147">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-148">-Name</span><span class="sxs-lookup"><span data-stu-id="cad47-148">-Name</span></span>
<span data-ttu-id="cad47-149">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="cad47-150">-O365Policy</span></span>
<span data-ttu-id="cad47-151">이 VpnSite에 대한 Office 365 트래픽 중단 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cad47-152">-ResourceGroupName</span></span>
<span data-ttu-id="cad47-153">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-153">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cad47-154">-ResourceId</span></span>
<span data-ttu-id="cad47-155">VPN 사이트의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-155">The Azure resource ID for the vpn site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceIdByVirtualWanName, ByVpnSiteResourceIdByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanObject, ByVpnSiteResourceIdNoVirtualWanUpdate
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="cad47-156">-Tag</span></span>
<span data-ttu-id="cad47-157">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cad47-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="cad47-158">-VirtualWan</span></span>
<span data-ttu-id="cad47-159">VirtualWan 이 VpnSite에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVpnSiteNameByVirtualWanObject, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteResourceIdByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="cad47-160">-VirtualWanId</span></span>
<span data-ttu-id="cad47-161">ResourceId VirtualWan 이 VpnSite에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="cad47-162">-VirtualWanName</span></span>
<span data-ttu-id="cad47-163">VirtualWan의 이름을 이 VpnSite에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cad47-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="cad47-165">VirtualWan의 리소스 그룹 이름 이 VpnSite에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="cad47-166">-VpnSiteLink</span></span>
<span data-ttu-id="cad47-167">이 VpnSite가 있는 VpnSiteLinks 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad47-168">-확인</span><span class="sxs-lookup"><span data-stu-id="cad47-168">-Confirm</span></span>
<span data-ttu-id="cad47-169">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cad47-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cad47-170">-WhatIf</span></span>
<span data-ttu-id="cad47-171">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cad47-172">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cad47-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad47-173">CommonParameters</span></span>
<span data-ttu-id="cad47-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cad47-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad47-175">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cad47-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad47-176">입력</span><span class="sxs-lookup"><span data-stu-id="cad47-176">INPUTS</span></span>

### <span data-ttu-id="cad47-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="cad47-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="cad47-178">System.String</span><span class="sxs-lookup"><span data-stu-id="cad47-178">System.String</span></span>

## <span data-ttu-id="cad47-179">출력</span><span class="sxs-lookup"><span data-stu-id="cad47-179">OUTPUTS</span></span>

### <span data-ttu-id="cad47-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="cad47-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="cad47-181">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cad47-181">NOTES</span></span>

## <span data-ttu-id="cad47-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cad47-182">RELATED LINKS</span></span>

[<span data-ttu-id="cad47-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="cad47-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="cad47-184">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="cad47-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="cad47-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="cad47-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
