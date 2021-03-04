---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: b3b4fe711cbccd195f4549ae936fe438185c9070
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951595"
---
# <span data-ttu-id="6fef7-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6fef7-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="6fef7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fef7-102">SYNOPSIS</span></span>
<span data-ttu-id="6fef7-103">VirtualHub와 연결된 허브 경로 테이블 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="6fef7-104">구문</span><span class="sxs-lookup"><span data-stu-id="6fef7-104">SYNTAX</span></span>

### <span data-ttu-id="6fef7-105">ByVHubRouteTableName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6fef7-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fef7-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="6fef7-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fef7-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="6fef7-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fef7-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="6fef7-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fef7-109">설명</span><span class="sxs-lookup"><span data-stu-id="6fef7-109">DESCRIPTION</span></span>
<span data-ttu-id="6fef7-110">지정된 가상 허브와 연결된 지정된 경로 테이블을 제공된 경로 또는 레이블로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="6fef7-111">예제</span><span class="sxs-lookup"><span data-stu-id="6fef7-111">EXAMPLES</span></span>

### <span data-ttu-id="6fef7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6fef7-112">Example 1</span></span>
```powershell
PS C:\> New-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan" -Location "westcentralus" -VirtualWANType "Standard" -AllowVnetToVnetTraffic -AllowBranchToBranchTraffic
PS C:\> $virtualWan = Get-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan"

PS C:\> New-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub" -Location "westcentralus" -AddressPrefix "10.0.0.0/16" -VirtualWan $virtualWan
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub"

PS C:\> $fwIp = New-AzFirewallHubPublicIpAddress -Count 1
PS C:\> $hubIpAddresses = New-AzFirewallHubIpAddress -PublicIP $fwIp
PS C:\> New-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg" -Location "westcentralus" -Sku AZFW_Hub -VirtualHubId $virtualHub.Id -HubIPAddress $hubIpAddresses
PS C:\> $firewall = Get-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg"

PS C:\> $route1 = New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> New-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route1) -Label @("testLabel")
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

PS C:\> $route2 = New-AzVHubRoute -Name "internet-traffic" -Destination @("0.0.0.0/0") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> Update-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route2)
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "internet-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "0.0.0.0/0"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="6fef7-113">이 명령은 가상 허브의 허브 경로 테이블을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="6fef7-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6fef7-114">PARAMETERS</span></span>

### <span data-ttu-id="6fef7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fef7-115">-AsJob</span></span>
<span data-ttu-id="6fef7-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6fef7-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fef7-117">-DefaultProfile</span></span>
<span data-ttu-id="6fef7-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fef7-119">-InputObject</span></span>
<span data-ttu-id="6fef7-120">업데이트할 vhubroutetable 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-120">The vhubroutetable resource to Update.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-121">-Label</span><span class="sxs-lookup"><span data-stu-id="6fef7-121">-Label</span></span>
<span data-ttu-id="6fef7-122">레이블 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-122">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6fef7-123">-Name</span></span>
<span data-ttu-id="6fef7-124">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6fef7-125">-ParentObject</span></span>
<span data-ttu-id="6fef7-126">이 리소스의 부모 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6fef7-127">-ParentResourceName</span></span>
<span data-ttu-id="6fef7-128">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fef7-129">-ResourceGroupName</span></span>
<span data-ttu-id="6fef7-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fef7-131">-ResourceId</span></span>
<span data-ttu-id="6fef7-132">업데이트할 vhubroutetable 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-132">The resource id of the vhubroutetable resource to Update.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-133">-Route</span><span class="sxs-lookup"><span data-stu-id="6fef7-133">-Route</span></span>
<span data-ttu-id="6fef7-134">이 경로 테이블의 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-134">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-135">-확인</span><span class="sxs-lookup"><span data-stu-id="6fef7-135">-Confirm</span></span>
<span data-ttu-id="6fef7-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fef7-137">-WhatIf</span></span>
<span data-ttu-id="6fef7-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fef7-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fef7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fef7-140">CommonParameters</span></span>
<span data-ttu-id="6fef7-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6fef7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fef7-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fef7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fef7-143">입력</span><span class="sxs-lookup"><span data-stu-id="6fef7-143">INPUTS</span></span>

### <span data-ttu-id="6fef7-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6fef7-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="6fef7-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6fef7-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="6fef7-146">System.String</span><span class="sxs-lookup"><span data-stu-id="6fef7-146">System.String</span></span>

## <span data-ttu-id="6fef7-147">출력</span><span class="sxs-lookup"><span data-stu-id="6fef7-147">OUTPUTS</span></span>

### <span data-ttu-id="6fef7-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6fef7-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="6fef7-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6fef7-149">NOTES</span></span>

## <span data-ttu-id="6fef7-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fef7-150">RELATED LINKS</span></span>

[<span data-ttu-id="6fef7-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6fef7-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="6fef7-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="6fef7-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="6fef7-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6fef7-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="6fef7-154">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6fef7-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)