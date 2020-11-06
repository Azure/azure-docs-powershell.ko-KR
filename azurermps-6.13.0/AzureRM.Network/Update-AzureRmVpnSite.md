---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnSite.md
ms.openlocfilehash: fa24f61d0e638cb38e7cf882aac2191a5119b1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531371"
---
# <span data-ttu-id="9ceae-101">Update-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="9ceae-101">Update-AzureRmVpnSite</span></span>

## <span data-ttu-id="9ceae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ceae-102">SYNOPSIS</span></span>
<span data-ttu-id="9ceae-103">고객 분기를 나타내는 VpnSite을 의도 하는 목표 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-103">Updates a VpnSite representing a customer branch to an intended goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ceae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ceae-104">SYNTAX</span></span>

### <span data-ttu-id="9ceae-105">ByVpnSiteNameNoVirtualWanUpdate (기본값)</span><span class="sxs-lookup"><span data-stu-id="9ceae-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ceae-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9ceae-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ceae-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9ceae-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ceae-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9ceae-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ceae-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9ceae-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ceae-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9ceae-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ceae-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9ceae-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ceae-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="9ceae-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ceae-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9ceae-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ceae-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9ceae-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ceae-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9ceae-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ceae-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="9ceae-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ceae-117">설명은</span><span class="sxs-lookup"><span data-stu-id="9ceae-117">DESCRIPTION</span></span>
<span data-ttu-id="9ceae-118">고객 분기를 나타내는 VpnSite을 의도 하는 목표 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-118">Updates a VpnSite representing a customer branch to an intended goal state.</span></span>

## <span data-ttu-id="9ceae-119">예제의</span><span class="sxs-lookup"><span data-stu-id="9ceae-119">EXAMPLES</span></span>

### <span data-ttu-id="9ceae-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="9ceae-120">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

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

<span data-ttu-id="9ceae-121">위의 방법으로 Azure의 "testRG" 리소스 그룹에 있는 서쪽의 가상 WAN 인 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="9ceae-122">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 가상 WAN에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="9ceae-123">사이트를 만든 후에는 Set-AzureRmVpnSite 명령을 사용 하 여 사이트의 IpAddress를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-123">Once the site is created, it updates the IpAddress of the site using the Set-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="9ceae-124">변수</span><span class="sxs-lookup"><span data-stu-id="9ceae-124">PARAMETERS</span></span>

### <span data-ttu-id="9ceae-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="9ceae-125">-AddressSpace</span></span>
<span data-ttu-id="9ceae-126">가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="9ceae-127">이 or AddressSpaceObject을 모두 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-127">Use this or AddressSpaceObject but not both.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ceae-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ceae-128">-AsJob</span></span>
<span data-ttu-id="9ceae-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9ceae-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ceae-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="9ceae-130">-BgpAsn</span></span>
<span data-ttu-id="9ceae-131">이 VpnSite의 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="9ceae-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="9ceae-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="9ceae-133">이 VpnSite의 BGP 피어 링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="9ceae-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="9ceae-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="9ceae-135">이 VpnSite의 BGP 피어 링 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="9ceae-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ceae-136">-DefaultProfile</span></span>
<span data-ttu-id="9ceae-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ceae-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="9ceae-138">-DeviceModel</span></span>
<span data-ttu-id="9ceae-139">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="9ceae-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="9ceae-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="9ceae-140">-DeviceVendor</span></span>
<span data-ttu-id="9ceae-141">원격 vpn 장치의 장치 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="9ceae-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ceae-142">-InputObject</span></span>
<span data-ttu-id="9ceae-143">수정할 vpn 사이트 개체</span><span class="sxs-lookup"><span data-stu-id="9ceae-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="9ceae-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="9ceae-144">-IpAddress</span></span>
<span data-ttu-id="9ceae-145">로컬 네트워크 게이트웨이의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="9ceae-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="9ceae-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="9ceae-147">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="9ceae-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="9ceae-148">-이름</span><span class="sxs-lookup"><span data-stu-id="9ceae-148">-Name</span></span>
<span data-ttu-id="9ceae-149">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-149">The resource name.</span></span>

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

### <span data-ttu-id="9ceae-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ceae-150">-ResourceGroupName</span></span>
<span data-ttu-id="9ceae-151">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-151">The resource group name.</span></span>

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

### <span data-ttu-id="9ceae-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ceae-152">-ResourceId</span></span>
<span data-ttu-id="9ceae-153">Vpn 사이트에 대 한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-153">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="9ceae-154">태그</span><span class="sxs-lookup"><span data-stu-id="9ceae-154">-Tag</span></span>
<span data-ttu-id="9ceae-155">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9ceae-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="9ceae-156">-VirtualWan</span></span>
<span data-ttu-id="9ceae-157">이 VpnSite에 연결 해야 하는 VirtualWan입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9ceae-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="9ceae-158">-VirtualWanId</span></span>
<span data-ttu-id="9ceae-159">이 VpnSite에 연결 되어야 하는 ResourceId VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="9ceae-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9ceae-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9ceae-160">-VirtualWanName</span></span>
<span data-ttu-id="9ceae-161">이 VpnSite에 연결 해야 하는 VirtualWan의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9ceae-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ceae-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="9ceae-163">이 VpnSite에 연결 되어야 하는 VirtualWan의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9ceae-164">-확인</span><span class="sxs-lookup"><span data-stu-id="9ceae-164">-Confirm</span></span>
<span data-ttu-id="9ceae-165">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ceae-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ceae-166">-WhatIf</span></span>
<span data-ttu-id="9ceae-167">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ceae-168">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ceae-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ceae-169">CommonParameters</span></span>
<span data-ttu-id="9ceae-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ceae-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ceae-171">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ceae-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ceae-172">입력</span><span class="sxs-lookup"><span data-stu-id="9ceae-172">INPUTS</span></span>

### <span data-ttu-id="9ceae-173">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9ceae-173">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="9ceae-174">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ceae-174">System.String</span></span>

## <span data-ttu-id="9ceae-175">출력</span><span class="sxs-lookup"><span data-stu-id="9ceae-175">OUTPUTS</span></span>

### <span data-ttu-id="9ceae-176">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9ceae-176">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="9ceae-177">상속자</span><span class="sxs-lookup"><span data-stu-id="9ceae-177">NOTES</span></span>

## <span data-ttu-id="9ceae-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ceae-178">RELATED LINKS</span></span>
