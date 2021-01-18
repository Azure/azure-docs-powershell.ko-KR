---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 1e13cad885d18d8c15a033ae85b340041107cdc0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496575"
---
# <span data-ttu-id="59efd-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="59efd-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="59efd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59efd-102">SYNOPSIS</span></span>
<span data-ttu-id="59efd-103">Remove-AzVpnGateway cmdlet은 Azure VPN Gateway를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="59efd-104">Azure Virtual WAN의 소프트웨어 정의 연결에 특정한 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="59efd-105">구문</span><span class="sxs-lookup"><span data-stu-id="59efd-105">SYNTAX</span></span>

### <span data-ttu-id="59efd-106">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="59efd-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59efd-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="59efd-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59efd-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="59efd-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59efd-109">설명</span><span class="sxs-lookup"><span data-stu-id="59efd-109">DESCRIPTION</span></span>
<span data-ttu-id="59efd-110">Remove-AzVpnGateway cmdlet은 Azure VPN Gateway를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="59efd-111">Azure Virtual WAN의 소프트웨어 정의 연결에 특정한 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="59efd-112">예제</span><span class="sxs-lookup"><span data-stu-id="59efd-112">EXAMPLES</span></span>

### <span data-ttu-id="59efd-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="59efd-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="59efd-114">이 예제에서는 리소스 그룹, Virtual WAN, Virtual Hub, 미국 중부에 확장 가능한 VPN Gateway를 만든 다음 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="59efd-115">Virtual Gateway를 삭제하는 경우 프롬프트를 표시하지 않습니다. -Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="59efd-116">그러면 VpnGateway 및 연결된 모든 VpnConnections가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="59efd-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="59efd-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="59efd-118">이 예제에서는 리소스 그룹, Virtual WAN, Virtual Hub, 미국 중부에 확장 가능한 VPN Gateway를 만든 다음 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="59efd-119">이 삭제는 Get-AzVpnGateway 명령에서 반환된 VpnGateway 개체를 사용하는 powershell 파이핑을 사용하여 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="59efd-120">Virtual Gateway를 삭제하는 경우 프롬프트를 표시하지 않습니다. -Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="59efd-121">그러면 VpnGateway 및 연결된 모든 VpnConnections가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="59efd-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59efd-122">PARAMETERS</span></span>

### <span data-ttu-id="59efd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59efd-123">-DefaultProfile</span></span>
<span data-ttu-id="59efd-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59efd-125">-Force</span><span class="sxs-lookup"><span data-stu-id="59efd-125">-Force</span></span>
<span data-ttu-id="59efd-126">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="59efd-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59efd-127">-InputObject</span></span>
<span data-ttu-id="59efd-128">삭제할 vpnGateway 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59efd-129">-Name</span><span class="sxs-lookup"><span data-stu-id="59efd-129">-Name</span></span>
<span data-ttu-id="59efd-130">vpnGateway 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59efd-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59efd-131">-PassThru</span></span>
<span data-ttu-id="59efd-132">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59efd-133">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59efd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59efd-134">-ResourceGroupName</span></span>
<span data-ttu-id="59efd-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59efd-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59efd-136">-ResourceId</span></span>
<span data-ttu-id="59efd-137">삭제할 vpnGateway에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59efd-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59efd-138">-Confirm</span></span>
<span data-ttu-id="59efd-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59efd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59efd-140">-WhatIf</span></span>
<span data-ttu-id="59efd-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="59efd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59efd-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59efd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59efd-143">CommonParameters</span></span>
<span data-ttu-id="59efd-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="59efd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59efd-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="59efd-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59efd-146">입력</span><span class="sxs-lookup"><span data-stu-id="59efd-146">INPUTS</span></span>

### <span data-ttu-id="59efd-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="59efd-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="59efd-148">System.String</span><span class="sxs-lookup"><span data-stu-id="59efd-148">System.String</span></span>

## <span data-ttu-id="59efd-149">출력</span><span class="sxs-lookup"><span data-stu-id="59efd-149">OUTPUTS</span></span>

### <span data-ttu-id="59efd-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="59efd-150">System.Boolean</span></span>

## <span data-ttu-id="59efd-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="59efd-151">NOTES</span></span>

## <span data-ttu-id="59efd-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59efd-152">RELATED LINKS</span></span>

[<span data-ttu-id="59efd-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="59efd-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="59efd-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="59efd-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="59efd-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="59efd-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
