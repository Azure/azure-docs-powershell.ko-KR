---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: df81d3df31ad1d04914164d04321151e0df2dfdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974768"
---
# <span data-ttu-id="740f4-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="740f4-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="740f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="740f4-102">SYNOPSIS</span></span>
<span data-ttu-id="740f4-103">확장 가능한 ExpressRoute Gateway를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="740f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="740f4-104">SYNTAX</span></span>

### <span data-ttu-id="740f4-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="740f4-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="740f4-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="740f4-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="740f4-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="740f4-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="740f4-108">설명</span><span class="sxs-lookup"><span data-stu-id="740f4-108">DESCRIPTION</span></span>

<span data-ttu-id="740f4-109">New-AzExpressRouteGateway ExpressRoute Gateway를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="740f4-110">VirtualHub 내부에서 Azure에 대한 프레미스에 대한 소프트웨어 정의 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="740f4-111">이 게이트웨이는 이 또는 cmdlet에 지정된 확장 단위에 따라 Set-AzExpressRouteGateway 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="740f4-112">연결은 프레미스 ExpressRoute 회로에서 확장 가능한 게이트웨이로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="740f4-113">ExpressRouteGateway는 참조된 VirtualHub와 동일한 위치에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="740f4-114">예제</span><span class="sxs-lookup"><span data-stu-id="740f4-114">EXAMPLES</span></span>

### <span data-ttu-id="740f4-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="740f4-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="740f4-116">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 "testRG" 리소스 그룹에서 미국 서부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="740f4-117">2개 확장 단위가 있는 Virtual Hub에서 ExpressRoute 게이트웨이가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="740f4-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="740f4-118">PARAMETERS</span></span>

### <span data-ttu-id="740f4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="740f4-119">-AsJob</span></span>
<span data-ttu-id="740f4-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="740f4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="740f4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="740f4-121">-DefaultProfile</span></span>
<span data-ttu-id="740f4-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="740f4-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="740f4-123">-MaxScaleUnits</span></span>
<span data-ttu-id="740f4-124">이 ExpressRouteGateway의 최대 확장 단위 수입니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="740f4-125">유효한 범위 > 2</span><span class="sxs-lookup"><span data-stu-id="740f4-125">Valid range > 2</span></span>

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

### <span data-ttu-id="740f4-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="740f4-126">-MinScaleUnits</span></span>
<span data-ttu-id="740f4-127">이 ExpressRouteGateway의 최소 배율 단위 수입니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="740f4-128">유효한 범위 > 2</span><span class="sxs-lookup"><span data-stu-id="740f4-128">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="740f4-129">-Name</span><span class="sxs-lookup"><span data-stu-id="740f4-129">-Name</span></span>
<span data-ttu-id="740f4-130">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="740f4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="740f4-131">-ResourceGroupName</span></span>
<span data-ttu-id="740f4-132">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-132">The resource name.</span></span>

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

### <span data-ttu-id="740f4-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="740f4-133">-Tag</span></span>
<span data-ttu-id="740f4-134">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="740f4-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="740f4-135">-VirtualHub</span></span>
<span data-ttu-id="740f4-136">VirtualHub 이 VpnGateway를 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="740f4-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="740f4-137">-VirtualHubId</span></span>
<span data-ttu-id="740f4-138">VirtualHub 이 VpnGateway의 ID를 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="740f4-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="740f4-139">-VirtualHubName</span></span>
<span data-ttu-id="740f4-140">VirtualHub 이 VpnGateway의 ID를 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="740f4-141">-확인</span><span class="sxs-lookup"><span data-stu-id="740f4-141">-Confirm</span></span>
<span data-ttu-id="740f4-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="740f4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="740f4-143">-WhatIf</span></span>
<span data-ttu-id="740f4-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="740f4-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="740f4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="740f4-146">CommonParameters</span></span>
<span data-ttu-id="740f4-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="740f4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="740f4-148">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="740f4-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="740f4-149">입력</span><span class="sxs-lookup"><span data-stu-id="740f4-149">INPUTS</span></span>

### <span data-ttu-id="740f4-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="740f4-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="740f4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="740f4-151">System.String</span></span>

## <span data-ttu-id="740f4-152">출력</span><span class="sxs-lookup"><span data-stu-id="740f4-152">OUTPUTS</span></span>

### <span data-ttu-id="740f4-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="740f4-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="740f4-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="740f4-154">NOTES</span></span>

## <span data-ttu-id="740f4-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="740f4-155">RELATED LINKS</span></span>
