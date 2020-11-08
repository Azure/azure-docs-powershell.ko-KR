---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 8db43fc826086235a51f32e67a8f787a3ac5792d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041771"
---
# <span data-ttu-id="63802-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="63802-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="63802-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63802-102">SYNOPSIS</span></span>
<span data-ttu-id="63802-103">확장 가능한 VPN 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="63802-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="63802-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63802-104">SYNTAX</span></span>

### <span data-ttu-id="63802-105">ByVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="63802-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63802-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="63802-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63802-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="63802-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63802-108">설명은</span><span class="sxs-lookup"><span data-stu-id="63802-108">DESCRIPTION</span></span>
<span data-ttu-id="63802-109">**업데이트 AzVpnGateway** cmdlet은 확장 가능한 VPN 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="63802-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="63802-110">Azure VPN 게이트웨이는 VirtualHub 내 사이트 간 연결에 대해 소프트웨어에 정의 된 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="63802-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="63802-111">이 게이트웨이에는 사용자가 지정한 배율 단위에 따라 크기가 조정 되 고 크기가 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63802-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="63802-112">VPN 사이트 라고 하는 지사/사이트에서 확장 가능한 게이트웨이로의 연결을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63802-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="63802-113">각 연결은 2 개의 Active-Active 터널로 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63802-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="63802-114">예제의</span><span class="sxs-lookup"><span data-stu-id="63802-114">EXAMPLES</span></span>

### <span data-ttu-id="63802-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="63802-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="63802-116">위의 방법을 통해 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63802-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="63802-117">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63802-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="63802-118">게이트웨이를 만든 후에는 Set-AzVpnGateway를 사용 하 여 게이트웨이를 3 단위 단위로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="63802-118">After the gateway has been created, it uses Set-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="63802-119">변수</span><span class="sxs-lookup"><span data-stu-id="63802-119">PARAMETERS</span></span>

### <span data-ttu-id="63802-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63802-120">-AsJob</span></span>
<span data-ttu-id="63802-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="63802-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63802-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63802-122">-DefaultProfile</span></span>
<span data-ttu-id="63802-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63802-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63802-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63802-124">-InputObject</span></span>
<span data-ttu-id="63802-125">수정할 vpn 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="63802-125">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="63802-126">-이름</span><span class="sxs-lookup"><span data-stu-id="63802-126">-Name</span></span>
<span data-ttu-id="63802-127">가상 wan 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63802-127">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63802-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63802-128">-ResourceGroupName</span></span>
<span data-ttu-id="63802-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63802-129">The resource group name.</span></span>

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

### <span data-ttu-id="63802-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63802-130">-ResourceId</span></span>
<span data-ttu-id="63802-131">수정할 VpnGateway의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="63802-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63802-132">태그</span><span class="sxs-lookup"><span data-stu-id="63802-132">-Tag</span></span>
<span data-ttu-id="63802-133">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="63802-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="63802-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="63802-134">-VpnConnection</span></span>
<span data-ttu-id="63802-135">이 VpnGateway에 있어야 하는 VpnConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="63802-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63802-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="63802-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="63802-137">이 VpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="63802-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="63802-138">-확인</span><span class="sxs-lookup"><span data-stu-id="63802-138">-Confirm</span></span>
<span data-ttu-id="63802-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63802-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63802-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63802-140">-WhatIf</span></span>
<span data-ttu-id="63802-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="63802-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63802-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63802-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63802-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63802-143">CommonParameters</span></span>
<span data-ttu-id="63802-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63802-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63802-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63802-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63802-146">입력</span><span class="sxs-lookup"><span data-stu-id="63802-146">INPUTS</span></span>

### <span data-ttu-id="63802-147">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="63802-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="63802-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63802-148">System.String</span></span>

## <span data-ttu-id="63802-149">출력</span><span class="sxs-lookup"><span data-stu-id="63802-149">OUTPUTS</span></span>

### <span data-ttu-id="63802-150">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="63802-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="63802-151">상속자</span><span class="sxs-lookup"><span data-stu-id="63802-151">NOTES</span></span>

## <span data-ttu-id="63802-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63802-152">RELATED LINKS</span></span>

[<span data-ttu-id="63802-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="63802-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="63802-154">새로운 AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="63802-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="63802-155">제거-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="63802-155">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)
