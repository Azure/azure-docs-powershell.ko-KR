---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: 30e8113cee3a544e514bb10ef4592995e50a0353
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699920"
---
# <span data-ttu-id="fbdf0-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="fbdf0-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="fbdf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbdf0-102">SYNOPSIS</span></span>
<span data-ttu-id="fbdf0-103">VPN 사이트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-103">Updates a VPN site.</span></span>

## <span data-ttu-id="fbdf0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fbdf0-104">SYNTAX</span></span>

### <span data-ttu-id="fbdf0-105">ByVpnSiteNameNoVirtualWanUpdate (기본값)</span><span class="sxs-lookup"><span data-stu-id="fbdf0-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbdf0-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="fbdf0-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbdf0-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="fbdf0-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbdf0-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="fbdf0-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbdf0-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="fbdf0-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbdf0-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="fbdf0-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbdf0-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="fbdf0-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbdf0-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="fbdf0-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbdf0-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="fbdf0-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbdf0-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="fbdf0-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbdf0-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="fbdf0-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbdf0-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="fbdf0-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbdf0-117">설명은</span><span class="sxs-lookup"><span data-stu-id="fbdf0-117">DESCRIPTION</span></span>
<span data-ttu-id="fbdf0-118">**업데이트 AzVpnSite** CMDLET은 VPN 사이트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="fbdf0-119">예제의</span><span class="sxs-lookup"><span data-stu-id="fbdf0-119">EXAMPLES</span></span>

### <span data-ttu-id="fbdf0-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="fbdf0-120">Example 1</span></span>

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

<span data-ttu-id="fbdf0-121">위의 방법으로 Azure의 "testRG" 리소스 그룹에 있는 서쪽의 가상 WAN 인 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="fbdf0-122">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 가상 WAN에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="fbdf0-123">사이트를 만든 후에는 Set-AzVpnSite 명령을 사용 하 여 사이트의 IpAddress를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="fbdf0-124">변수</span><span class="sxs-lookup"><span data-stu-id="fbdf0-124">PARAMETERS</span></span>

### <span data-ttu-id="fbdf0-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="fbdf0-125">-AddressSpace</span></span>
<span data-ttu-id="fbdf0-126">가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="fbdf0-127">이 or AddressSpaceObject을 모두 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="fbdf0-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbdf0-128">-AsJob</span></span>
<span data-ttu-id="fbdf0-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fbdf0-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbdf0-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="fbdf0-130">-BgpAsn</span></span>
<span data-ttu-id="fbdf0-131">이 VpnSite의 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="fbdf0-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="fbdf0-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="fbdf0-133">이 VpnSite의 BGP 피어 링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="fbdf0-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="fbdf0-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="fbdf0-135">이 VpnSite의 BGP 피어 링 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="fbdf0-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbdf0-136">-DefaultProfile</span></span>
<span data-ttu-id="fbdf0-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbdf0-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="fbdf0-138">-DeviceModel</span></span>
<span data-ttu-id="fbdf0-139">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="fbdf0-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="fbdf0-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="fbdf0-140">-DeviceVendor</span></span>
<span data-ttu-id="fbdf0-141">원격 vpn 장치의 장치 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="fbdf0-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbdf0-142">-InputObject</span></span>
<span data-ttu-id="fbdf0-143">수정할 vpn 사이트 개체</span><span class="sxs-lookup"><span data-stu-id="fbdf0-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="fbdf0-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="fbdf0-144">-IpAddress</span></span>
<span data-ttu-id="fbdf0-145">로컬 네트워크 게이트웨이의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="fbdf0-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="fbdf0-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="fbdf0-147">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="fbdf0-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="fbdf0-148">-이름</span><span class="sxs-lookup"><span data-stu-id="fbdf0-148">-Name</span></span>
<span data-ttu-id="fbdf0-149">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-149">The resource name.</span></span>

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

### <span data-ttu-id="fbdf0-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbdf0-150">-ResourceGroupName</span></span>
<span data-ttu-id="fbdf0-151">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-151">The resource group name.</span></span>

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

### <span data-ttu-id="fbdf0-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbdf0-152">-ResourceId</span></span>
<span data-ttu-id="fbdf0-153">Vpn 사이트에 대 한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-153">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="fbdf0-154">태그</span><span class="sxs-lookup"><span data-stu-id="fbdf0-154">-Tag</span></span>
<span data-ttu-id="fbdf0-155">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fbdf0-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="fbdf0-156">-VirtualWan</span></span>
<span data-ttu-id="fbdf0-157">이 VpnSite에 연결 해야 하는 VirtualWan입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="fbdf0-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="fbdf0-158">-VirtualWanId</span></span>
<span data-ttu-id="fbdf0-159">이 VpnSite에 연결 되어야 하는 ResourceId VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="fbdf0-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="fbdf0-160">-VirtualWanName</span></span>
<span data-ttu-id="fbdf0-161">이 VpnSite에 연결 해야 하는 VirtualWan의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="fbdf0-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbdf0-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="fbdf0-163">이 VpnSite에 연결 되어야 하는 VirtualWan의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="fbdf0-164">-확인</span><span class="sxs-lookup"><span data-stu-id="fbdf0-164">-Confirm</span></span>
<span data-ttu-id="fbdf0-165">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbdf0-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbdf0-166">-WhatIf</span></span>
<span data-ttu-id="fbdf0-167">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbdf0-168">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbdf0-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbdf0-169">CommonParameters</span></span>
<span data-ttu-id="fbdf0-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbdf0-171">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbdf0-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbdf0-172">입력</span><span class="sxs-lookup"><span data-stu-id="fbdf0-172">INPUTS</span></span>

### <span data-ttu-id="fbdf0-173">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-173">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="fbdf0-174">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fbdf0-174">System.String</span></span>

## <span data-ttu-id="fbdf0-175">출력</span><span class="sxs-lookup"><span data-stu-id="fbdf0-175">OUTPUTS</span></span>

### <span data-ttu-id="fbdf0-176">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="fbdf0-176">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="fbdf0-177">상속자</span><span class="sxs-lookup"><span data-stu-id="fbdf0-177">NOTES</span></span>

## <span data-ttu-id="fbdf0-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbdf0-178">RELATED LINKS</span></span>

[<span data-ttu-id="fbdf0-179">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="fbdf0-179">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="fbdf0-180">새로운 AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="fbdf0-180">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="fbdf0-181">제거-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="fbdf0-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)