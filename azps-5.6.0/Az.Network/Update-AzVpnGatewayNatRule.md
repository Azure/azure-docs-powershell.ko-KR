---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
ms.openlocfilehash: e0a2722a59a9ffe1b6a7c3fb401b4faca85a1650
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951451"
---
# <span data-ttu-id="c3b6c-101">Update-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="c3b6c-101">Update-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="c3b6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b6c-103">VpnGateway와 연결된 NAT 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-103">Updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="c3b6c-104">구문</span><span class="sxs-lookup"><span data-stu-id="c3b6c-104">SYNTAX</span></span>

### <span data-ttu-id="c3b6c-105">ByVpnGatewayNatRuleName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c3b6c-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Update-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>] [-ExternalMapping <String[]>]
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3b6c-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="c3b6c-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Update-AzVpnGatewayNatRule -ResourceId <String> [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>]
 [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3b6c-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="c3b6c-107">ByVpnGatewayNatRuleObject</span></span>
```
Update-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Type <String>] [-Mode <String>]
 [-InternalMapping <String[]>] [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3b6c-108">설명</span><span class="sxs-lookup"><span data-stu-id="c3b6c-108">DESCRIPTION</span></span>
<span data-ttu-id="c3b6c-109">**Update-AzVpnGatewayNatRule** cmdlet은 VpnGateway와 연결된 NAT 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-109">The **Update-AzVpnGatewayNatRule** cmdlet updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="c3b6c-110">예제</span><span class="sxs-lookup"><span data-stu-id="c3b6c-110">EXAMPLES</span></span>

### <span data-ttu-id="c3b6c-111">예제</span><span class="sxs-lookup"><span data-stu-id="c3b6c-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> $natRule = Update-AzVpnGatewayNatRule -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy
PS C:\> Update-AzVpnGatewayNatRule -InputObject $natRule -Type Dynamic -Mode IngressSnat

Type                      : Dynamic
Mode                      : IngressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule
```

<span data-ttu-id="c3b6c-112">위의 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="c3b6c-113">그런 다음 해당 Virtual Hub 아래에 VpnGateway를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="c3b6c-114">그런 다음, 만든 VpnGateway와 연결된 새 NAT 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-114">Then, create new NAT rule associated with created VpnGateway.</span></span>
<span data-ttu-id="c3b6c-115">이 명령을 사용하여 Update-AzVpnGatewayNatRule, NAT 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-115">Using this command: Update-AzVpnGatewayNatRule, update NAT rule.</span></span>

## <span data-ttu-id="c3b6c-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c3b6c-116">PARAMETERS</span></span>

### <span data-ttu-id="c3b6c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3b6c-117">-AsJob</span></span>
<span data-ttu-id="c3b6c-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c3b6c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3b6c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b6c-119">-DefaultProfile</span></span>
<span data-ttu-id="c3b6c-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3b6c-121">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="c3b6c-121">-ExternalMapping</span></span>
<span data-ttu-id="c3b6c-122">NAT에 대한 개인 IP 주소 서브넷 외부 매핑 목록</span><span class="sxs-lookup"><span data-stu-id="c3b6c-122">The list of private IP address subnet external mappings for NAT</span></span>

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

### <span data-ttu-id="c3b6c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3b6c-123">-InputObject</span></span>
<span data-ttu-id="c3b6c-124">업데이트할 VpnGatewayNatRule 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-124">The VpnGatewayNatRule object to update.</span></span>

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

### <span data-ttu-id="c3b6c-125">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="c3b6c-125">-InternalMapping</span></span>
<span data-ttu-id="c3b6c-126">NAT에 대한 개인 IP 주소 서브넷 내부 매핑 목록</span><span class="sxs-lookup"><span data-stu-id="c3b6c-126">The list of private IP address subnet internal mappings for NAT</span></span>

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

### <span data-ttu-id="c3b6c-127">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c3b6c-127">-IpConfigurationId</span></span>
<span data-ttu-id="c3b6c-128">이 NAT 규칙이 적용되는 IP 구성 ID</span><span class="sxs-lookup"><span data-stu-id="c3b6c-128">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="c3b6c-129">-Mode</span><span class="sxs-lookup"><span data-stu-id="c3b6c-129">-Mode</span></span>
<span data-ttu-id="c3b6c-130">VPN NAT의 원본 NAT 방향</span><span class="sxs-lookup"><span data-stu-id="c3b6c-130">The Source NAT direction of a VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EgressSnat, IngressSnat

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b6c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c3b6c-131">-Name</span></span>
<span data-ttu-id="c3b6c-132">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-132">The resource name.</span></span>

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

### <span data-ttu-id="c3b6c-133">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c3b6c-133">-ParentResourceName</span></span>
<span data-ttu-id="c3b6c-134">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-134">The parent resource name.</span></span>

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

### <span data-ttu-id="c3b6c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3b6c-135">-ResourceGroupName</span></span>
<span data-ttu-id="c3b6c-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-136">The resource group name.</span></span>

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

### <span data-ttu-id="c3b6c-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3b6c-137">-ResourceId</span></span>
<span data-ttu-id="c3b6c-138">삭제할 VpnGatewayNatRule 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-138">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b6c-139">-Type</span><span class="sxs-lookup"><span data-stu-id="c3b6c-139">-Type</span></span>
<span data-ttu-id="c3b6c-140">VPN NAT에 대한 NAT 규칙의 유형</span><span class="sxs-lookup"><span data-stu-id="c3b6c-140">The type of NAT rule for VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b6c-141">-확인</span><span class="sxs-lookup"><span data-stu-id="c3b6c-141">-Confirm</span></span>
<span data-ttu-id="c3b6c-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3b6c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3b6c-143">-WhatIf</span></span>
<span data-ttu-id="c3b6c-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3b6c-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3b6c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b6c-146">CommonParameters</span></span>
<span data-ttu-id="c3b6c-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b6c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b6c-148">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3b6c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b6c-149">입력</span><span class="sxs-lookup"><span data-stu-id="c3b6c-149">INPUTS</span></span>

### <span data-ttu-id="c3b6c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c3b6c-150">System.String</span></span>

### <span data-ttu-id="c3b6c-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="c3b6c-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="c3b6c-152">출력</span><span class="sxs-lookup"><span data-stu-id="c3b6c-152">OUTPUTS</span></span>

### <span data-ttu-id="c3b6c-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="c3b6c-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="c3b6c-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c3b6c-154">NOTES</span></span>

## <span data-ttu-id="c3b6c-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3b6c-155">RELATED LINKS</span></span>
