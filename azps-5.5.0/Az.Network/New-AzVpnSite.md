---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191812"
---
# <span data-ttu-id="13a14-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="13a14-101">New-AzVpnSite</span></span>

## <span data-ttu-id="13a14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13a14-102">SYNOPSIS</span></span>
<span data-ttu-id="13a14-103">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="13a14-104">이는 Cortex 가상 허브와의 S2S 연결을 위해 Azure에 업로드된 고객 분기의 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="13a14-105">구문</span><span class="sxs-lookup"><span data-stu-id="13a14-105">SYNTAX</span></span>

### <span data-ttu-id="13a14-106">ByVirtualWanNameByVpnSiteIpAddress(기본값)</span><span class="sxs-lookup"><span data-stu-id="13a14-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13a14-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="13a14-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13a14-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="13a14-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13a14-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="13a14-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13a14-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="13a14-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13a14-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="13a14-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13a14-112">설명</span><span class="sxs-lookup"><span data-stu-id="13a14-112">DESCRIPTION</span></span>
<span data-ttu-id="13a14-113">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="13a14-114">이는 Cortex 가상 허브와의 S2S 연결을 위해 Azure에 업로드된 고객 분기의 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="13a14-115">예제</span><span class="sxs-lookup"><span data-stu-id="13a14-115">EXAMPLES</span></span>

### <span data-ttu-id="13a14-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="13a14-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "nonlinkSite"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "nonlinkSite" -Name myVirtualWAN -Location "East US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "nonlinkSite" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : nonlinkSite
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="13a14-117">위에서는 Azure의 "nonlinkSite" 리소스 그룹에 미국 동부의 Virtual WAN 리소스 그룹인 Virtual WAN을 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="13a14-118">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 Virtual WAN에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="13a14-119">IPSec 연결은 다음 명령을 사용하여 이 분기 및 VpnGateway를 사용하여 New-AzVpnConnection 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="13a14-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="13a14-120">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "multilink"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName multilink -Name myVirtualWAN -Location "East US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "multilink" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)
```

<span data-ttu-id="13a14-121">위에서는 Azure의 "다중 링크" 리소스 그룹에 미국 동부에 VpnSiteLinks 1개가 있는 리소스 그룹, Virtual WAN 및 VpnSite를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="13a14-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="13a14-122">Example 3</span></span>

<span data-ttu-id="13a14-123">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="13a14-124">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="13a14-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="13a14-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13a14-125">PARAMETERS</span></span>

### <span data-ttu-id="13a14-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="13a14-126">-AddressSpace</span></span>
<span data-ttu-id="13a14-127">가상 네트워크의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="13a14-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13a14-128">-AsJob</span></span>
<span data-ttu-id="13a14-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="13a14-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13a14-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="13a14-130">-BgpAsn</span></span>
<span data-ttu-id="13a14-131">이 VpnSite에 대한 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a14-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="13a14-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="13a14-133">이 VpnSite에 대한 BGP 피어링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a14-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="13a14-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="13a14-135">이 VpnSite에 대한 BGP 피어링 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a14-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a14-136">-DefaultProfile</span></span>
<span data-ttu-id="13a14-137">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13a14-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="13a14-138">-DeviceModel</span></span>
<span data-ttu-id="13a14-139">원격 VPN 디바이스의 디바이스 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="13a14-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="13a14-140">-DeviceVendor</span></span>
<span data-ttu-id="13a14-141">원격 VPN 디바이스의 디바이스 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="13a14-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="13a14-142">-IpAddress</span></span>
<span data-ttu-id="13a14-143">이 VpnSite의 IPAddress입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-143">The IPAddress for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a14-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="13a14-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="13a14-145">원격 VPN 디바이스의 디바이스 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-145">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a14-146">-Location</span><span class="sxs-lookup"><span data-stu-id="13a14-146">-Location</span></span>
<span data-ttu-id="13a14-147">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-147">The resource location.</span></span>

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

### <span data-ttu-id="13a14-148">-Name</span><span class="sxs-lookup"><span data-stu-id="13a14-148">-Name</span></span>
<span data-ttu-id="13a14-149">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a14-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="13a14-150">-O365Policy</span></span>
<span data-ttu-id="13a14-151">이 VpnSite에 대한 Office 365 트래픽 중단 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="13a14-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a14-152">-ResourceGroupName</span></span>
<span data-ttu-id="13a14-153">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-153">The resource name.</span></span>

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

### <span data-ttu-id="13a14-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="13a14-154">-Tag</span></span>
<span data-ttu-id="13a14-155">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="13a14-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="13a14-156">-VirtualWan</span></span>
<span data-ttu-id="13a14-157">이 VpnSite를 VirtualWan에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a14-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="13a14-158">-VirtualWanId</span></span>
<span data-ttu-id="13a14-159">이 VpnSite를 ResourceId VirtualWan에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a14-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="13a14-160">-VirtualWanName</span></span>
<span data-ttu-id="13a14-161">이 VpnSite를 연결해야 하는 VirtualWan의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a14-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a14-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="13a14-163">이 VpnSite를 연결해야 하는 VirtualWan의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a14-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="13a14-164">-VpnSiteLink</span></span>
<span data-ttu-id="13a14-165">이 VpnSite에 있는 VpnSiteLinks 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: ByVirtualWanNameByVpnSiteLinkObject, ByVirtualWanObjectByVpnSiteLinkObject, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a14-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13a14-166">-Confirm</span></span>
<span data-ttu-id="13a14-167">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13a14-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13a14-168">-WhatIf</span></span>
<span data-ttu-id="13a14-169">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="13a14-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13a14-170">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13a14-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a14-171">CommonParameters</span></span>
<span data-ttu-id="13a14-172">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13a14-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a14-173">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13a14-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a14-174">입력</span><span class="sxs-lookup"><span data-stu-id="13a14-174">INPUTS</span></span>

### <span data-ttu-id="13a14-175">없음</span><span class="sxs-lookup"><span data-stu-id="13a14-175">None</span></span>

## <span data-ttu-id="13a14-176">출력</span><span class="sxs-lookup"><span data-stu-id="13a14-176">OUTPUTS</span></span>

### <span data-ttu-id="13a14-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="13a14-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="13a14-178">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13a14-178">NOTES</span></span>

## <span data-ttu-id="13a14-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13a14-179">RELATED LINKS</span></span>

[<span data-ttu-id="13a14-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="13a14-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="13a14-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="13a14-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="13a14-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="13a14-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
