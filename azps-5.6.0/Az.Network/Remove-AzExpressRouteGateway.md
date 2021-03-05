---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 77c41a4565a517a51b02c904d79953d79e908c39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996394"
---
# <span data-ttu-id="d603b-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d603b-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="d603b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d603b-102">SYNOPSIS</span></span>
<span data-ttu-id="d603b-103">Remove-AzExpressRouteGateway cmdlet은 Azure ExpressRoute 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="d603b-104">Azure Virtual WAN의 소프트웨어 정의 연결과 관련이 있는 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="d603b-105">구문</span><span class="sxs-lookup"><span data-stu-id="d603b-105">SYNTAX</span></span>

### <span data-ttu-id="d603b-106">ByExpressRouteGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d603b-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d603b-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d603b-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d603b-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d603b-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d603b-109">설명</span><span class="sxs-lookup"><span data-stu-id="d603b-109">DESCRIPTION</span></span>
<span data-ttu-id="d603b-110">Remove-AzExpressRouteGateway cmdlet은 Azure ExpressRoute 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="d603b-111">Azure Virtual WAN의 소프트웨어 정의 연결과 관련이 있는 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="d603b-112">예제</span><span class="sxs-lookup"><span data-stu-id="d603b-112">EXAMPLES</span></span>

### <span data-ttu-id="d603b-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="d603b-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="d603b-114">이 예제에서는 리소스 그룹, Virtual WAN, Virtual Hub, 확장 가능한 ExpressRoute 게이트웨이를 미국 중부에 만들고 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="d603b-115">Virtual Gateway를 삭제할 때 프롬프트를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="d603b-116">그러면 ExpressRouteGateway 및 연결된 모든 ExpressRouteConnections가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="d603b-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="d603b-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="d603b-118">이 예제에서는 리소스 그룹, Virtual WAN, Virtual Hub, 확장 가능한 ExpressRoute 게이트웨이를 미국 중서부에 만들고 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="d603b-119">이 삭제는 powershell 배관을 사용하여 발생합니다. 이 Get-AzExpressRouteGateway 반환된 ExpressRouteGateway 개체를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="d603b-120">Virtual Gateway를 삭제할 때 프롬프트를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="d603b-121">그러면 ExpressRouteGateway 및 연결된 모든 ExpressRouteConnections가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="d603b-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d603b-122">PARAMETERS</span></span>

### <span data-ttu-id="d603b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d603b-123">-DefaultProfile</span></span>
<span data-ttu-id="d603b-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d603b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d603b-125">-Force</span></span>
<span data-ttu-id="d603b-126">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d603b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d603b-127">-InputObject</span></span>
<span data-ttu-id="d603b-128">삭제할 ExpressRouteGateway 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="d603b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d603b-129">-Name</span></span>
<span data-ttu-id="d603b-130">ExpressRouteGateway 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-130">The ExpressRouteGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d603b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d603b-131">-PassThru</span></span>
<span data-ttu-id="d603b-132">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d603b-133">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d603b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d603b-134">-ResourceGroupName</span></span>
<span data-ttu-id="d603b-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-135">The resource group name.</span></span>

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

### <span data-ttu-id="d603b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d603b-136">-ResourceId</span></span>
<span data-ttu-id="d603b-137">삭제할 ExpressRouteGateway에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d603b-138">-확인</span><span class="sxs-lookup"><span data-stu-id="d603b-138">-Confirm</span></span>
<span data-ttu-id="d603b-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d603b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d603b-140">-WhatIf</span></span>
<span data-ttu-id="d603b-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d603b-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d603b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d603b-143">CommonParameters</span></span>
<span data-ttu-id="d603b-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d603b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d603b-145">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d603b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d603b-146">입력</span><span class="sxs-lookup"><span data-stu-id="d603b-146">INPUTS</span></span>

### <span data-ttu-id="d603b-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d603b-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="d603b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d603b-148">System.String</span></span>

## <span data-ttu-id="d603b-149">출력</span><span class="sxs-lookup"><span data-stu-id="d603b-149">OUTPUTS</span></span>

### <span data-ttu-id="d603b-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d603b-150">System.Boolean</span></span>

## <span data-ttu-id="d603b-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d603b-151">NOTES</span></span>

## <span data-ttu-id="d603b-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d603b-152">RELATED LINKS</span></span>
