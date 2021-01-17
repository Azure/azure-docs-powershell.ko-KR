---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: bd800f362a1a5fb66968e0f75b1211b2f0bbdf72
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339950"
---
# <span data-ttu-id="7a8b4-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7a8b4-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="7a8b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8b4-103">확장 가능한 ExpressRoute 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="7a8b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a8b4-104">SYNTAX</span></span>

### <span data-ttu-id="7a8b4-105">ByExpressRouteGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a8b4-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a8b4-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7a8b4-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a8b4-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7a8b4-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a8b4-108">설명</span><span class="sxs-lookup"><span data-stu-id="7a8b4-108">DESCRIPTION</span></span>

<span data-ttu-id="7a8b4-109">**Set-AzExpressRouteGateway** cmdlet을 사용하면 기존 ExpressRouteGateway의 배율 단위를 업데이트하거나 리소스 태그를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="7a8b4-110">예제</span><span class="sxs-lookup"><span data-stu-id="7a8b4-110">EXAMPLES</span></span>

### <span data-ttu-id="7a8b4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a8b4-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="7a8b4-112">위의 리소스 그룹인 Virtual WAN, Virtual Network, Azure의 "testRG" 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7a8b4-113">ExpressRoute 게이트웨이는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어지며 3개 배율 단위로 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="7a8b4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a8b4-114">PARAMETERS</span></span>

### <span data-ttu-id="7a8b4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a8b4-115">-AsJob</span></span>
<span data-ttu-id="7a8b4-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7a8b4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a8b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a8b4-117">-DefaultProfile</span></span>
<span data-ttu-id="7a8b4-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a8b4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a8b4-119">-InputObject</span></span>
<span data-ttu-id="7a8b4-120">업데이트해야 하는 ExpressRouteGateway입니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-120">The ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b4-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="7a8b4-121">-MaxScaleUnits</span></span>
<span data-ttu-id="7a8b4-122">이 ExpressRouteGateway의 최대 배율 단위 수입니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="7a8b4-123">유효한 범위 > 2</span><span class="sxs-lookup"><span data-stu-id="7a8b4-123">Valid range > 2</span></span>

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

### <span data-ttu-id="7a8b4-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="7a8b4-124">-MinScaleUnits</span></span>
<span data-ttu-id="7a8b4-125">이 ExpressRouteGateway의 최소 배율 단위 수입니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="7a8b4-126">유효한 범위 > 2</span><span class="sxs-lookup"><span data-stu-id="7a8b4-126">Valid range > 2</span></span>

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

### <span data-ttu-id="7a8b4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="7a8b4-127">-Name</span></span>
<span data-ttu-id="7a8b4-128">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a8b4-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a8b4-130">업데이트할 ExpressRouteGateway의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a8b4-131">-ResourceId</span></span>
<span data-ttu-id="7a8b4-132">업데이트해야 하는 ExpressRouteGateway의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b4-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="7a8b4-133">-Tag</span></span>
<span data-ttu-id="7a8b4-134">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7a8b4-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a8b4-135">-Confirm</span></span>
<span data-ttu-id="7a8b4-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a8b4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a8b4-137">-WhatIf</span></span>
<span data-ttu-id="7a8b4-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7a8b4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a8b4-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a8b4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8b4-140">CommonParameters</span></span>
<span data-ttu-id="7a8b4-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8b4-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8b4-143">입력</span><span class="sxs-lookup"><span data-stu-id="7a8b4-143">INPUTS</span></span>

### <span data-ttu-id="7a8b4-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7a8b4-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="7a8b4-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7a8b4-145">System.String</span></span>

## <span data-ttu-id="7a8b4-146">출력</span><span class="sxs-lookup"><span data-stu-id="7a8b4-146">OUTPUTS</span></span>

### <span data-ttu-id="7a8b4-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7a8b4-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="7a8b4-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a8b4-148">NOTES</span></span>

## <span data-ttu-id="7a8b4-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a8b4-149">RELATED LINKS</span></span>
