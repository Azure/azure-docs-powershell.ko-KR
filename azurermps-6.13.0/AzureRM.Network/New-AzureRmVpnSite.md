---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnSite.md
ms.openlocfilehash: b8594aab0b9475ed37a0a205010e92fdb2a4db7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702308"
---
# <span data-ttu-id="84b88-101">New-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="84b88-101">New-AzureRmVpnSite</span></span>

## <span data-ttu-id="84b88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84b88-102">SYNOPSIS</span></span>
<span data-ttu-id="84b88-103">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="84b88-104">이는 Cortex 가상 허브를 사용 하 여 S2S 연결을 위해 Azure에 업로드 되는 고객 분기에 대 한 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84b88-105">구문과</span><span class="sxs-lookup"><span data-stu-id="84b88-105">SYNTAX</span></span>

### <span data-ttu-id="84b88-106">ByVirtualWanName (기본값)</span><span class="sxs-lookup"><span data-stu-id="84b88-106">ByVirtualWanName (Default)</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b88-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="84b88-107">ByVirtualWanObject</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84b88-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="84b88-108">ByVirtualWanResourceId</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84b88-109">설명은</span><span class="sxs-lookup"><span data-stu-id="84b88-109">DESCRIPTION</span></span>
<span data-ttu-id="84b88-110">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="84b88-111">이는 Cortex 가상 허브를 사용 하 여 S2S 연결을 위해 Azure에 업로드 되는 고객 분기에 대 한 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="84b88-112">예제의</span><span class="sxs-lookup"><span data-stu-id="84b88-112">EXAMPLES</span></span>

### <span data-ttu-id="84b88-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="84b88-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="84b88-114">위의 방법으로 Azure의 "testRG" 리소스 그룹에 있는 서쪽의 가상 WAN 인 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="84b88-115">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 가상 WAN에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="84b88-116">그런 다음 New-AzureRmVpnConnection 명령을 사용 하 여이 분기와 VpnGateway IPSec 연결을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzureRmVpnConnection command.</span></span>

## <span data-ttu-id="84b88-117">변수</span><span class="sxs-lookup"><span data-stu-id="84b88-117">PARAMETERS</span></span>

### <span data-ttu-id="84b88-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="84b88-118">-AddressSpace</span></span>
<span data-ttu-id="84b88-119">가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="84b88-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84b88-120">-AsJob</span></span>
<span data-ttu-id="84b88-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="84b88-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84b88-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="84b88-122">-BgpAsn</span></span>
<span data-ttu-id="84b88-123">이 VpnSite의 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="84b88-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="84b88-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="84b88-125">이 VpnSite의 BGP 피어 링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="84b88-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="84b88-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="84b88-127">이 VpnSite의 BGP 피어 링 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="84b88-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b88-128">-DefaultProfile</span></span>
<span data-ttu-id="84b88-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84b88-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="84b88-130">-DeviceModel</span></span>
<span data-ttu-id="84b88-131">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="84b88-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="84b88-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="84b88-132">-DeviceVendor</span></span>
<span data-ttu-id="84b88-133">원격 vpn 장치의 장치 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="84b88-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="84b88-134">-IpAddress</span></span>
<span data-ttu-id="84b88-135">이 VpnSite의 IPAddress입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="84b88-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="84b88-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="84b88-137">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="84b88-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="84b88-138">-위치</span><span class="sxs-lookup"><span data-stu-id="84b88-138">-Location</span></span>
<span data-ttu-id="84b88-139">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-139">The resource location.</span></span>

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

### <span data-ttu-id="84b88-140">-이름</span><span class="sxs-lookup"><span data-stu-id="84b88-140">-Name</span></span>
<span data-ttu-id="84b88-141">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-141">The resource name.</span></span>

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

### <span data-ttu-id="84b88-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b88-142">-ResourceGroupName</span></span>
<span data-ttu-id="84b88-143">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-143">The resource name.</span></span>

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

### <span data-ttu-id="84b88-144">태그</span><span class="sxs-lookup"><span data-stu-id="84b88-144">-Tag</span></span>
<span data-ttu-id="84b88-145">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="84b88-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="84b88-146">-VirtualWan</span></span>
<span data-ttu-id="84b88-147">이 VpnSite에 연결 해야 하는 VirtualWan입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b88-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="84b88-148">-VirtualWanId</span></span>
<span data-ttu-id="84b88-149">이 VpnSite에 연결 되어야 하는 ResourceId VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="84b88-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b88-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="84b88-150">-VirtualWanName</span></span>
<span data-ttu-id="84b88-151">이 VpnSite에 연결 해야 하는 VirtualWan의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b88-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b88-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="84b88-153">이 VpnSite에 연결 되어야 하는 VirtualWan의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b88-154">-확인</span><span class="sxs-lookup"><span data-stu-id="84b88-154">-Confirm</span></span>
<span data-ttu-id="84b88-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84b88-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b88-156">-WhatIf</span></span>
<span data-ttu-id="84b88-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84b88-158">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84b88-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b88-159">CommonParameters</span></span>
<span data-ttu-id="84b88-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84b88-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b88-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b88-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b88-162">입력</span><span class="sxs-lookup"><span data-stu-id="84b88-162">INPUTS</span></span>

### <span data-ttu-id="84b88-163">않아야</span><span class="sxs-lookup"><span data-stu-id="84b88-163">None</span></span>

## <span data-ttu-id="84b88-164">출력</span><span class="sxs-lookup"><span data-stu-id="84b88-164">OUTPUTS</span></span>

### <span data-ttu-id="84b88-165">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="84b88-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="84b88-166">상속자</span><span class="sxs-lookup"><span data-stu-id="84b88-166">NOTES</span></span>

## <span data-ttu-id="84b88-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84b88-167">RELATED LINKS</span></span>
