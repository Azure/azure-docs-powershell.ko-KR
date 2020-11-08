---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: d9c7b4895d05b4f55ef91705062db7c200d702cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214363"
---
# <span data-ttu-id="15f19-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="15f19-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="15f19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15f19-102">SYNOPSIS</span></span>
<span data-ttu-id="15f19-103">VirtualHub와 연결 된 허브 경로 테이블 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="15f19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15f19-104">SYNTAX</span></span>

### <span data-ttu-id="15f19-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="15f19-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15f19-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="15f19-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15f19-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="15f19-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15f19-108">설명은</span><span class="sxs-lookup"><span data-stu-id="15f19-108">DESCRIPTION</span></span>
<span data-ttu-id="15f19-109">제공 된 경로와 레이블을 사용 하 여 지정 된 가상 허브에 연결 된 지정 된 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="15f19-110">예제의</span><span class="sxs-lookup"><span data-stu-id="15f19-110">EXAMPLES</span></span>

### <span data-ttu-id="15f19-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="15f19-111">Example 1</span></span>

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

<span data-ttu-id="15f19-112">이 명령은 가상 허브의 허브 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="15f19-113">변수</span><span class="sxs-lookup"><span data-stu-id="15f19-113">PARAMETERS</span></span>

### <span data-ttu-id="15f19-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15f19-114">-AsJob</span></span>
<span data-ttu-id="15f19-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="15f19-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15f19-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f19-116">-DefaultProfile</span></span>
<span data-ttu-id="15f19-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15f19-118">-레이블</span><span class="sxs-lookup"><span data-stu-id="15f19-118">-Label</span></span>
<span data-ttu-id="15f19-119">레이블 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-119">The list of labels.</span></span>

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

### <span data-ttu-id="15f19-120">-이름</span><span class="sxs-lookup"><span data-stu-id="15f19-120">-Name</span></span>
<span data-ttu-id="15f19-121">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-121">The resource name.</span></span>

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

### <span data-ttu-id="15f19-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="15f19-122">-ParentObject</span></span>
<span data-ttu-id="15f19-123">이 리소스의 부모 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="15f19-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="15f19-124">-ParentResourceName</span></span>
<span data-ttu-id="15f19-125">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-125">The parent resource name.</span></span>

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

### <span data-ttu-id="15f19-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15f19-126">-ResourceGroupName</span></span>
<span data-ttu-id="15f19-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-127">The resource group name.</span></span>

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

### <span data-ttu-id="15f19-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="15f19-128">-ParentResourceId</span></span>
<span data-ttu-id="15f19-129">가상 허브 리소스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-129">The resource id of the virtual hub resource.</span></span>

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

### <span data-ttu-id="15f19-130">-경로</span><span class="sxs-lookup"><span data-stu-id="15f19-130">-Route</span></span>
<span data-ttu-id="15f19-131">이 경로 테이블에 대 한 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-131">The list of routes for this route table.</span></span>

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

### <span data-ttu-id="15f19-132">-확인</span><span class="sxs-lookup"><span data-stu-id="15f19-132">-Confirm</span></span>
<span data-ttu-id="15f19-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15f19-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15f19-134">-WhatIf</span></span>
<span data-ttu-id="15f19-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15f19-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15f19-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f19-137">CommonParameters</span></span>
<span data-ttu-id="15f19-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15f19-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f19-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15f19-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f19-140">입력</span><span class="sxs-lookup"><span data-stu-id="15f19-140">INPUTS</span></span>

### <span data-ttu-id="15f19-141">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="15f19-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="15f19-142">PSVHubRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="15f19-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="15f19-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="15f19-143">System.String</span></span>

## <span data-ttu-id="15f19-144">출력</span><span class="sxs-lookup"><span data-stu-id="15f19-144">OUTPUTS</span></span>

### <span data-ttu-id="15f19-145">PSVHubRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="15f19-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="15f19-146">상속자</span><span class="sxs-lookup"><span data-stu-id="15f19-146">NOTES</span></span>

## <span data-ttu-id="15f19-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15f19-147">RELATED LINKS</span></span>

[<span data-ttu-id="15f19-148">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="15f19-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="15f19-149">새로운 AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="15f19-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="15f19-150">제거-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="15f19-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="15f19-151">업데이트-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="15f19-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
