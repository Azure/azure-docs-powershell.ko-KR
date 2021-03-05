---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: faa634facf6baa8d0d55490ec32a9395feaea5db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963984"
---
# <span data-ttu-id="3dd39-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="3dd39-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="3dd39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dd39-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd39-103">확장 가능한 ExpressRoute Gateway를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="3dd39-104">구문</span><span class="sxs-lookup"><span data-stu-id="3dd39-104">SYNTAX</span></span>

### <span data-ttu-id="3dd39-105">ByExpressRouteGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="3dd39-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dd39-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="3dd39-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3dd39-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="3dd39-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3dd39-108">설명</span><span class="sxs-lookup"><span data-stu-id="3dd39-108">DESCRIPTION</span></span>

<span data-ttu-id="3dd39-109">**Set-AzExpressRouteGateway** cmdlet을 사용하면 기존 ExpressRouteGateway의 확장 단위를 업데이트하거나 리소스 태그를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="3dd39-110">예제</span><span class="sxs-lookup"><span data-stu-id="3dd39-110">EXAMPLES</span></span>

### <span data-ttu-id="3dd39-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3dd39-111">Example 1</span></span>

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

<span data-ttu-id="3dd39-112">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 "testRG" 리소스 그룹에서 미국 서부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="3dd39-113">이 후 Virtual Hub에서 2개 확장 단위가 있는 ExpressRoute 게이트웨이가 생성됩니다. 그런 다음 3개 확장 단위로 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="3dd39-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3dd39-114">PARAMETERS</span></span>

### <span data-ttu-id="3dd39-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dd39-115">-AsJob</span></span>
<span data-ttu-id="3dd39-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3dd39-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dd39-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd39-117">-DefaultProfile</span></span>
<span data-ttu-id="3dd39-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dd39-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dd39-119">-InputObject</span></span>
<span data-ttu-id="3dd39-120">업데이트해야 하는 ExpressRouteGateway입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="3dd39-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="3dd39-121">-MaxScaleUnits</span></span>
<span data-ttu-id="3dd39-122">이 ExpressRouteGateway의 최대 확장 단위 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="3dd39-123">유효한 범위 > 2</span><span class="sxs-lookup"><span data-stu-id="3dd39-123">Valid range > 2</span></span>

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

### <span data-ttu-id="3dd39-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="3dd39-124">-MinScaleUnits</span></span>
<span data-ttu-id="3dd39-125">이 ExpressRouteGateway의 최소 배율 단위 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="3dd39-126">유효한 범위 > 2</span><span class="sxs-lookup"><span data-stu-id="3dd39-126">Valid range > 2</span></span>

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

### <span data-ttu-id="3dd39-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3dd39-127">-Name</span></span>
<span data-ttu-id="3dd39-128">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-128">The resource name.</span></span>

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

### <span data-ttu-id="3dd39-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dd39-129">-ResourceGroupName</span></span>
<span data-ttu-id="3dd39-130">업데이트할 ExpressRouteGateway의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="3dd39-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dd39-131">-ResourceId</span></span>
<span data-ttu-id="3dd39-132">업데이트해야 하는 ExpressRouteGateway의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="3dd39-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="3dd39-133">-Tag</span></span>
<span data-ttu-id="3dd39-134">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3dd39-135">-확인</span><span class="sxs-lookup"><span data-stu-id="3dd39-135">-Confirm</span></span>
<span data-ttu-id="3dd39-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dd39-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dd39-137">-WhatIf</span></span>
<span data-ttu-id="3dd39-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dd39-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dd39-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd39-140">CommonParameters</span></span>
<span data-ttu-id="3dd39-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3dd39-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd39-142">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3dd39-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd39-143">입력</span><span class="sxs-lookup"><span data-stu-id="3dd39-143">INPUTS</span></span>

### <span data-ttu-id="3dd39-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3dd39-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="3dd39-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3dd39-145">System.String</span></span>

## <span data-ttu-id="3dd39-146">출력</span><span class="sxs-lookup"><span data-stu-id="3dd39-146">OUTPUTS</span></span>

### <span data-ttu-id="3dd39-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="3dd39-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="3dd39-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3dd39-148">NOTES</span></span>

## <span data-ttu-id="3dd39-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3dd39-149">RELATED LINKS</span></span>
