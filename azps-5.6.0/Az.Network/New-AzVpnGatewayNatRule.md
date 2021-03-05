---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
ms.openlocfilehash: d4f0b908a229ee47472d40eefe60c5771c0147d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984368"
---
# <span data-ttu-id="4f689-101">New-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="4f689-101">New-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="4f689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f689-102">SYNOPSIS</span></span>
<span data-ttu-id="4f689-103">VpnSiteLinkConnection과 연결할 수 있는 VpnGateway에서 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-103">Creates a NAT rule on a VpnGateway which can be associated with VpnSiteLinkConnection.</span></span>

## <span data-ttu-id="4f689-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f689-104">SYNTAX</span></span>

### <span data-ttu-id="4f689-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4f689-105">ByVpnGatewayName (Default)</span></span>
```
New-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] -InternalMapping <String[]> -ExternalMapping <String[]>
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f689-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="4f689-106">ByVpnGatewayObject</span></span>
```
New-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f689-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4f689-107">ByVpnGatewayResourceId</span></span>
```
New-AzVpnGatewayNatRule -ParentResourceId <String> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f689-108">설명</span><span class="sxs-lookup"><span data-stu-id="4f689-108">DESCRIPTION</span></span>
<span data-ttu-id="4f689-109">VpnGateway와 연결될 수 있는 VPNGateway에 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-109">Creates a NAT rule on a VpnGateway which can be associated with VpnGateway.</span></span>

## <span data-ttu-id="4f689-110">예제</span><span class="sxs-lookup"><span data-stu-id="4f689-110">EXAMPLES</span></span>

### <span data-ttu-id="4f689-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f689-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"

Type                      : Static
Mode                      : EgressSnat
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

<span data-ttu-id="4f689-112">위의 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="4f689-113">그런 다음 해당 Virtual Hub 아래에 VpnGateway를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="4f689-114">그런 다음 이 명령을 사용하여 New-AzVpnGatewayNatRule, NAT 규칙을 만들 수 있습니다. 생성된 VpnGateway와 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-114">Then, using this command: New-AzVpnGatewayNatRule, NAT rule can be createdand associated with created VpnGateway.</span></span>

## <span data-ttu-id="4f689-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4f689-115">PARAMETERS</span></span>

### <span data-ttu-id="4f689-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f689-116">-AsJob</span></span>
<span data-ttu-id="4f689-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4f689-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f689-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f689-118">-DefaultProfile</span></span>
<span data-ttu-id="4f689-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f689-120">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="4f689-120">-ExternalMapping</span></span>
<span data-ttu-id="4f689-121">NAT에 대한 개인 IP 주소 서브넷 외부 매핑 목록</span><span class="sxs-lookup"><span data-stu-id="4f689-121">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f689-122">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="4f689-122">-InternalMapping</span></span>
<span data-ttu-id="4f689-123">NAT에 대한 개인 IP 주소 서브넷 내부 매핑 목록</span><span class="sxs-lookup"><span data-stu-id="4f689-123">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f689-124">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4f689-124">-IpConfigurationId</span></span>
<span data-ttu-id="4f689-125">이 NAT 규칙이 적용되는 IP 구성 ID</span><span class="sxs-lookup"><span data-stu-id="4f689-125">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="4f689-126">-Mode</span><span class="sxs-lookup"><span data-stu-id="4f689-126">-Mode</span></span>
<span data-ttu-id="4f689-127">VPN NAT의 원본 NAT 방향</span><span class="sxs-lookup"><span data-stu-id="4f689-127">The Source NAT direction of a VPN NAT</span></span>

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

### <span data-ttu-id="4f689-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4f689-128">-Name</span></span>
<span data-ttu-id="4f689-129">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-129">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f689-130">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4f689-130">-ParentObject</span></span>
<span data-ttu-id="4f689-131">이 NAT 규칙에 대한 상위 VpnGateway입니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-131">The parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f689-132">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4f689-132">-ParentResourceId</span></span>
<span data-ttu-id="4f689-133">이 NAT 규칙에 대한 부모 VpnGateway의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-133">The resource id of the parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f689-134">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4f689-134">-ParentResourceName</span></span>
<span data-ttu-id="4f689-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f689-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f689-136">-ResourceGroupName</span></span>
<span data-ttu-id="4f689-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-137">The resource group name.</span></span>

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

### <span data-ttu-id="4f689-138">-Type</span><span class="sxs-lookup"><span data-stu-id="4f689-138">-Type</span></span>
<span data-ttu-id="4f689-139">VPN NAT에 대한 NAT 규칙의 유형</span><span class="sxs-lookup"><span data-stu-id="4f689-139">The type of NAT rule for VPN NAT</span></span>

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

### <span data-ttu-id="4f689-140">-확인</span><span class="sxs-lookup"><span data-stu-id="4f689-140">-Confirm</span></span>
<span data-ttu-id="4f689-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f689-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f689-142">-WhatIf</span></span>
<span data-ttu-id="4f689-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f689-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f689-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f689-145">CommonParameters</span></span>
<span data-ttu-id="4f689-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f689-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f689-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f689-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f689-148">입력</span><span class="sxs-lookup"><span data-stu-id="4f689-148">INPUTS</span></span>

### <span data-ttu-id="4f689-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4f689-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="4f689-150">System.String</span><span class="sxs-lookup"><span data-stu-id="4f689-150">System.String</span></span>

## <span data-ttu-id="4f689-151">출력</span><span class="sxs-lookup"><span data-stu-id="4f689-151">OUTPUTS</span></span>

### <span data-ttu-id="4f689-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="4f689-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="4f689-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f689-153">NOTES</span></span>

## <span data-ttu-id="4f689-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f689-154">RELATED LINKS</span></span>
