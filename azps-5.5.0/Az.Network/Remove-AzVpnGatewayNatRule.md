---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
ms.openlocfilehash: 35a59b24297efe3fd94a66d19a778913f488b800
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179401"
---
# <span data-ttu-id="ec02b-101">Remove-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="ec02b-101">Remove-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="ec02b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec02b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec02b-103">VpnGateway와 연결된 NAT 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-103">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="ec02b-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec02b-104">SYNTAX</span></span>

### <span data-ttu-id="ec02b-105">ByVpnGatewayNatRuleName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ec02b-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec02b-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="ec02b-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec02b-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="ec02b-107">ByVpnGatewayNatRuleObject</span></span>
```
Remove-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec02b-108">설명</span><span class="sxs-lookup"><span data-stu-id="ec02b-108">DESCRIPTION</span></span>
<span data-ttu-id="ec02b-109">VpnGateway와 연결된 NAT 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-109">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="ec02b-110">예제</span><span class="sxs-lookup"><span data-stu-id="ec02b-110">EXAMPLES</span></span>

### <span data-ttu-id="ec02b-111">Example1</span><span class="sxs-lookup"><span data-stu-id="ec02b-111">Example1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Remove-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"
```

<span data-ttu-id="ec02b-112">위의 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub, VpnGateway 및 해당 VpnGateway와 연결된 NAT 규칙을 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub,VpnGateway and NAT rule associated with that VpnGateway.</span></span>
<span data-ttu-id="ec02b-113">그런 다음 NAT 규칙 이름을 사용하여 NAT 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-113">Then it removes the NAT rule using the NAT rule name.</span></span>


## <span data-ttu-id="ec02b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec02b-114">PARAMETERS</span></span>

### <span data-ttu-id="ec02b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec02b-115">-DefaultProfile</span></span>
<span data-ttu-id="ec02b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec02b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ec02b-117">-Force</span></span>
<span data-ttu-id="ec02b-118">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-118">Do not ask for confirmation if you want to delete a resource</span></span>

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

### <span data-ttu-id="ec02b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec02b-119">-InputObject</span></span>
<span data-ttu-id="ec02b-120">업데이트할 VpnGatewayNatRule 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-120">The VpnGatewayNatRule object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule
Parameter Sets: ByVpnGatewayNatRuleObject
Aliases: VpnGatewayNatRule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec02b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ec02b-121">-Name</span></span>
<span data-ttu-id="ec02b-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec02b-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="ec02b-123">-ParentResourceName</span></span>
<span data-ttu-id="ec02b-124">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec02b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec02b-125">-PassThru</span></span>
<span data-ttu-id="ec02b-126">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="ec02b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec02b-127">-ResourceGroupName</span></span>
<span data-ttu-id="ec02b-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec02b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec02b-129">-ResourceId</span></span>
<span data-ttu-id="ec02b-130">삭제할 VpnGatewayNatRule 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-130">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec02b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec02b-131">-Confirm</span></span>
<span data-ttu-id="ec02b-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec02b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec02b-133">-WhatIf</span></span>
<span data-ttu-id="ec02b-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ec02b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec02b-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec02b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec02b-136">CommonParameters</span></span>
<span data-ttu-id="ec02b-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec02b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec02b-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec02b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec02b-139">입력</span><span class="sxs-lookup"><span data-stu-id="ec02b-139">INPUTS</span></span>

### <span data-ttu-id="ec02b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ec02b-140">System.String</span></span>

### <span data-ttu-id="ec02b-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="ec02b-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="ec02b-142">출력</span><span class="sxs-lookup"><span data-stu-id="ec02b-142">OUTPUTS</span></span>

### <span data-ttu-id="ec02b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ec02b-143">System.Boolean</span></span>

## <span data-ttu-id="ec02b-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec02b-144">NOTES</span></span>

## <span data-ttu-id="ec02b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec02b-145">RELATED LINKS</span></span>
