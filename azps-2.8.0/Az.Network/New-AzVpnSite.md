---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: fe9449eedaedfa08880548ceda769835d6eb3f7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871325"
---
# <span data-ttu-id="418a6-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="418a6-101">New-AzVpnSite</span></span>

## <span data-ttu-id="418a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="418a6-102">SYNOPSIS</span></span>
<span data-ttu-id="418a6-103">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="418a6-104">이는 Cortex 가상 허브를 사용 하 여 S2S 연결을 위해 Azure에 업로드 되는 고객 분기에 대 한 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="418a6-105">구문과</span><span class="sxs-lookup"><span data-stu-id="418a6-105">SYNTAX</span></span>

### <span data-ttu-id="418a6-106">ByVirtualWanNameByVpnSiteIpAddress (기본값)</span><span class="sxs-lookup"><span data-stu-id="418a6-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="418a6-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="418a6-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="418a6-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="418a6-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="418a6-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="418a6-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="418a6-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="418a6-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="418a6-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="418a6-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="418a6-112">설명은</span><span class="sxs-lookup"><span data-stu-id="418a6-112">DESCRIPTION</span></span>
<span data-ttu-id="418a6-113">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="418a6-114">이는 Cortex 가상 허브를 사용 하 여 S2S 연결을 위해 Azure에 업로드 되는 고객 분기에 대 한 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="418a6-115">예제의</span><span class="sxs-lookup"><span data-stu-id="418a6-115">EXAMPLES</span></span>

### <span data-ttu-id="418a6-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="418a6-116">Example 1</span></span>

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

<span data-ttu-id="418a6-117">위의 방법으로 Azure에서 "nonlinkSite" 리소스 그룹에 있는 동쪽의 가상 WAN 인 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="418a6-118">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 가상 WAN에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="418a6-119">그런 다음 New-AzVpnConnection 명령을 사용 하 여이 분기와 VpnGateway IPSec 연결을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="418a6-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="418a6-120">Example 2</span></span>
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

<span data-ttu-id="418a6-121">Azure의 "멀티 링크" 리소스 그룹에 미국 VpnSiteLinks 1 개를 사용 하 여 리소스 그룹, 가상 WAN 및 VpnSite를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

## <span data-ttu-id="418a6-122">변수</span><span class="sxs-lookup"><span data-stu-id="418a6-122">PARAMETERS</span></span>

### <span data-ttu-id="418a6-123">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="418a6-123">-AddressSpace</span></span>
<span data-ttu-id="418a6-124">가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-124">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="418a6-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="418a6-125">-AsJob</span></span>
<span data-ttu-id="418a6-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="418a6-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="418a6-127">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="418a6-127">-BgpAsn</span></span>
<span data-ttu-id="418a6-128">이 VpnSite의 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-128">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="418a6-129">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="418a6-129">-BgpPeeringAddress</span></span>
<span data-ttu-id="418a6-130">이 VpnSite의 BGP 피어 링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-130">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="418a6-131">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="418a6-131">-BgpPeeringWeight</span></span>
<span data-ttu-id="418a6-132">이 VpnSite의 BGP 피어 링 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-132">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="418a6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418a6-133">-DefaultProfile</span></span>
<span data-ttu-id="418a6-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="418a6-135">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="418a6-135">-DeviceModel</span></span>
<span data-ttu-id="418a6-136">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="418a6-136">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="418a6-137">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="418a6-137">-DeviceVendor</span></span>
<span data-ttu-id="418a6-138">원격 vpn 장치의 장치 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-138">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="418a6-139">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="418a6-139">-IpAddress</span></span>
<span data-ttu-id="418a6-140">이 VpnSite의 IPAddress입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-140">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="418a6-141">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="418a6-141">-LinkSpeedInMbps</span></span>
<span data-ttu-id="418a6-142">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="418a6-142">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="418a6-143">-위치</span><span class="sxs-lookup"><span data-stu-id="418a6-143">-Location</span></span>
<span data-ttu-id="418a6-144">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-144">The resource location.</span></span>

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

### <span data-ttu-id="418a6-145">-이름</span><span class="sxs-lookup"><span data-stu-id="418a6-145">-Name</span></span>
<span data-ttu-id="418a6-146">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-146">The resource name.</span></span>

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

### <span data-ttu-id="418a6-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="418a6-147">-ResourceGroupName</span></span>
<span data-ttu-id="418a6-148">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-148">The resource name.</span></span>

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

### <span data-ttu-id="418a6-149">태그</span><span class="sxs-lookup"><span data-stu-id="418a6-149">-Tag</span></span>
<span data-ttu-id="418a6-150">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-150">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="418a6-151">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="418a6-151">-VirtualWan</span></span>
<span data-ttu-id="418a6-152">이 VpnSite에 연결 해야 하는 VirtualWan입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-152">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="418a6-153">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="418a6-153">-VirtualWanId</span></span>
<span data-ttu-id="418a6-154">이 VpnSite에 연결 되어야 하는 ResourceId VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="418a6-154">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="418a6-155">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="418a6-155">-VirtualWanName</span></span>
<span data-ttu-id="418a6-156">이 VpnSite에 연결 해야 하는 VirtualWan의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-156">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="418a6-157">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="418a6-157">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="418a6-158">이 VpnSite에 연결 되어야 하는 VirtualWan의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-158">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="418a6-159">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="418a6-159">-VpnSiteLink</span></span>
<span data-ttu-id="418a6-160">이 VpnSite에 있는 VpnSiteLinks의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-160">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="418a6-161">-확인</span><span class="sxs-lookup"><span data-stu-id="418a6-161">-Confirm</span></span>
<span data-ttu-id="418a6-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="418a6-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="418a6-163">-WhatIf</span></span>
<span data-ttu-id="418a6-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="418a6-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="418a6-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418a6-166">CommonParameters</span></span>
<span data-ttu-id="418a6-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="418a6-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418a6-168">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="418a6-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418a6-169">입력</span><span class="sxs-lookup"><span data-stu-id="418a6-169">INPUTS</span></span>

### <span data-ttu-id="418a6-170">않아야</span><span class="sxs-lookup"><span data-stu-id="418a6-170">None</span></span>

## <span data-ttu-id="418a6-171">출력</span><span class="sxs-lookup"><span data-stu-id="418a6-171">OUTPUTS</span></span>

### <span data-ttu-id="418a6-172">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="418a6-172">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="418a6-173">상속자</span><span class="sxs-lookup"><span data-stu-id="418a6-173">NOTES</span></span>

## <span data-ttu-id="418a6-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="418a6-174">RELATED LINKS</span></span>

[<span data-ttu-id="418a6-175">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="418a6-175">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="418a6-176">제거-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="418a6-176">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="418a6-177">업데이트-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="418a6-177">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
