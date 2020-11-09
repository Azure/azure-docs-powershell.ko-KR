---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 1e13cad885d18d8c15a033ae85b340041107cdc0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309457"
---
# <span data-ttu-id="c68e8-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c68e8-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="c68e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c68e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c68e8-103">Remove-AzVpnGateway cmdlet은 Azure VPN 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="c68e8-104">Azure 가상 WAN의 소프트웨어 정의 연결과 관련 된 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="c68e8-105">구문과</span><span class="sxs-lookup"><span data-stu-id="c68e8-105">SYNTAX</span></span>

### <span data-ttu-id="c68e8-106">ByVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c68e8-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c68e8-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c68e8-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c68e8-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c68e8-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c68e8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c68e8-109">DESCRIPTION</span></span>
<span data-ttu-id="c68e8-110">Remove-AzVpnGateway cmdlet은 Azure VPN 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="c68e8-111">Azure 가상 WAN의 소프트웨어 정의 연결과 관련 된 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="c68e8-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c68e8-112">EXAMPLES</span></span>

### <span data-ttu-id="c68e8-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="c68e8-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="c68e8-114">이 예제에서는 중앙 US에 리소스 그룹, 가상 WAN, 가상 허브, 확장 가능한 VPN 게이트웨이를 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="c68e8-115">가상 게이트웨이를 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="c68e8-116">VpnGateway 및이에 연결 된 모든 VpnConnections 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="c68e8-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="c68e8-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="c68e8-118">이 예제에서는 중앙 US에 리소스 그룹, 가상 WAN, 가상 허브, 확장 가능한 VPN 게이트웨이를 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="c68e8-119">이 삭제는 Get-AzVpnGateway 명령으로 반환 된 VpnGateway 개체를 사용 하는 powershell 파이핑을 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="c68e8-120">가상 게이트웨이를 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="c68e8-121">VpnGateway 및이에 연결 된 모든 VpnConnections 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="c68e8-122">변수</span><span class="sxs-lookup"><span data-stu-id="c68e8-122">PARAMETERS</span></span>

### <span data-ttu-id="c68e8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68e8-123">-DefaultProfile</span></span>
<span data-ttu-id="c68e8-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c68e8-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c68e8-125">-Force</span></span>
<span data-ttu-id="c68e8-126">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c68e8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c68e8-127">-InputObject</span></span>
<span data-ttu-id="c68e8-128">삭제할 vpnGateway 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="c68e8-129">-이름</span><span class="sxs-lookup"><span data-stu-id="c68e8-129">-Name</span></span>
<span data-ttu-id="c68e8-130">VpnGateway 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-130">The vpnGateway name.</span></span>

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

### <span data-ttu-id="c68e8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c68e8-131">-PassThru</span></span>
<span data-ttu-id="c68e8-132">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c68e8-133">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c68e8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c68e8-134">-ResourceGroupName</span></span>
<span data-ttu-id="c68e8-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-135">The resource group name.</span></span>

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

### <span data-ttu-id="c68e8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c68e8-136">-ResourceId</span></span>
<span data-ttu-id="c68e8-137">삭제할 vpnGateway의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="c68e8-138">-확인</span><span class="sxs-lookup"><span data-stu-id="c68e8-138">-Confirm</span></span>
<span data-ttu-id="c68e8-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c68e8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c68e8-140">-WhatIf</span></span>
<span data-ttu-id="c68e8-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c68e8-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c68e8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68e8-143">CommonParameters</span></span>
<span data-ttu-id="c68e8-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c68e8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68e8-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c68e8-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68e8-146">입력</span><span class="sxs-lookup"><span data-stu-id="c68e8-146">INPUTS</span></span>

### <span data-ttu-id="c68e8-147">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c68e8-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="c68e8-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c68e8-148">System.String</span></span>

## <span data-ttu-id="c68e8-149">출력</span><span class="sxs-lookup"><span data-stu-id="c68e8-149">OUTPUTS</span></span>

### <span data-ttu-id="c68e8-150">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c68e8-150">System.Boolean</span></span>

## <span data-ttu-id="c68e8-151">상속자</span><span class="sxs-lookup"><span data-stu-id="c68e8-151">NOTES</span></span>

## <span data-ttu-id="c68e8-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c68e8-152">RELATED LINKS</span></span>

[<span data-ttu-id="c68e8-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c68e8-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="c68e8-154">새로운 AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c68e8-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="c68e8-155">업데이트-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c68e8-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
