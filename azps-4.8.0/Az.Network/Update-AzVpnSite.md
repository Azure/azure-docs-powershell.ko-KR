---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212964"
---
# <span data-ttu-id="95d67-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="95d67-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="95d67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d67-102">SYNOPSIS</span></span>
<span data-ttu-id="95d67-103">VPN 사이트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-103">Updates a VPN site.</span></span>

## <span data-ttu-id="95d67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95d67-104">SYNTAX</span></span>

### <span data-ttu-id="95d67-105">ByVpnSiteNameNoVirtualWanUpdate (기본값)</span><span class="sxs-lookup"><span data-stu-id="95d67-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d67-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="95d67-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d67-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="95d67-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95d67-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="95d67-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95d67-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="95d67-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d67-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="95d67-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95d67-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="95d67-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95d67-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="95d67-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d67-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="95d67-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d67-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="95d67-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d67-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="95d67-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95d67-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="95d67-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d67-117">설명은</span><span class="sxs-lookup"><span data-stu-id="95d67-117">DESCRIPTION</span></span>
<span data-ttu-id="95d67-118">**업데이트 AzVpnSite** CMDLET은 VPN 사이트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="95d67-119">예제의</span><span class="sxs-lookup"><span data-stu-id="95d67-119">EXAMPLES</span></span>

### <span data-ttu-id="95d67-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="95d67-120">Example 1</span></span>

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

<span data-ttu-id="95d67-121">위의 방법으로 Azure의 "testRG" 리소스 그룹에 있는 서쪽의 가상 WAN 인 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="95d67-122">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 가상 WAN에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="95d67-123">사이트를 만든 후에는 Set-AzVpnSite 명령을 사용 하 여 사이트의 IpAddress를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="95d67-124">변수</span><span class="sxs-lookup"><span data-stu-id="95d67-124">PARAMETERS</span></span>

### <span data-ttu-id="95d67-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="95d67-125">-AddressSpace</span></span>
<span data-ttu-id="95d67-126">가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="95d67-127">이 or AddressSpaceObject을 모두 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="95d67-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95d67-128">-AsJob</span></span>
<span data-ttu-id="95d67-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="95d67-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95d67-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="95d67-130">-BgpAsn</span></span>
<span data-ttu-id="95d67-131">이 VpnSite의 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="95d67-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="95d67-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="95d67-133">이 VpnSite의 BGP 피어 링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="95d67-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="95d67-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="95d67-135">이 VpnSite의 BGP 피어 링 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="95d67-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d67-136">-DefaultProfile</span></span>
<span data-ttu-id="95d67-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95d67-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="95d67-138">-DeviceModel</span></span>
<span data-ttu-id="95d67-139">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="95d67-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="95d67-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="95d67-140">-DeviceVendor</span></span>
<span data-ttu-id="95d67-141">원격 vpn 장치의 장치 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="95d67-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95d67-142">-InputObject</span></span>
<span data-ttu-id="95d67-143">수정할 vpn 사이트 개체</span><span class="sxs-lookup"><span data-stu-id="95d67-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="95d67-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="95d67-144">-IpAddress</span></span>
<span data-ttu-id="95d67-145">로컬 네트워크 게이트웨이의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="95d67-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="95d67-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="95d67-147">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="95d67-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="95d67-148">-이름</span><span class="sxs-lookup"><span data-stu-id="95d67-148">-Name</span></span>
<span data-ttu-id="95d67-149">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-149">The resource name.</span></span>

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

### <span data-ttu-id="95d67-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="95d67-150">-O365Policy</span></span>
<span data-ttu-id="95d67-151">이 VpnSite에 대 한 office 365 트래픽 아웃 브레이크 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="95d67-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d67-152">-ResourceGroupName</span></span>
<span data-ttu-id="95d67-153">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-153">The resource group name.</span></span>

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

### <span data-ttu-id="95d67-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95d67-154">-ResourceId</span></span>
<span data-ttu-id="95d67-155">Vpn 사이트에 대 한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-155">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="95d67-156">태그</span><span class="sxs-lookup"><span data-stu-id="95d67-156">-Tag</span></span>
<span data-ttu-id="95d67-157">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="95d67-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="95d67-158">-VirtualWan</span></span>
<span data-ttu-id="95d67-159">이 VpnSite에 연결 해야 하는 VirtualWan입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="95d67-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="95d67-160">-VirtualWanId</span></span>
<span data-ttu-id="95d67-161">이 VpnSite에 연결 되어야 하는 ResourceId VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="95d67-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="95d67-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="95d67-162">-VirtualWanName</span></span>
<span data-ttu-id="95d67-163">이 VpnSite에 연결 해야 하는 VirtualWan의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="95d67-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d67-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="95d67-165">이 VpnSite에 연결 되어야 하는 VirtualWan의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="95d67-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="95d67-166">-VpnSiteLink</span></span>
<span data-ttu-id="95d67-167">이 VpnSite에 있는 VpnSiteLinks의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="95d67-168">-확인</span><span class="sxs-lookup"><span data-stu-id="95d67-168">-Confirm</span></span>
<span data-ttu-id="95d67-169">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d67-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d67-170">-WhatIf</span></span>
<span data-ttu-id="95d67-171">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95d67-172">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d67-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d67-173">CommonParameters</span></span>
<span data-ttu-id="95d67-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d67-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d67-175">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95d67-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d67-176">입력</span><span class="sxs-lookup"><span data-stu-id="95d67-176">INPUTS</span></span>

### <span data-ttu-id="95d67-177">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="95d67-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="95d67-178">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="95d67-178">System.String</span></span>

## <span data-ttu-id="95d67-179">출력</span><span class="sxs-lookup"><span data-stu-id="95d67-179">OUTPUTS</span></span>

### <span data-ttu-id="95d67-180">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="95d67-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="95d67-181">상속자</span><span class="sxs-lookup"><span data-stu-id="95d67-181">NOTES</span></span>

## <span data-ttu-id="95d67-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95d67-182">RELATED LINKS</span></span>

[<span data-ttu-id="95d67-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="95d67-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="95d67-184">새로운 AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="95d67-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="95d67-185">제거-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="95d67-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
