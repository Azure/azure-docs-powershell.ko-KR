---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: d330b7e25cc1184a3efaea2c3deb569bf44171b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214045"
---
# <span data-ttu-id="ddefa-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ddefa-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="ddefa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddefa-102">SYNOPSIS</span></span>
<span data-ttu-id="ddefa-103">VirtualHub와 연결 된 허브 경로 테이블 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="ddefa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ddefa-104">SYNTAX</span></span>

### <span data-ttu-id="ddefa-105">ByVHubRouteTableName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ddefa-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddefa-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ddefa-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddefa-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="ddefa-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddefa-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="ddefa-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddefa-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ddefa-109">DESCRIPTION</span></span>
<span data-ttu-id="ddefa-110">제공 된 경로 또는 레이블로 지정 된 가상 허브에 연결 된 지정 된 경로 테이블을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="ddefa-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ddefa-111">EXAMPLES</span></span>

### <span data-ttu-id="ddefa-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ddefa-112">Example 1</span></span>
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

<span data-ttu-id="ddefa-113">이 명령은 가상 허브의 허브 경로 테이블을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="ddefa-114">변수</span><span class="sxs-lookup"><span data-stu-id="ddefa-114">PARAMETERS</span></span>

### <span data-ttu-id="ddefa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddefa-115">-AsJob</span></span>
<span data-ttu-id="ddefa-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ddefa-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddefa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddefa-117">-DefaultProfile</span></span>
<span data-ttu-id="ddefa-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddefa-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddefa-119">-InputObject</span></span>
<span data-ttu-id="ddefa-120">업데이트할 vhubroutetable 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-120">The vhubroutetable resource to Update.</span></span>

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

### <span data-ttu-id="ddefa-121">-레이블</span><span class="sxs-lookup"><span data-stu-id="ddefa-121">-Label</span></span>
<span data-ttu-id="ddefa-122">레이블 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-122">The list of labels.</span></span>

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

### <span data-ttu-id="ddefa-123">-이름</span><span class="sxs-lookup"><span data-stu-id="ddefa-123">-Name</span></span>
<span data-ttu-id="ddefa-124">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-124">The resource name.</span></span>

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

### <span data-ttu-id="ddefa-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ddefa-125">-ParentObject</span></span>
<span data-ttu-id="ddefa-126">이 리소스의 부모 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="ddefa-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="ddefa-127">-ParentResourceName</span></span>
<span data-ttu-id="ddefa-128">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-128">The parent resource name.</span></span>

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

### <span data-ttu-id="ddefa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddefa-129">-ResourceGroupName</span></span>
<span data-ttu-id="ddefa-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-130">The resource group name.</span></span>

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

### <span data-ttu-id="ddefa-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddefa-131">-ResourceId</span></span>
<span data-ttu-id="ddefa-132">업데이트할 vhubroutetable 리소스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-132">The resource id of the vhubroutetable resource to Update.</span></span>

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

### <span data-ttu-id="ddefa-133">-경로</span><span class="sxs-lookup"><span data-stu-id="ddefa-133">-Route</span></span>
<span data-ttu-id="ddefa-134">이 경로 테이블에 대 한 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-134">The list of routes for this route table.</span></span>

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

### <span data-ttu-id="ddefa-135">-확인</span><span class="sxs-lookup"><span data-stu-id="ddefa-135">-Confirm</span></span>
<span data-ttu-id="ddefa-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddefa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddefa-137">-WhatIf</span></span>
<span data-ttu-id="ddefa-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddefa-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddefa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddefa-140">CommonParameters</span></span>
<span data-ttu-id="ddefa-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddefa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddefa-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ddefa-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddefa-143">입력</span><span class="sxs-lookup"><span data-stu-id="ddefa-143">INPUTS</span></span>

### <span data-ttu-id="ddefa-144">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ddefa-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ddefa-145">PSVHubRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ddefa-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="ddefa-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ddefa-146">System.String</span></span>

## <span data-ttu-id="ddefa-147">출력</span><span class="sxs-lookup"><span data-stu-id="ddefa-147">OUTPUTS</span></span>

### <span data-ttu-id="ddefa-148">PSVHubRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ddefa-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="ddefa-149">상속자</span><span class="sxs-lookup"><span data-stu-id="ddefa-149">NOTES</span></span>

## <span data-ttu-id="ddefa-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ddefa-150">RELATED LINKS</span></span>

[<span data-ttu-id="ddefa-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ddefa-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="ddefa-152">새로운 AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="ddefa-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="ddefa-153">새로운 AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ddefa-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="ddefa-154">제거-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ddefa-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)