---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 825090358ea94223d483fe418d06896f1f741045
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385162"
---
# <span data-ttu-id="0ff42-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="0ff42-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="0ff42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ff42-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff42-103">VpnConnection을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="0ff42-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ff42-104">SYNTAX</span></span>

### <span data-ttu-id="0ff42-105">ByVpnConnectionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="0ff42-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff42-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="0ff42-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff42-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="0ff42-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ff42-108">설명</span><span class="sxs-lookup"><span data-stu-id="0ff42-108">DESCRIPTION</span></span>
<span data-ttu-id="0ff42-109">VpnConnection을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="0ff42-110">예제</span><span class="sxs-lookup"><span data-stu-id="0ff42-110">EXAMPLES</span></span>

### <span data-ttu-id="0ff42-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0ff42-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="0ff42-112">위의 경우 Azure의 "testRG" 리소스 그룹에 미국 서부에 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub 및 VpnSite가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="0ff42-113">VPN Gateway는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="0ff42-114">게이트웨이를 만든 후 New-AzVpnConnection 명령을 사용하여 VpnSite에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="0ff42-115">그런 다음 연결 이름을 사용하여 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="0ff42-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="0ff42-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="0ff42-117">예제 1과 동일하지만 이제 Get-AzVpnConnection에서 파이프된 개체를 사용하여 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="0ff42-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ff42-118">PARAMETERS</span></span>

### <span data-ttu-id="0ff42-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff42-119">-DefaultProfile</span></span>
<span data-ttu-id="0ff42-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ff42-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0ff42-121">-Force</span></span>
<span data-ttu-id="0ff42-122">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0ff42-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ff42-123">-InputObject</span></span>
<span data-ttu-id="0ff42-124">업데이트할 VpnConnection 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-124">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff42-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0ff42-125">-Name</span></span>
<span data-ttu-id="0ff42-126">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff42-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="0ff42-127">-ParentResourceName</span></span>
<span data-ttu-id="0ff42-128">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff42-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ff42-129">-PassThru</span></span>
<span data-ttu-id="0ff42-130">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0ff42-131">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0ff42-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff42-132">-ResourceGroupName</span></span>
<span data-ttu-id="0ff42-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff42-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ff42-134">-ResourceId</span></span>
<span data-ttu-id="0ff42-135">삭제할 VpnConnection 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-135">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff42-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ff42-136">-Confirm</span></span>
<span data-ttu-id="0ff42-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff42-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff42-138">-WhatIf</span></span>
<span data-ttu-id="0ff42-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0ff42-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ff42-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff42-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff42-141">CommonParameters</span></span>
<span data-ttu-id="0ff42-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff42-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff42-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0ff42-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff42-144">입력</span><span class="sxs-lookup"><span data-stu-id="0ff42-144">INPUTS</span></span>

### <span data-ttu-id="0ff42-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0ff42-145">System.String</span></span>

### <span data-ttu-id="0ff42-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="0ff42-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="0ff42-147">출력</span><span class="sxs-lookup"><span data-stu-id="0ff42-147">OUTPUTS</span></span>

### <span data-ttu-id="0ff42-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0ff42-148">System.Boolean</span></span>

## <span data-ttu-id="0ff42-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ff42-149">NOTES</span></span>

## <span data-ttu-id="0ff42-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ff42-150">RELATED LINKS</span></span>

[<span data-ttu-id="0ff42-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="0ff42-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="0ff42-152">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="0ff42-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="0ff42-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="0ff42-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
