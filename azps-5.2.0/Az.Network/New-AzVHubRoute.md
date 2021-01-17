---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330614"
---
# <span data-ttu-id="c3b08-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="c3b08-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="c3b08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3b08-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b08-103">VHubRoute 개체를 만듭니다. 이 개체를 매개 변수로 New-AzVHubRouteTable 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="c3b08-104">구문</span><span class="sxs-lookup"><span data-stu-id="c3b08-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3b08-105">설명</span><span class="sxs-lookup"><span data-stu-id="c3b08-105">DESCRIPTION</span></span>

<span data-ttu-id="c3b08-106">VHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="c3b08-107">예제</span><span class="sxs-lookup"><span data-stu-id="c3b08-107">EXAMPLES</span></span>

### <span data-ttu-id="c3b08-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3b08-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="c3b08-109">위의 명령은 지정된 방화벽으로 nextHop을 사용하여 VHubRoute 개체를 만든 다음, VHubRouteTable 리소스에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="c3b08-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="c3b08-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="c3b08-111">위의 명령은 nextHop이 지정된 hubVnetConnection으로 VHubRouteTable 리소스에 추가할 수 있는 VHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="c3b08-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="c3b08-112">Example 3</span></span>
```powershell
PS C:\> $hub = Get-AzVirtualHub -ResourceGroupName {rgname} -Name {virtual-hub-name}
PS C:\> $hubVnetConn = Get-AzVirtualHubVnetConnection -ParentObject $hub -Name {connection-name}
PS C:\> $hubVnetConn
Name                   : conn_2
Id                     : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubVirtualNetworkConnections/conn_2
RemoteVirtualNetwork   : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualNetworks/rVnet_2
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration   : {
                           "AssociatedRouteTable": {
                             "Id": "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                           },
                           "PropagatedRouteTables": {
                             "Labels": [
                               "default"
                             ],
                             "Ids": [
                               {
                                 "Id":
                         "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                               }
                             ]
                           },
                           "VnetRoutes": {
                             "StaticRoutes": []
                           }
                         }
                         
PS C:\> $staticRoute1 = New-AzStaticRoute -Name "static_route1" -AddressPrefix @("10.2.1.0/24", "10.2.3.0/24") -NextHopIpAddress "10.2.0.5"
PS C:\> $routingConfig = $hubVnetConn.RoutingConfiguration
PS C:\> $routingConfig.VnetRoutes.StaticRoutes = @($staticRoute1)
PS C:\> $routingConfig
AssociatedRouteTable  : Microsoft.Azure.Commands.Network.Models.PSResourceId
PropagatedRouteTables : {
                          "Labels": [
                            "default"
                          ],
                          "Ids": [
                            {
                              "Id":
                        "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/rTestHub1/hubRouteTables/defaultRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "static_route1",
                              "AddressPrefixes": [
                                "10.2.1.0/24",
                                "10.2.3.0/24"
                              ],
                              "NextHopIpAddress": "10.2.0.5"
                            }
                          ]
                        }

PS C:\> Update-AzVirtualHubVnetConnection -InputObject $hubVnetConn -RoutingConfiguration $routingConfig
```
<span data-ttu-id="c3b08-113">위의 명령은 기존 AzVHubRoute의 RoutingConfiguration을 얻은 다음 연결에 정적 경로를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="c3b08-114">또는 그 안에 정적 경로를 사용하여 새 연결을 만들 수 있는 경우 여기에서 예제 1을 [참조하세요.](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c3b08-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="c3b08-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3b08-115">PARAMETERS</span></span>

### <span data-ttu-id="c3b08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b08-116">-DefaultProfile</span></span>
<span data-ttu-id="c3b08-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3b08-118">-Destination</span><span class="sxs-lookup"><span data-stu-id="c3b08-118">-Destination</span></span>
<span data-ttu-id="c3b08-119">대상 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-119">List of Destinations.</span></span>

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

### <span data-ttu-id="c3b08-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="c3b08-120">-DestinationType</span></span>
<span data-ttu-id="c3b08-121">대상 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-121">Type of Destinations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b08-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c3b08-122">-Name</span></span>
<span data-ttu-id="c3b08-123">경로 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-123">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b08-124">-NextHop</span><span class="sxs-lookup"><span data-stu-id="c3b08-124">-NextHop</span></span>
<span data-ttu-id="c3b08-125">다음 홉입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-125">The next hop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b08-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="c3b08-126">-NextHopType</span></span>
<span data-ttu-id="c3b08-127">다음 홉 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-127">The Next Hop type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b08-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b08-128">CommonParameters</span></span>
<span data-ttu-id="c3b08-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b08-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b08-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c3b08-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b08-131">입력</span><span class="sxs-lookup"><span data-stu-id="c3b08-131">INPUTS</span></span>

### <span data-ttu-id="c3b08-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c3b08-132">System.String</span></span>

## <span data-ttu-id="c3b08-133">출력</span><span class="sxs-lookup"><span data-stu-id="c3b08-133">OUTPUTS</span></span>

### <span data-ttu-id="c3b08-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="c3b08-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="c3b08-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c3b08-135">NOTES</span></span>

## <span data-ttu-id="c3b08-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3b08-136">RELATED LINKS</span></span>

[<span data-ttu-id="c3b08-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3b08-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="c3b08-138">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3b08-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="c3b08-139">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3b08-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="c3b08-140">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3b08-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)