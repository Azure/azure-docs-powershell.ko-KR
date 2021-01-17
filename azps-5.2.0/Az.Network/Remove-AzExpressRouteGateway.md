---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362223"
---
# <span data-ttu-id="16735-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="16735-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="16735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16735-102">SYNOPSIS</span></span>
<span data-ttu-id="16735-103">Remove-AzExpressRouteGateway cmdlet은 Azure ExpressRoute 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16735-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="16735-104">Azure Virtual WAN의 소프트웨어 정의 연결에 특정한 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="16735-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="16735-105">구문</span><span class="sxs-lookup"><span data-stu-id="16735-105">SYNTAX</span></span>

### <span data-ttu-id="16735-106">ByExpressRouteGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="16735-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16735-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="16735-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16735-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="16735-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16735-109">설명</span><span class="sxs-lookup"><span data-stu-id="16735-109">DESCRIPTION</span></span>
<span data-ttu-id="16735-110">Remove-AzExpressRouteGateway cmdlet은 Azure ExpressRoute 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16735-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="16735-111">Azure Virtual WAN의 소프트웨어 정의 연결에 특정한 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="16735-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="16735-112">예제</span><span class="sxs-lookup"><span data-stu-id="16735-112">EXAMPLES</span></span>

### <span data-ttu-id="16735-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="16735-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="16735-114">이 예제에서는 리소스 그룹, Virtual WAN, Virtual Hub, 미국 중부에 확장 가능한 ExpressRoute 게이트웨이를 만든 다음 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="16735-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="16735-115">Virtual Gateway를 삭제하는 경우 프롬프트를 표시하지 않습니다. -Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16735-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="16735-116">그러면 ExpressRouteGateway 및 연결된 모든 ExpressRouteConnections가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="16735-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="16735-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="16735-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="16735-118">이 예제에서는 리소스 그룹, Virtual WAN, Virtual Hub, 확장 가능한 ExpressRoute 게이트웨이를 미국 중서부에 만든 다음 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="16735-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="16735-119">이 삭제는 명령에서 반환된 ExpressRouteGateway 개체를 사용하는 powershell 파이핑을 Get-AzExpressRouteGateway 합니다.</span><span class="sxs-lookup"><span data-stu-id="16735-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="16735-120">Virtual Gateway를 삭제하는 경우 프롬프트를 표시하지 않습니다. -Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16735-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="16735-121">그러면 ExpressRouteGateway 및 연결된 모든 ExpressRouteConnections가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="16735-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="16735-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16735-122">PARAMETERS</span></span>

### <span data-ttu-id="16735-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16735-123">-DefaultProfile</span></span>
<span data-ttu-id="16735-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16735-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16735-125">-Force</span><span class="sxs-lookup"><span data-stu-id="16735-125">-Force</span></span>
<span data-ttu-id="16735-126">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16735-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="16735-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16735-127">-InputObject</span></span>
<span data-ttu-id="16735-128">삭제할 ExpressRouteGateway 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="16735-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="16735-129">-Name</span><span class="sxs-lookup"><span data-stu-id="16735-129">-Name</span></span>
<span data-ttu-id="16735-130">ExpressRouteGateway 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16735-130">The ExpressRouteGateway name.</span></span>

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

### <span data-ttu-id="16735-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16735-131">-PassThru</span></span>
<span data-ttu-id="16735-132">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="16735-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="16735-133">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16735-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="16735-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16735-134">-ResourceGroupName</span></span>
<span data-ttu-id="16735-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16735-135">The resource group name.</span></span>

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

### <span data-ttu-id="16735-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16735-136">-ResourceId</span></span>
<span data-ttu-id="16735-137">삭제할 ExpressRouteGateway에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="16735-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="16735-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16735-138">-Confirm</span></span>
<span data-ttu-id="16735-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16735-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16735-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16735-140">-WhatIf</span></span>
<span data-ttu-id="16735-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="16735-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16735-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16735-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16735-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16735-143">CommonParameters</span></span>
<span data-ttu-id="16735-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16735-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16735-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="16735-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16735-146">입력</span><span class="sxs-lookup"><span data-stu-id="16735-146">INPUTS</span></span>

### <span data-ttu-id="16735-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="16735-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="16735-148">System.String</span><span class="sxs-lookup"><span data-stu-id="16735-148">System.String</span></span>

## <span data-ttu-id="16735-149">출력</span><span class="sxs-lookup"><span data-stu-id="16735-149">OUTPUTS</span></span>

### <span data-ttu-id="16735-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16735-150">System.Boolean</span></span>

## <span data-ttu-id="16735-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16735-151">NOTES</span></span>

## <span data-ttu-id="16735-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16735-152">RELATED LINKS</span></span>
