---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193260"
---
# <span data-ttu-id="a782e-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a782e-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="a782e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a782e-102">SYNOPSIS</span></span>
<span data-ttu-id="a782e-103">VPN 사이트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-103">Updates a VPN site.</span></span>

## <span data-ttu-id="a782e-104">구문</span><span class="sxs-lookup"><span data-stu-id="a782e-104">SYNTAX</span></span>

### <span data-ttu-id="a782e-105">ByVpnSiteNameNoVirtualWanUpdate(기본값)</span><span class="sxs-lookup"><span data-stu-id="a782e-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a782e-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="a782e-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a782e-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="a782e-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a782e-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="a782e-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a782e-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="a782e-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a782e-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="a782e-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a782e-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="a782e-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a782e-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="a782e-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a782e-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="a782e-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a782e-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="a782e-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a782e-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="a782e-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a782e-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="a782e-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a782e-117">설명</span><span class="sxs-lookup"><span data-stu-id="a782e-117">DESCRIPTION</span></span>
<span data-ttu-id="a782e-118">**Update-AzVpnSite** cmdlet은 VPN 사이트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="a782e-119">예제</span><span class="sxs-lookup"><span data-stu-id="a782e-119">EXAMPLES</span></span>

### <span data-ttu-id="a782e-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="a782e-120">Example 1</span></span>

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

<span data-ttu-id="a782e-121">위의 경우 Azure의 "testRG" 리소스 그룹에 미국 서부의 Virtual WAN 리소스 그룹인 Virtual WAN이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="a782e-122">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 Virtual WAN에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="a782e-123">사이트가 만들어지면 Set-AzVpnSite 명령을 사용하여 사이트의 IpAddress를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="a782e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a782e-124">PARAMETERS</span></span>

### <span data-ttu-id="a782e-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="a782e-125">-AddressSpace</span></span>
<span data-ttu-id="a782e-126">가상 네트워크의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="a782e-127">이 또는 AddressSpaceObject를 사용하지만 둘 다 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="a782e-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a782e-128">-AsJob</span></span>
<span data-ttu-id="a782e-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a782e-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a782e-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="a782e-130">-BgpAsn</span></span>
<span data-ttu-id="a782e-131">이 VpnSite에 대한 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="a782e-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="a782e-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="a782e-133">이 VpnSite에 대한 BGP 피어링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="a782e-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="a782e-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="a782e-135">이 VpnSite에 대한 BGP 피어링 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="a782e-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a782e-136">-DefaultProfile</span></span>
<span data-ttu-id="a782e-137">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a782e-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="a782e-138">-DeviceModel</span></span>
<span data-ttu-id="a782e-139">원격 VPN 디바이스의 디바이스 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="a782e-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="a782e-140">-DeviceVendor</span></span>
<span data-ttu-id="a782e-141">원격 VPN 디바이스의 디바이스 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="a782e-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a782e-142">-InputObject</span></span>
<span data-ttu-id="a782e-143">수정할 vpn 사이트 개체</span><span class="sxs-lookup"><span data-stu-id="a782e-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="a782e-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="a782e-144">-IpAddress</span></span>
<span data-ttu-id="a782e-145">로컬 네트워크 게이트웨이의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="a782e-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="a782e-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="a782e-147">원격 VPN 디바이스의 디바이스 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="a782e-148">-Name</span><span class="sxs-lookup"><span data-stu-id="a782e-148">-Name</span></span>
<span data-ttu-id="a782e-149">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-149">The resource name.</span></span>

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

### <span data-ttu-id="a782e-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="a782e-150">-O365Policy</span></span>
<span data-ttu-id="a782e-151">이 VpnSite에 대한 Office 365 트래픽 중단 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="a782e-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a782e-152">-ResourceGroupName</span></span>
<span data-ttu-id="a782e-153">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-153">The resource group name.</span></span>

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

### <span data-ttu-id="a782e-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a782e-154">-ResourceId</span></span>
<span data-ttu-id="a782e-155">VPN 사이트에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-155">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="a782e-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="a782e-156">-Tag</span></span>
<span data-ttu-id="a782e-157">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a782e-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="a782e-158">-VirtualWan</span></span>
<span data-ttu-id="a782e-159">이 VpnSite를 VirtualWan에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="a782e-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="a782e-160">-VirtualWanId</span></span>
<span data-ttu-id="a782e-161">이 VpnSite를 ResourceId VirtualWan에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="a782e-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="a782e-162">-VirtualWanName</span></span>
<span data-ttu-id="a782e-163">이 VpnSite를 연결해야 하는 VirtualWan의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="a782e-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a782e-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="a782e-165">이 VpnSite를 연결해야 하는 VirtualWan의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="a782e-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a782e-166">-VpnSiteLink</span></span>
<span data-ttu-id="a782e-167">이 VpnSite에 있는 VpnSiteLinks 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="a782e-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a782e-168">-Confirm</span></span>
<span data-ttu-id="a782e-169">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a782e-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a782e-170">-WhatIf</span></span>
<span data-ttu-id="a782e-171">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a782e-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a782e-172">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a782e-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a782e-173">CommonParameters</span></span>
<span data-ttu-id="a782e-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a782e-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a782e-175">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a782e-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a782e-176">입력</span><span class="sxs-lookup"><span data-stu-id="a782e-176">INPUTS</span></span>

### <span data-ttu-id="a782e-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="a782e-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="a782e-178">System.String</span><span class="sxs-lookup"><span data-stu-id="a782e-178">System.String</span></span>

## <span data-ttu-id="a782e-179">출력</span><span class="sxs-lookup"><span data-stu-id="a782e-179">OUTPUTS</span></span>

### <span data-ttu-id="a782e-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="a782e-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="a782e-181">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a782e-181">NOTES</span></span>

## <span data-ttu-id="a782e-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a782e-182">RELATED LINKS</span></span>

[<span data-ttu-id="a782e-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a782e-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="a782e-184">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a782e-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="a782e-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a782e-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
