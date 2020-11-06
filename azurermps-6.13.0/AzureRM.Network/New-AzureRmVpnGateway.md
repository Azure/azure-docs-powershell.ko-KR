---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnGateway.md
ms.openlocfilehash: b29b57ea7d7a5182a25cb05ae05e6d1644a5c18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529497"
---
# <span data-ttu-id="6e38f-101">New-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6e38f-101">New-AzureRmVpnGateway</span></span>

## <span data-ttu-id="6e38f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e38f-102">SYNOPSIS</span></span>
<span data-ttu-id="6e38f-103">확장 가능한 VPN 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-103">Creates a Scalable VPN Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e38f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e38f-104">SYNTAX</span></span>

### <span data-ttu-id="6e38f-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6e38f-105">ByVirtualHubName (Default)</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e38f-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="6e38f-106">ByVirtualHubObject</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e38f-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6e38f-107">ByVirtualHubResourceId</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e38f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6e38f-108">DESCRIPTION</span></span>

<span data-ttu-id="6e38f-109">New-AzureRmVpnGateway는 확장 가능한 VPN 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-109">New-AzureRmVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="6e38f-110">이는 VirtualHub 내 사이트 간 연결에 대 한 소프트웨어 정의 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="6e38f-111">이 게이트웨이에는이 게이트웨이의 크기를 조정 하 고이를 Set-AzureRmVpnGateway cmdlet에 지정 된 배율 단위를 기준으로 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzureRmVpnGateway cmdlet.</span></span> 

<span data-ttu-id="6e38f-112">VPNSite로 알려진 지사/사이트에서 확장 가능한 게이트웨이로 연결이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="6e38f-113">각 연결은 2 개의 Active-Active 터널로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="6e38f-114">VpnGateway는 참조 되는 VirtualHub와 같은 위치에 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="6e38f-115">예제의</span><span class="sxs-lookup"><span data-stu-id="6e38f-115">EXAMPLES</span></span>

### <span data-ttu-id="6e38f-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e38f-116">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

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

<span data-ttu-id="6e38f-117">위의 방법을 통해 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="6e38f-118">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="6e38f-119">변수</span><span class="sxs-lookup"><span data-stu-id="6e38f-119">PARAMETERS</span></span>

### <span data-ttu-id="6e38f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e38f-120">-AsJob</span></span>
<span data-ttu-id="6e38f-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6e38f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e38f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e38f-122">-DefaultProfile</span></span>
<span data-ttu-id="6e38f-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e38f-124">-이름</span><span class="sxs-lookup"><span data-stu-id="6e38f-124">-Name</span></span>
<span data-ttu-id="6e38f-125">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-125">The resource name.</span></span>

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

### <span data-ttu-id="6e38f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e38f-126">-ResourceGroupName</span></span>
<span data-ttu-id="6e38f-127">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-127">The resource name.</span></span>

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

### <span data-ttu-id="6e38f-128">태그</span><span class="sxs-lookup"><span data-stu-id="6e38f-128">-Tag</span></span>
<span data-ttu-id="6e38f-129">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6e38f-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="6e38f-130">-VirtualHub</span></span>
<span data-ttu-id="6e38f-131">이 VpnGateway 연결 해야 하는 VirtualHub입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="6e38f-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="6e38f-132">-VirtualHubId</span></span>
<span data-ttu-id="6e38f-133">이 VpnGateway와 연결 되어야 하는 VirtualHub의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="6e38f-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="6e38f-134">-VirtualHubName</span></span>
<span data-ttu-id="6e38f-135">이 VpnGateway와 연결 되어야 하는 VirtualHub의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="6e38f-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6e38f-136">-VpnConnection</span></span>
<span data-ttu-id="6e38f-137">이 VpnGateway에 있어야 하는 VpnConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="6e38f-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="6e38f-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="6e38f-139">이 VpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-139">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="6e38f-140">-확인</span><span class="sxs-lookup"><span data-stu-id="6e38f-140">-Confirm</span></span>
<span data-ttu-id="6e38f-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e38f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e38f-142">-WhatIf</span></span>
<span data-ttu-id="6e38f-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e38f-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e38f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e38f-145">CommonParameters</span></span>
<span data-ttu-id="6e38f-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e38f-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e38f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e38f-148">입력</span><span class="sxs-lookup"><span data-stu-id="6e38f-148">INPUTS</span></span>

### <span data-ttu-id="6e38f-149">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6e38f-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="6e38f-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6e38f-150">System.String</span></span>

## <span data-ttu-id="6e38f-151">출력</span><span class="sxs-lookup"><span data-stu-id="6e38f-151">OUTPUTS</span></span>

### <span data-ttu-id="6e38f-152">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6e38f-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="6e38f-153">상속자</span><span class="sxs-lookup"><span data-stu-id="6e38f-153">NOTES</span></span>

## <span data-ttu-id="6e38f-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e38f-154">RELATED LINKS</span></span>
