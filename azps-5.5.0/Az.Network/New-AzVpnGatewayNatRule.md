---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
ms.openlocfilehash: 45ec34bf437c64b96c3c46afa142d5e5b12f6010
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193537"
---
# <span data-ttu-id="39fd0-101">New-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="39fd0-101">New-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="39fd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="39fd0-103">VpnSiteLinkConnection과 연결할 수 있는 VpnGateway에 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-103">Creates a NAT rule on a VpnGateway which can be associated with VpnSiteLinkConnection.</span></span>

## <span data-ttu-id="39fd0-104">구문</span><span class="sxs-lookup"><span data-stu-id="39fd0-104">SYNTAX</span></span>

### <span data-ttu-id="39fd0-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="39fd0-105">ByVpnGatewayName (Default)</span></span>
```
New-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] -InternalMapping <String[]> -ExternalMapping <String[]>
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39fd0-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="39fd0-106">ByVpnGatewayObject</span></span>
```
New-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39fd0-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="39fd0-107">ByVpnGatewayResourceId</span></span>
```
New-AzVpnGatewayNatRule -ParentResourceId <String> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39fd0-108">설명</span><span class="sxs-lookup"><span data-stu-id="39fd0-108">DESCRIPTION</span></span>
<span data-ttu-id="39fd0-109">VpnGateway와 연결될 수 있는 VpnGateway에 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-109">Creates a NAT rule on a VpnGateway which can be associated with VpnGateway.</span></span>

## <span data-ttu-id="39fd0-110">예제</span><span class="sxs-lookup"><span data-stu-id="39fd0-110">EXAMPLES</span></span>

### <span data-ttu-id="39fd0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="39fd0-111">Example 1</span></span>

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

<span data-ttu-id="39fd0-112">위의 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="39fd0-113">그런 다음 해당 Virtual Hub 아래에 VpnGateway를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="39fd0-114">그런 다음, New-AzVpnGatewayNatRule 명령을 사용하여 NAT 규칙을 만들 수 있습니다. 생성된 VpnGateway와 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-114">Then, using this command: New-AzVpnGatewayNatRule, NAT rule can be createdand associated with created VpnGateway.</span></span>

## <span data-ttu-id="39fd0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39fd0-115">PARAMETERS</span></span>

### <span data-ttu-id="39fd0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39fd0-116">-AsJob</span></span>
<span data-ttu-id="39fd0-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="39fd0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39fd0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39fd0-118">-DefaultProfile</span></span>
<span data-ttu-id="39fd0-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39fd0-120">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="39fd0-120">-ExternalMapping</span></span>
<span data-ttu-id="39fd0-121">NAT에 대한 개인 IP 주소 서브넷 외부 매핑 목록</span><span class="sxs-lookup"><span data-stu-id="39fd0-121">The list of private IP address subnet external mappings for NAT</span></span>

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

### <span data-ttu-id="39fd0-122">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="39fd0-122">-InternalMapping</span></span>
<span data-ttu-id="39fd0-123">NAT에 대한 개인 IP 주소 서브넷 내부 매핑 목록</span><span class="sxs-lookup"><span data-stu-id="39fd0-123">The list of private IP address subnet internal mappings for NAT</span></span>

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

### <span data-ttu-id="39fd0-124">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="39fd0-124">-IpConfigurationId</span></span>
<span data-ttu-id="39fd0-125">이 NAT 규칙이 적용되는 IP 구성 ID</span><span class="sxs-lookup"><span data-stu-id="39fd0-125">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="39fd0-126">-Mode</span><span class="sxs-lookup"><span data-stu-id="39fd0-126">-Mode</span></span>
<span data-ttu-id="39fd0-127">VPN NAT의 원본 NAT 방향</span><span class="sxs-lookup"><span data-stu-id="39fd0-127">The Source NAT direction of a VPN NAT</span></span>

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

### <span data-ttu-id="39fd0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="39fd0-128">-Name</span></span>
<span data-ttu-id="39fd0-129">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-129">The resource name.</span></span>

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

### <span data-ttu-id="39fd0-130">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="39fd0-130">-ParentObject</span></span>
<span data-ttu-id="39fd0-131">이 NAT 규칙에 대한 부모 VpnGateway입니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-131">The parent VpnGateway for this NAT Rule.</span></span>

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

### <span data-ttu-id="39fd0-132">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="39fd0-132">-ParentResourceId</span></span>
<span data-ttu-id="39fd0-133">이 NAT 규칙에 대한 부모 VpnGateway의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-133">The resource id of the parent VpnGateway for this NAT Rule.</span></span>

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

### <span data-ttu-id="39fd0-134">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="39fd0-134">-ParentResourceName</span></span>
<span data-ttu-id="39fd0-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-135">The resource group name.</span></span>

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

### <span data-ttu-id="39fd0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39fd0-136">-ResourceGroupName</span></span>
<span data-ttu-id="39fd0-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-137">The resource group name.</span></span>

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

### <span data-ttu-id="39fd0-138">-Type</span><span class="sxs-lookup"><span data-stu-id="39fd0-138">-Type</span></span>
<span data-ttu-id="39fd0-139">VPN NAT에 대한 NAT 규칙의 유형</span><span class="sxs-lookup"><span data-stu-id="39fd0-139">The type of NAT rule for VPN NAT</span></span>

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

### <span data-ttu-id="39fd0-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39fd0-140">-Confirm</span></span>
<span data-ttu-id="39fd0-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39fd0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39fd0-142">-WhatIf</span></span>
<span data-ttu-id="39fd0-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="39fd0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39fd0-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39fd0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39fd0-145">CommonParameters</span></span>
<span data-ttu-id="39fd0-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="39fd0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39fd0-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39fd0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39fd0-148">입력</span><span class="sxs-lookup"><span data-stu-id="39fd0-148">INPUTS</span></span>

### <span data-ttu-id="39fd0-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39fd0-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="39fd0-150">System.String</span><span class="sxs-lookup"><span data-stu-id="39fd0-150">System.String</span></span>

## <span data-ttu-id="39fd0-151">출력</span><span class="sxs-lookup"><span data-stu-id="39fd0-151">OUTPUTS</span></span>

### <span data-ttu-id="39fd0-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="39fd0-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="39fd0-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="39fd0-153">NOTES</span></span>

## <span data-ttu-id="39fd0-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39fd0-154">RELATED LINKS</span></span>
