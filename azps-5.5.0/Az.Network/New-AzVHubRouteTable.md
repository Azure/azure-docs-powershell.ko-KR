---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: d9c7b4895d05b4f55ef91705062db7c200d702cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193580"
---
# <span data-ttu-id="bd906-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bd906-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="bd906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd906-102">SYNOPSIS</span></span>
<span data-ttu-id="bd906-103">VirtualHub와 연결된 허브 경로 테이블 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="bd906-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd906-104">SYNTAX</span></span>

### <span data-ttu-id="bd906-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="bd906-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd906-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="bd906-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd906-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="bd906-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd906-108">설명</span><span class="sxs-lookup"><span data-stu-id="bd906-108">DESCRIPTION</span></span>
<span data-ttu-id="bd906-109">제공된 경로 및 레이블을 통해 지정된 가상 허브와 연결된 지정된 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="bd906-110">예제</span><span class="sxs-lookup"><span data-stu-id="bd906-110">EXAMPLES</span></span>

### <span data-ttu-id="bd906-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bd906-111">Example 1</span></span>

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

<span data-ttu-id="bd906-112">이 명령은 가상 허브의 허브 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="bd906-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd906-113">PARAMETERS</span></span>

### <span data-ttu-id="bd906-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd906-114">-AsJob</span></span>
<span data-ttu-id="bd906-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bd906-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd906-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd906-116">-DefaultProfile</span></span>
<span data-ttu-id="bd906-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd906-118">-Label</span><span class="sxs-lookup"><span data-stu-id="bd906-118">-Label</span></span>
<span data-ttu-id="bd906-119">레이블 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-119">The list of labels.</span></span>

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

### <span data-ttu-id="bd906-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bd906-120">-Name</span></span>
<span data-ttu-id="bd906-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-121">The resource name.</span></span>

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

### <span data-ttu-id="bd906-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bd906-122">-ParentObject</span></span>
<span data-ttu-id="bd906-123">이 리소스의 부모 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="bd906-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="bd906-124">-ParentResourceName</span></span>
<span data-ttu-id="bd906-125">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-125">The parent resource name.</span></span>

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

### <span data-ttu-id="bd906-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd906-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd906-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-127">The resource group name.</span></span>

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

### <span data-ttu-id="bd906-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bd906-128">-ParentResourceId</span></span>
<span data-ttu-id="bd906-129">가상 허브 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-129">The resource id of the virtual hub resource.</span></span>

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

### <span data-ttu-id="bd906-130">-Route</span><span class="sxs-lookup"><span data-stu-id="bd906-130">-Route</span></span>
<span data-ttu-id="bd906-131">이 경로 테이블에 대한 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-131">The list of routes for this route table.</span></span>

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

### <span data-ttu-id="bd906-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd906-132">-Confirm</span></span>
<span data-ttu-id="bd906-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd906-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd906-134">-WhatIf</span></span>
<span data-ttu-id="bd906-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bd906-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd906-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd906-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd906-137">CommonParameters</span></span>
<span data-ttu-id="bd906-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd906-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd906-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bd906-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd906-140">입력</span><span class="sxs-lookup"><span data-stu-id="bd906-140">INPUTS</span></span>

### <span data-ttu-id="bd906-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bd906-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="bd906-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bd906-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="bd906-143">System.String</span><span class="sxs-lookup"><span data-stu-id="bd906-143">System.String</span></span>

## <span data-ttu-id="bd906-144">출력</span><span class="sxs-lookup"><span data-stu-id="bd906-144">OUTPUTS</span></span>

### <span data-ttu-id="bd906-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bd906-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="bd906-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd906-146">NOTES</span></span>

## <span data-ttu-id="bd906-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd906-147">RELATED LINKS</span></span>

[<span data-ttu-id="bd906-148">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bd906-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="bd906-149">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="bd906-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="bd906-150">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bd906-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="bd906-151">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bd906-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
