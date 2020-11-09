---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: 31601c93a6979d09dfb3641cac079cba2757d043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309530"
---
# <span data-ttu-id="ad45f-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad45f-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="ad45f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad45f-102">SYNOPSIS</span></span>
<span data-ttu-id="ad45f-103">RoutingConfiguration 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad45f-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="ad45f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad45f-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad45f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ad45f-105">DESCRIPTION</span></span>
<span data-ttu-id="ad45f-106">RoutingConfiguration 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad45f-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="ad45f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ad45f-107">EXAMPLES</span></span>

### <span data-ttu-id="ad45f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad45f-108">Example 1</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
```

<span data-ttu-id="ad45f-109">위의 명령은 연결 리소스에 추가 될 수 있는 RoutingConfiguration 개체를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ad45f-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="ad45f-110">Static 경로는 HubVirtualNetworkConnection 개체 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad45f-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="ad45f-111">변수</span><span class="sxs-lookup"><span data-stu-id="ad45f-111">PARAMETERS</span></span>

### <span data-ttu-id="ad45f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad45f-112">-DefaultProfile</span></span>
<span data-ttu-id="ad45f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad45f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad45f-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad45f-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="ad45f-115">이 라우팅 구성과 연결 된 허브 경로 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="ad45f-115">The hub route table associated with this routing configuration.</span></span>

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

### <span data-ttu-id="ad45f-116">-Id</span><span class="sxs-lookup"><span data-stu-id="ad45f-116">-Id</span></span>
<span data-ttu-id="ad45f-117">PropagatedRouteTables 속성에 대 한 경로를 광고 하는 모든 허브 경로 테이블의 리소스 id 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ad45f-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="ad45f-118">-레이블</span><span class="sxs-lookup"><span data-stu-id="ad45f-118">-Label</span></span>
<span data-ttu-id="ad45f-119">PropagatedRouteTables 속성에 대 한 레이블 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ad45f-119">The list of labels for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad45f-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="ad45f-120">-StaticRoute</span></span>
<span data-ttu-id="ad45f-121">VirtualHub에서 가상 네트워크 연결로의 라우팅을 제어 하는 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ad45f-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

```yaml
Type: PSStaticRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad45f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad45f-122">CommonParameters</span></span>
<span data-ttu-id="ad45f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad45f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad45f-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad45f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad45f-125">입력</span><span class="sxs-lookup"><span data-stu-id="ad45f-125">INPUTS</span></span>

### <span data-ttu-id="ad45f-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad45f-126">System.String</span></span>

### <span data-ttu-id="ad45f-127">Microsoft. 네트워크 모델. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="ad45f-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="ad45f-128">출력</span><span class="sxs-lookup"><span data-stu-id="ad45f-128">OUTPUTS</span></span>

### <span data-ttu-id="ad45f-129">Microsoft. 네트워크 모델. PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad45f-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="ad45f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="ad45f-130">NOTES</span></span>

## <span data-ttu-id="ad45f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad45f-131">RELATED LINKS</span></span>

[<span data-ttu-id="ad45f-132">새로운 AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="ad45f-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="ad45f-133">새로운 AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="ad45f-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="ad45f-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="ad45f-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="ad45f-135">새로운 AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ad45f-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="ad45f-136">업데이트-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ad45f-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="ad45f-137">새로운 AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ad45f-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="ad45f-138">업데이트-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ad45f-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="ad45f-139">새로운 AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ad45f-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="ad45f-140">업데이트-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ad45f-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)