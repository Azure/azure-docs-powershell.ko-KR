---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: b67b37f66e9b13c692b10dbdca54230bc1b0a529
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953883"
---
# <span data-ttu-id="ba4e6-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba4e6-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="ba4e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ba4e6-103">라우팅 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba4e6-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="ba4e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba4e6-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba4e6-105">설명</span><span class="sxs-lookup"><span data-stu-id="ba4e6-105">DESCRIPTION</span></span>
<span data-ttu-id="ba4e6-106">라우팅 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba4e6-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="ba4e6-107">예제</span><span class="sxs-lookup"><span data-stu-id="ba4e6-107">EXAMPLES</span></span>

### <span data-ttu-id="ba4e6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba4e6-108">Example 1</span></span>
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

<span data-ttu-id="ba4e6-109">위의 명령은 연결 리소스에 추가할 수 있는 라우팅Configuration 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba4e6-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="ba4e6-110">정적 경로는 HubVirtualNetworkConnection 개체로만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba4e6-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="ba4e6-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ba4e6-111">PARAMETERS</span></span>

### <span data-ttu-id="ba4e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4e6-112">-DefaultProfile</span></span>
<span data-ttu-id="ba4e6-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba4e6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba4e6-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="ba4e6-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="ba4e6-115">이 라우팅 구성과 연결된 허브 경로 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="ba4e6-115">The hub route table associated with this routing configuration.</span></span>

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

### <span data-ttu-id="ba4e6-116">-Id</span><span class="sxs-lookup"><span data-stu-id="ba4e6-116">-Id</span></span>
<span data-ttu-id="ba4e6-117">PropagatedRouteTables 속성에 대한 경로를 보급할 모든 허브 경로 테이블의 리소스 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ba4e6-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="ba4e6-118">-Label</span><span class="sxs-lookup"><span data-stu-id="ba4e6-118">-Label</span></span>
<span data-ttu-id="ba4e6-119">PropagatedRouteTables 속성에 대한 레이블 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ba4e6-119">The list of labels for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="ba4e6-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="ba4e6-120">-StaticRoute</span></span>
<span data-ttu-id="ba4e6-121">VirtualHub에서 가상 네트워크 연결로 라우팅을 제어하는 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ba4e6-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

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

### <span data-ttu-id="ba4e6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4e6-122">CommonParameters</span></span>
<span data-ttu-id="ba4e6-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba4e6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4e6-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba4e6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4e6-125">입력</span><span class="sxs-lookup"><span data-stu-id="ba4e6-125">INPUTS</span></span>

### <span data-ttu-id="ba4e6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ba4e6-126">System.String</span></span>

### <span data-ttu-id="ba4e6-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="ba4e6-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="ba4e6-128">출력</span><span class="sxs-lookup"><span data-stu-id="ba4e6-128">OUTPUTS</span></span>

### <span data-ttu-id="ba4e6-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba4e6-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="ba4e6-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba4e6-130">NOTES</span></span>

## <span data-ttu-id="ba4e6-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba4e6-131">RELATED LINKS</span></span>

[<span data-ttu-id="ba4e6-132">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="ba4e6-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="ba4e6-133">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="ba4e6-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="ba4e6-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="ba4e6-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="ba4e6-135">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ba4e6-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="ba4e6-136">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ba4e6-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="ba4e6-137">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ba4e6-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="ba4e6-138">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ba4e6-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="ba4e6-139">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ba4e6-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="ba4e6-140">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ba4e6-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)