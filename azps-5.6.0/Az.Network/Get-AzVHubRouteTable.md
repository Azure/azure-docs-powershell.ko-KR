---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 83758842fe91ef6cf8fca24f360750f813a31311
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016235"
---
# <span data-ttu-id="88a7c-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="88a7c-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="88a7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="88a7c-103">VirtualHub와 연결된 허브 경로 테이블 리소스를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="88a7c-104">구문</span><span class="sxs-lookup"><span data-stu-id="88a7c-104">SYNTAX</span></span>

### <span data-ttu-id="88a7c-105">ByVHubRouteTableName(기본값)</span><span class="sxs-lookup"><span data-stu-id="88a7c-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88a7c-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="88a7c-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88a7c-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="88a7c-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88a7c-108">설명</span><span class="sxs-lookup"><span data-stu-id="88a7c-108">DESCRIPTION</span></span>
<span data-ttu-id="88a7c-109">지정된 가상 허브와 연결된 지정된 허브 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="88a7c-110">예제</span><span class="sxs-lookup"><span data-stu-id="88a7c-110">EXAMPLES</span></span>

### <span data-ttu-id="88a7c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="88a7c-111">Example 1</span></span>

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

<span data-ttu-id="88a7c-112">이 명령은 가상 허브의 허브 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="88a7c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="88a7c-113">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName


Name                   : defaultRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []


Name                   : noneRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="88a7c-114">이 명령은 지정된 VirtualHub의 모든 허브 경로 테이블을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="88a7c-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="88a7c-115">PARAMETERS</span></span>

### <span data-ttu-id="88a7c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88a7c-116">-AsJob</span></span>
<span data-ttu-id="88a7c-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="88a7c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88a7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a7c-118">-DefaultProfile</span></span>
<span data-ttu-id="88a7c-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88a7c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="88a7c-120">-Name</span></span>
<span data-ttu-id="88a7c-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-121">The resource name.</span></span>

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

### <span data-ttu-id="88a7c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="88a7c-122">-ParentObject</span></span>
<span data-ttu-id="88a7c-123">이 리소스의 부모 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="88a7c-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="88a7c-124">-ParentResourceName</span></span>
<span data-ttu-id="88a7c-125">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-125">The parent resource name.</span></span>

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

### <span data-ttu-id="88a7c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88a7c-126">-ResourceGroupName</span></span>
<span data-ttu-id="88a7c-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-127">The resource group name.</span></span>

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

### <span data-ttu-id="88a7c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88a7c-128">-ResourceId</span></span>
<span data-ttu-id="88a7c-129">Get에 대한 vhubroutetable 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="88a7c-130">-확인</span><span class="sxs-lookup"><span data-stu-id="88a7c-130">-Confirm</span></span>
<span data-ttu-id="88a7c-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88a7c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88a7c-132">-WhatIf</span></span>
<span data-ttu-id="88a7c-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88a7c-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88a7c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a7c-135">CommonParameters</span></span>
<span data-ttu-id="88a7c-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88a7c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a7c-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88a7c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a7c-138">입력</span><span class="sxs-lookup"><span data-stu-id="88a7c-138">INPUTS</span></span>

### <span data-ttu-id="88a7c-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="88a7c-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="88a7c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="88a7c-140">System.String</span></span>

## <span data-ttu-id="88a7c-141">출력</span><span class="sxs-lookup"><span data-stu-id="88a7c-141">OUTPUTS</span></span>

### <span data-ttu-id="88a7c-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="88a7c-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="88a7c-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88a7c-143">NOTES</span></span>

## <span data-ttu-id="88a7c-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88a7c-144">RELATED LINKS</span></span>

[<span data-ttu-id="88a7c-145">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="88a7c-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="88a7c-146">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="88a7c-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="88a7c-147">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="88a7c-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="88a7c-148">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="88a7c-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)