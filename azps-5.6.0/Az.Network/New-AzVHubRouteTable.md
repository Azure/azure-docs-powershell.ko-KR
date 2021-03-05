---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: 77288758af2f0f3294d8f32c92b7f687dab79a97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964144"
---
# <span data-ttu-id="ee22a-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ee22a-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="ee22a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee22a-102">SYNOPSIS</span></span>
<span data-ttu-id="ee22a-103">VirtualHub와 연결된 허브 경로 테이블 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="ee22a-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee22a-104">SYNTAX</span></span>

### <span data-ttu-id="ee22a-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ee22a-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee22a-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ee22a-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee22a-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ee22a-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee22a-108">설명</span><span class="sxs-lookup"><span data-stu-id="ee22a-108">DESCRIPTION</span></span>
<span data-ttu-id="ee22a-109">지정된 가상 허브와 연결된 지정된 경로 테이블을 제공된 경로 및 레이블로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="ee22a-110">예제</span><span class="sxs-lookup"><span data-stu-id="ee22a-110">EXAMPLES</span></span>

### <span data-ttu-id="ee22a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee22a-111">Example 1</span></span>

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

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "private-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "10.30.0.0/16",
                               "10.40.0.0/16"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="ee22a-112">이 명령은 가상 허브의 허브 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="ee22a-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ee22a-113">PARAMETERS</span></span>

### <span data-ttu-id="ee22a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee22a-114">-AsJob</span></span>
<span data-ttu-id="ee22a-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ee22a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee22a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee22a-116">-DefaultProfile</span></span>
<span data-ttu-id="ee22a-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee22a-118">-Label</span><span class="sxs-lookup"><span data-stu-id="ee22a-118">-Label</span></span>
<span data-ttu-id="ee22a-119">레이블 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-119">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee22a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ee22a-120">-Name</span></span>
<span data-ttu-id="ee22a-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee22a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ee22a-122">-ParentObject</span></span>
<span data-ttu-id="ee22a-123">이 리소스의 부모 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="ee22a-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="ee22a-124">-ParentResourceName</span></span>
<span data-ttu-id="ee22a-125">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-125">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee22a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee22a-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee22a-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee22a-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ee22a-128">-ParentResourceId</span></span>
<span data-ttu-id="ee22a-129">가상 허브 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-129">The resource id of the virtual hub resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee22a-130">-Route</span><span class="sxs-lookup"><span data-stu-id="ee22a-130">-Route</span></span>
<span data-ttu-id="ee22a-131">이 경로 테이블의 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-131">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee22a-132">-확인</span><span class="sxs-lookup"><span data-stu-id="ee22a-132">-Confirm</span></span>
<span data-ttu-id="ee22a-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee22a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee22a-134">-WhatIf</span></span>
<span data-ttu-id="ee22a-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee22a-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee22a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee22a-137">CommonParameters</span></span>
<span data-ttu-id="ee22a-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee22a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee22a-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee22a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee22a-140">입력</span><span class="sxs-lookup"><span data-stu-id="ee22a-140">INPUTS</span></span>

### <span data-ttu-id="ee22a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ee22a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ee22a-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ee22a-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="ee22a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ee22a-143">System.String</span></span>

## <span data-ttu-id="ee22a-144">출력</span><span class="sxs-lookup"><span data-stu-id="ee22a-144">OUTPUTS</span></span>

### <span data-ttu-id="ee22a-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ee22a-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="ee22a-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee22a-146">NOTES</span></span>

## <span data-ttu-id="ee22a-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee22a-147">RELATED LINKS</span></span>

[<span data-ttu-id="ee22a-148">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ee22a-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="ee22a-149">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="ee22a-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="ee22a-150">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ee22a-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="ee22a-151">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ee22a-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
