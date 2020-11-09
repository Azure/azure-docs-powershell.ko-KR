---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309505"
---
# <span data-ttu-id="221e1-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="221e1-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="221e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="221e1-102">SYNOPSIS</span></span>
<span data-ttu-id="221e1-103">New-AzVHubRouteTable 명령에 매개 변수로 전달 될 수 있는 VHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="221e1-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="221e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="221e1-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="221e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="221e1-105">DESCRIPTION</span></span>

<span data-ttu-id="221e1-106">VHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="221e1-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="221e1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="221e1-107">EXAMPLES</span></span>

### <span data-ttu-id="221e1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="221e1-108">Example 1</span></span>

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

<span data-ttu-id="221e1-109">위의 명령을 사용 하면 nextHop에서 지정한 방화벽으로 VHubRoute 개체를 만든 다음 VHubRouteTable 리소스에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="221e1-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="221e1-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="221e1-110">Example 2</span></span>

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

<span data-ttu-id="221e1-111">위의 명령을 사용 하면 nextHop VHubRoute 개체가 생성 되어 VHubRouteTable 리소스에 추가 될 수 있는 지정 된 hubVnetConnection.</span><span class="sxs-lookup"><span data-stu-id="221e1-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="221e1-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="221e1-112">Example 3</span></span>
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
<span data-ttu-id="221e1-113">위의 명령은 이미 존재 하는 AzVHubRoute의 RoutingConfiguration을 얻은 다음 연결에 고정 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="221e1-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="221e1-114">또는 그 안의 고정 경로를 사용 하 여 새 연결을 만들려는 경우 여기에 예제 1을 참조 하세요 [.](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="221e1-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="221e1-115">변수</span><span class="sxs-lookup"><span data-stu-id="221e1-115">PARAMETERS</span></span>

### <span data-ttu-id="221e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="221e1-116">-DefaultProfile</span></span>
<span data-ttu-id="221e1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="221e1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="221e1-118">-대상</span><span class="sxs-lookup"><span data-stu-id="221e1-118">-Destination</span></span>
<span data-ttu-id="221e1-119">대상의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="221e1-119">List of Destinations.</span></span>

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

### <span data-ttu-id="221e1-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="221e1-120">-DestinationType</span></span>
<span data-ttu-id="221e1-121">대상의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="221e1-121">Type of Destinations.</span></span>

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

### <span data-ttu-id="221e1-122">-이름</span><span class="sxs-lookup"><span data-stu-id="221e1-122">-Name</span></span>
<span data-ttu-id="221e1-123">경로 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="221e1-123">The route name.</span></span>

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

### <span data-ttu-id="221e1-124">-NextHop</span><span class="sxs-lookup"><span data-stu-id="221e1-124">-NextHop</span></span>
<span data-ttu-id="221e1-125">다음 홉.</span><span class="sxs-lookup"><span data-stu-id="221e1-125">The next hop.</span></span>

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

### <span data-ttu-id="221e1-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="221e1-126">-NextHopType</span></span>
<span data-ttu-id="221e1-127">다음 홉 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="221e1-127">The Next Hop type.</span></span>

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

### <span data-ttu-id="221e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="221e1-128">CommonParameters</span></span>
<span data-ttu-id="221e1-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="221e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="221e1-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="221e1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="221e1-131">입력</span><span class="sxs-lookup"><span data-stu-id="221e1-131">INPUTS</span></span>

### <span data-ttu-id="221e1-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="221e1-132">System.String</span></span>

## <span data-ttu-id="221e1-133">출력</span><span class="sxs-lookup"><span data-stu-id="221e1-133">OUTPUTS</span></span>

### <span data-ttu-id="221e1-134">PSVHubRoute에 대 한.</span><span class="sxs-lookup"><span data-stu-id="221e1-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="221e1-135">상속자</span><span class="sxs-lookup"><span data-stu-id="221e1-135">NOTES</span></span>

## <span data-ttu-id="221e1-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="221e1-136">RELATED LINKS</span></span>

[<span data-ttu-id="221e1-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="221e1-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="221e1-138">새로운 AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="221e1-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="221e1-139">제거-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="221e1-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="221e1-140">업데이트-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="221e1-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)