---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 980b84fd1b23cb7e4b034dee485b785b96893f11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700237"
---
# <span data-ttu-id="f5d03-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f5d03-101">New-AzVpnSite</span></span>

## <span data-ttu-id="f5d03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5d03-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d03-103">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="f5d03-104">이는 Cortex 가상 허브를 사용 하 여 S2S 연결을 위해 Azure에 업로드 되는 고객 분기에 대 한 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="f5d03-105">구문과</span><span class="sxs-lookup"><span data-stu-id="f5d03-105">SYNTAX</span></span>

### <span data-ttu-id="f5d03-106">ByVirtualWanName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f5d03-106">ByVirtualWanName (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5d03-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="f5d03-107">ByVirtualWanObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5d03-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="f5d03-108">ByVirtualWanResourceId</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5d03-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f5d03-109">DESCRIPTION</span></span>
<span data-ttu-id="f5d03-110">새 Azure VpnSite 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="f5d03-111">이는 Cortex 가상 허브를 사용 하 여 S2S 연결을 위해 Azure에 업로드 되는 고객 분기에 대 한 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="f5d03-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f5d03-112">EXAMPLES</span></span>

### <span data-ttu-id="f5d03-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5d03-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

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

<span data-ttu-id="f5d03-114">위의 방법으로 Azure의 "testRG" 리소스 그룹에 있는 서쪽의 가상 WAN 인 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="f5d03-115">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 가상 WAN에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="f5d03-116">그런 다음 New-AzVpnConnection 명령을 사용 하 여이 분기와 VpnGateway IPSec 연결을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="f5d03-117">변수</span><span class="sxs-lookup"><span data-stu-id="f5d03-117">PARAMETERS</span></span>

### <span data-ttu-id="f5d03-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="f5d03-118">-AddressSpace</span></span>
<span data-ttu-id="f5d03-119">가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="f5d03-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5d03-120">-AsJob</span></span>
<span data-ttu-id="f5d03-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f5d03-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5d03-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="f5d03-122">-BgpAsn</span></span>
<span data-ttu-id="f5d03-123">이 VpnSite의 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="f5d03-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="f5d03-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="f5d03-125">이 VpnSite의 BGP 피어 링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="f5d03-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="f5d03-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="f5d03-127">이 VpnSite의 BGP 피어 링 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="f5d03-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d03-128">-DefaultProfile</span></span>
<span data-ttu-id="f5d03-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5d03-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="f5d03-130">-DeviceModel</span></span>
<span data-ttu-id="f5d03-131">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="f5d03-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="f5d03-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="f5d03-132">-DeviceVendor</span></span>
<span data-ttu-id="f5d03-133">원격 vpn 장치의 장치 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="f5d03-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="f5d03-134">-IpAddress</span></span>
<span data-ttu-id="f5d03-135">이 VpnSite의 IPAddress입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="f5d03-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="f5d03-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="f5d03-137">원격 vpn 장치의 장치 모델</span><span class="sxs-lookup"><span data-stu-id="f5d03-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="f5d03-138">-위치</span><span class="sxs-lookup"><span data-stu-id="f5d03-138">-Location</span></span>
<span data-ttu-id="f5d03-139">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-139">The resource location.</span></span>

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

### <span data-ttu-id="f5d03-140">-이름</span><span class="sxs-lookup"><span data-stu-id="f5d03-140">-Name</span></span>
<span data-ttu-id="f5d03-141">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-141">The resource name.</span></span>

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

### <span data-ttu-id="f5d03-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5d03-142">-ResourceGroupName</span></span>
<span data-ttu-id="f5d03-143">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-143">The resource name.</span></span>

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

### <span data-ttu-id="f5d03-144">태그</span><span class="sxs-lookup"><span data-stu-id="f5d03-144">-Tag</span></span>
<span data-ttu-id="f5d03-145">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f5d03-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="f5d03-146">-VirtualWan</span></span>
<span data-ttu-id="f5d03-147">이 VpnSite에 연결 해야 하는 VirtualWan입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="f5d03-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="f5d03-148">-VirtualWanId</span></span>
<span data-ttu-id="f5d03-149">이 VpnSite에 연결 되어야 하는 ResourceId VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f5d03-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="f5d03-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="f5d03-150">-VirtualWanName</span></span>
<span data-ttu-id="f5d03-151">이 VpnSite에 연결 해야 하는 VirtualWan의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="f5d03-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5d03-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="f5d03-153">이 VpnSite에 연결 되어야 하는 VirtualWan의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="f5d03-154">-확인</span><span class="sxs-lookup"><span data-stu-id="f5d03-154">-Confirm</span></span>
<span data-ttu-id="f5d03-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5d03-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5d03-156">-WhatIf</span></span>
<span data-ttu-id="f5d03-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5d03-158">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5d03-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d03-159">CommonParameters</span></span>
<span data-ttu-id="f5d03-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d03-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d03-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5d03-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d03-162">입력</span><span class="sxs-lookup"><span data-stu-id="f5d03-162">INPUTS</span></span>

### <span data-ttu-id="f5d03-163">않아야</span><span class="sxs-lookup"><span data-stu-id="f5d03-163">None</span></span>

## <span data-ttu-id="f5d03-164">출력</span><span class="sxs-lookup"><span data-stu-id="f5d03-164">OUTPUTS</span></span>

### <span data-ttu-id="f5d03-165">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f5d03-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="f5d03-166">상속자</span><span class="sxs-lookup"><span data-stu-id="f5d03-166">NOTES</span></span>

## <span data-ttu-id="f5d03-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5d03-167">RELATED LINKS</span></span>

[<span data-ttu-id="f5d03-168">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f5d03-168">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="f5d03-169">제거-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f5d03-169">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="f5d03-170">업데이트-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f5d03-170">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
