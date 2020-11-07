---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 08915aaf72fbab91d8173480f4e608ebdbaa28ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869797"
---
# <span data-ttu-id="1fad2-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1fad2-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="1fad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fad2-102">SYNOPSIS</span></span>
<span data-ttu-id="1fad2-103">확장 가능한 VPN 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="1fad2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1fad2-104">SYNTAX</span></span>

### <span data-ttu-id="1fad2-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1fad2-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fad2-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="1fad2-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fad2-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="1fad2-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fad2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1fad2-108">DESCRIPTION</span></span>

<span data-ttu-id="1fad2-109">New-AzVpnGateway는 확장 가능한 VPN 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="1fad2-110">이는 VirtualHub 내 사이트 간 연결에 대 한 소프트웨어 정의 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="1fad2-111">이 게이트웨이에는이 게이트웨이의 크기를 조정 하 고이를 Set-AzVpnGateway cmdlet에 지정 된 배율 단위를 기준으로 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="1fad2-112">VPNSite로 알려진 지사/사이트에서 확장 가능한 게이트웨이로 연결이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="1fad2-113">각 연결은 2 개의 Active-Active 터널로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="1fad2-114">VpnGateway는 참조 되는 VirtualHub와 같은 위치에 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="1fad2-115">예제의</span><span class="sxs-lookup"><span data-stu-id="1fad2-115">EXAMPLES</span></span>

### <span data-ttu-id="1fad2-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="1fad2-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="1fad2-117">위의 방법을 통해 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="1fad2-118">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="1fad2-119">변수</span><span class="sxs-lookup"><span data-stu-id="1fad2-119">PARAMETERS</span></span>

### <span data-ttu-id="1fad2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fad2-120">-AsJob</span></span>
<span data-ttu-id="1fad2-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1fad2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fad2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fad2-122">-DefaultProfile</span></span>
<span data-ttu-id="1fad2-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fad2-124">-이름</span><span class="sxs-lookup"><span data-stu-id="1fad2-124">-Name</span></span>
<span data-ttu-id="1fad2-125">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fad2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fad2-126">-ResourceGroupName</span></span>
<span data-ttu-id="1fad2-127">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-127">The resource name.</span></span>

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

### <span data-ttu-id="1fad2-128">태그</span><span class="sxs-lookup"><span data-stu-id="1fad2-128">-Tag</span></span>
<span data-ttu-id="1fad2-129">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1fad2-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="1fad2-130">-VirtualHub</span></span>
<span data-ttu-id="1fad2-131">이 VpnGateway 연결 해야 하는 VirtualHub입니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="1fad2-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="1fad2-132">-VirtualHubId</span></span>
<span data-ttu-id="1fad2-133">이 VpnGateway와 연결 되어야 하는 VirtualHub의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="1fad2-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="1fad2-134">-VirtualHubName</span></span>
<span data-ttu-id="1fad2-135">이 VpnGateway와 연결 되어야 하는 VirtualHub의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="1fad2-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="1fad2-136">-VpnConnection</span></span>
<span data-ttu-id="1fad2-137">이 VpnGateway에 있어야 하는 VpnConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="1fad2-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="1fad2-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="1fad2-139">이 VpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-139">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="1fad2-140">-확인</span><span class="sxs-lookup"><span data-stu-id="1fad2-140">-Confirm</span></span>
<span data-ttu-id="1fad2-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fad2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fad2-142">-WhatIf</span></span>
<span data-ttu-id="1fad2-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fad2-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fad2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fad2-145">CommonParameters</span></span>
<span data-ttu-id="1fad2-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fad2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fad2-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fad2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fad2-148">입력</span><span class="sxs-lookup"><span data-stu-id="1fad2-148">INPUTS</span></span>

### <span data-ttu-id="1fad2-149">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1fad2-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="1fad2-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1fad2-150">System.String</span></span>

## <span data-ttu-id="1fad2-151">출력</span><span class="sxs-lookup"><span data-stu-id="1fad2-151">OUTPUTS</span></span>

### <span data-ttu-id="1fad2-152">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1fad2-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="1fad2-153">상속자</span><span class="sxs-lookup"><span data-stu-id="1fad2-153">NOTES</span></span>

## <span data-ttu-id="1fad2-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fad2-154">RELATED LINKS</span></span>

[<span data-ttu-id="1fad2-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1fad2-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="1fad2-156">제거-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1fad2-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="1fad2-157">업데이트-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1fad2-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
