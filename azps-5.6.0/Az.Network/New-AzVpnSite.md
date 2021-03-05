---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 578835b000b6efecb3a1429b884ad2416f6c289d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984336"
---
# <span data-ttu-id="faf1f-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="faf1f-101">New-AzVpnSite</span></span>

## <span data-ttu-id="faf1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf1f-102">SYNOPSIS</span></span>
<span data-ttu-id="faf1f-103">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="faf1f-104">이는 Cortex 가상 허브와 S2S 연결에 대해 Azure에 업로드된 고객 분기의 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="faf1f-105">구문</span><span class="sxs-lookup"><span data-stu-id="faf1f-105">SYNTAX</span></span>

### <span data-ttu-id="faf1f-106">ByVirtualWanNameByVpnSiteIpAddress(기본값)</span><span class="sxs-lookup"><span data-stu-id="faf1f-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf1f-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="faf1f-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf1f-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="faf1f-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="faf1f-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="faf1f-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="faf1f-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="faf1f-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="faf1f-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="faf1f-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="faf1f-112">설명</span><span class="sxs-lookup"><span data-stu-id="faf1f-112">DESCRIPTION</span></span>
<span data-ttu-id="faf1f-113">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="faf1f-114">이는 Cortex 가상 허브와 S2S 연결에 대해 Azure에 업로드된 고객 분기의 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="faf1f-115">예제</span><span class="sxs-lookup"><span data-stu-id="faf1f-115">EXAMPLES</span></span>

### <span data-ttu-id="faf1f-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="faf1f-116">Example 1</span></span>

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

<span data-ttu-id="faf1f-117">위의 리소스 그룹은 Azure에서 "nonlinkSite" 리소스 그룹에서 미국 동부의 Virtual WAN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="faf1f-118">그런 다음, VpnSite를 만들어 고객 분기를 나타내고 Virtual WAN에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="faf1f-119">그런 다음 IPSec 연결을 이 분기 및 VpnGateway를 사용하여 New-AzVpnConnection 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="faf1f-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="faf1f-120">Example 2</span></span>
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

<span data-ttu-id="faf1f-121">위의 리소스 그룹은 Azure의 "멀티링크" 리소스 그룹에서 미국 동부에 VpnSiteLinks 1개가 있는 VpnSite 그룹, Virtual WAN 및 VpnSite를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="faf1f-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="faf1f-122">Example 3</span></span>

<span data-ttu-id="faf1f-123">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="faf1f-124">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="faf1f-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="faf1f-125">매개 변수</span><span class="sxs-lookup"><span data-stu-id="faf1f-125">PARAMETERS</span></span>

### <span data-ttu-id="faf1f-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="faf1f-126">-AddressSpace</span></span>
<span data-ttu-id="faf1f-127">가상 네트워크의 주소 도두사입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="faf1f-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="faf1f-128">-AsJob</span></span>
<span data-ttu-id="faf1f-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="faf1f-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="faf1f-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="faf1f-130">-BgpAsn</span></span>
<span data-ttu-id="faf1f-131">이 VpnSite에 대한 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="faf1f-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="faf1f-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="faf1f-133">이 VpnSite에 대한 BGP 피어링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="faf1f-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="faf1f-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="faf1f-135">이 VpnSite에 대한 BGP 피어링 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="faf1f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf1f-136">-DefaultProfile</span></span>
<span data-ttu-id="faf1f-137">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faf1f-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="faf1f-138">-DeviceModel</span></span>
<span data-ttu-id="faf1f-139">원격 VPN 장치의 디바이스 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="faf1f-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="faf1f-140">-DeviceVendor</span></span>
<span data-ttu-id="faf1f-141">원격 VPN 디바이스의 디바이스 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="faf1f-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="faf1f-142">-IpAddress</span></span>
<span data-ttu-id="faf1f-143">이 VpnSite의 IPAddress입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-143">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="faf1f-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="faf1f-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="faf1f-145">원격 VPN 장치의 디바이스 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-145">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="faf1f-146">-Location</span><span class="sxs-lookup"><span data-stu-id="faf1f-146">-Location</span></span>
<span data-ttu-id="faf1f-147">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-147">The resource location.</span></span>

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

### <span data-ttu-id="faf1f-148">-Name</span><span class="sxs-lookup"><span data-stu-id="faf1f-148">-Name</span></span>
<span data-ttu-id="faf1f-149">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-149">The resource name.</span></span>

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

### <span data-ttu-id="faf1f-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="faf1f-150">-O365Policy</span></span>
<span data-ttu-id="faf1f-151">이 VpnSite에 대한 Office 365 트래픽 중단 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="faf1f-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf1f-152">-ResourceGroupName</span></span>
<span data-ttu-id="faf1f-153">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-153">The resource name.</span></span>

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

### <span data-ttu-id="faf1f-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="faf1f-154">-Tag</span></span>
<span data-ttu-id="faf1f-155">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="faf1f-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="faf1f-156">-VirtualWan</span></span>
<span data-ttu-id="faf1f-157">VirtualWan 이 VpnSite에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="faf1f-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="faf1f-158">-VirtualWanId</span></span>
<span data-ttu-id="faf1f-159">ResourceId VirtualWan 이 VpnSite에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="faf1f-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="faf1f-160">-VirtualWanName</span></span>
<span data-ttu-id="faf1f-161">VirtualWan의 이름을 이 VpnSite에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="faf1f-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf1f-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="faf1f-163">VirtualWan의 리소스 그룹 이름 이 VpnSite에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="faf1f-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="faf1f-164">-VpnSiteLink</span></span>
<span data-ttu-id="faf1f-165">이 VpnSite가 있는 VpnSiteLinks 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="faf1f-166">-확인</span><span class="sxs-lookup"><span data-stu-id="faf1f-166">-Confirm</span></span>
<span data-ttu-id="faf1f-167">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faf1f-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faf1f-168">-WhatIf</span></span>
<span data-ttu-id="faf1f-169">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faf1f-170">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faf1f-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf1f-171">CommonParameters</span></span>
<span data-ttu-id="faf1f-172">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="faf1f-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf1f-173">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="faf1f-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf1f-174">입력</span><span class="sxs-lookup"><span data-stu-id="faf1f-174">INPUTS</span></span>

### <span data-ttu-id="faf1f-175">없음</span><span class="sxs-lookup"><span data-stu-id="faf1f-175">None</span></span>

## <span data-ttu-id="faf1f-176">출력</span><span class="sxs-lookup"><span data-stu-id="faf1f-176">OUTPUTS</span></span>

### <span data-ttu-id="faf1f-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="faf1f-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="faf1f-178">참고 사항</span><span class="sxs-lookup"><span data-stu-id="faf1f-178">NOTES</span></span>

## <span data-ttu-id="faf1f-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="faf1f-179">RELATED LINKS</span></span>

[<span data-ttu-id="faf1f-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="faf1f-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="faf1f-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="faf1f-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="faf1f-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="faf1f-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
