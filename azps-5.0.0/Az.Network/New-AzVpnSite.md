---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311456"
---
# <span data-ttu-id="79552-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="79552-101">New-AzVpnSite</span></span>

## <span data-ttu-id="79552-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79552-102">SYNOPSIS</span></span>
<span data-ttu-id="79552-103">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79552-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="79552-104">이는 Cortex 가상 허브를 사용 하 여 S2S 연결을 위해 Azure에 업로드 되는 고객 분기에 대 한 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="79552-105">구문과</span><span class="sxs-lookup"><span data-stu-id="79552-105">SYNTAX</span></span>

### <span data-ttu-id="79552-106">ByVirtualWanNameByVpnSiteIpAddress (기본값)</span><span class="sxs-lookup"><span data-stu-id="79552-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79552-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="79552-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79552-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="79552-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79552-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="79552-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79552-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="79552-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79552-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="79552-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79552-112">설명은</span><span class="sxs-lookup"><span data-stu-id="79552-112">DESCRIPTION</span></span>
<span data-ttu-id="79552-113">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79552-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="79552-114">이는 Cortex 가상 허브를 사용 하 여 S2S 연결을 위해 Azure에 업로드 되는 고객 분기에 대 한 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="79552-115">예제의</span><span class="sxs-lookup"><span data-stu-id="79552-115">EXAMPLES</span></span>

### <span data-ttu-id="79552-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="79552-116">Example 1</span></span>

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

<span data-ttu-id="79552-117">위의 방법으로 Azure에서 "nonlinkSite" 리소스 그룹에 있는 동쪽의 가상 WAN 인 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79552-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="79552-118">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 가상 WAN에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="79552-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="79552-119">그런 다음 New-AzVpnConnection 명령을 사용 하 여이 분기와 VpnGateway IPSec 연결을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79552-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="79552-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="79552-120">Example 2</span></span>
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

<span data-ttu-id="79552-121">Azure의 "멀티 링크" 리소스 그룹에 미국 VpnSiteLinks 1 개를 사용 하 여 리소스 그룹, 가상 WAN 및 VpnSite를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79552-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="79552-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="79552-122">Example 3</span></span>

<span data-ttu-id="79552-123">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79552-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="79552-124">생성</span><span class="sxs-lookup"><span data-stu-id="79552-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="79552-125">변수</span><span class="sxs-lookup"><span data-stu-id="79552-125">PARAMETERS</span></span>

### <span data-ttu-id="79552-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="79552-126">-AddressSpace</span></span>
<span data-ttu-id="79552-127">가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="79552-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79552-128">-AsJob</span></span>
<span data-ttu-id="79552-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="79552-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79552-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="79552-130">-BgpAsn</span></span>
<span data-ttu-id="79552-131">이 VpnSite의 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="79552-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="79552-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="79552-133">이 VpnSite의 BGP 피어 링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="79552-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="79552-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="79552-135">이 VpnSite의 BGP 피어 링 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="79552-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79552-136">-DefaultProfile</span></span>
<span data-ttu-id="79552-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79552-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="79552-138">-DeviceModel</span></span>
<span data-ttu-id="79552-139">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="79552-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="79552-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="79552-140">-DeviceVendor</span></span>
<span data-ttu-id="79552-141">원격 vpn 장치의 장치 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="79552-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="79552-142">-IpAddress</span></span>
<span data-ttu-id="79552-143">이 VpnSite의 IPAddress입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-143">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="79552-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="79552-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="79552-145">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="79552-145">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="79552-146">-위치</span><span class="sxs-lookup"><span data-stu-id="79552-146">-Location</span></span>
<span data-ttu-id="79552-147">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-147">The resource location.</span></span>

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

### <span data-ttu-id="79552-148">-이름</span><span class="sxs-lookup"><span data-stu-id="79552-148">-Name</span></span>
<span data-ttu-id="79552-149">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-149">The resource name.</span></span>

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

### <span data-ttu-id="79552-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="79552-150">-O365Policy</span></span>
<span data-ttu-id="79552-151">이 VpnSite에 대 한 office 365 트래픽 아웃 브레이크 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="79552-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79552-152">-ResourceGroupName</span></span>
<span data-ttu-id="79552-153">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-153">The resource name.</span></span>

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

### <span data-ttu-id="79552-154">태그</span><span class="sxs-lookup"><span data-stu-id="79552-154">-Tag</span></span>
<span data-ttu-id="79552-155">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="79552-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="79552-156">-VirtualWan</span></span>
<span data-ttu-id="79552-157">이 VpnSite에 연결 해야 하는 VirtualWan입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="79552-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="79552-158">-VirtualWanId</span></span>
<span data-ttu-id="79552-159">이 VpnSite에 연결 되어야 하는 ResourceId VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="79552-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="79552-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="79552-160">-VirtualWanName</span></span>
<span data-ttu-id="79552-161">이 VpnSite에 연결 해야 하는 VirtualWan의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="79552-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79552-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="79552-163">이 VpnSite에 연결 되어야 하는 VirtualWan의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="79552-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="79552-164">-VpnSiteLink</span></span>
<span data-ttu-id="79552-165">이 VpnSite에 있는 VpnSiteLinks의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="79552-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="79552-166">-확인</span><span class="sxs-lookup"><span data-stu-id="79552-166">-Confirm</span></span>
<span data-ttu-id="79552-167">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79552-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79552-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79552-168">-WhatIf</span></span>
<span data-ttu-id="79552-169">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79552-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79552-170">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79552-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79552-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79552-171">CommonParameters</span></span>
<span data-ttu-id="79552-172">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79552-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79552-173">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79552-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79552-174">입력</span><span class="sxs-lookup"><span data-stu-id="79552-174">INPUTS</span></span>

### <span data-ttu-id="79552-175">않아야</span><span class="sxs-lookup"><span data-stu-id="79552-175">None</span></span>

## <span data-ttu-id="79552-176">출력</span><span class="sxs-lookup"><span data-stu-id="79552-176">OUTPUTS</span></span>

### <span data-ttu-id="79552-177">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="79552-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="79552-178">상속자</span><span class="sxs-lookup"><span data-stu-id="79552-178">NOTES</span></span>

## <span data-ttu-id="79552-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79552-179">RELATED LINKS</span></span>

[<span data-ttu-id="79552-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="79552-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="79552-181">제거-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="79552-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="79552-182">업데이트-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="79552-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
