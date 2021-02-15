---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 9648eb1561ae15501f7a395846f7fda71cf5a1f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193548"
---
# <span data-ttu-id="f08da-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f08da-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="f08da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f08da-102">SYNOPSIS</span></span>
<span data-ttu-id="f08da-103">Azure Virtual Hub 경로 테이블 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f08da-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="f08da-104">구문</span><span class="sxs-lookup"><span data-stu-id="f08da-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f08da-105">설명</span><span class="sxs-lookup"><span data-stu-id="f08da-105">DESCRIPTION</span></span>
<span data-ttu-id="f08da-106">Azure Virtual Hub 경로 테이블 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f08da-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="f08da-107">예제</span><span class="sxs-lookup"><span data-stu-id="f08da-107">EXAMPLES</span></span>

### <span data-ttu-id="f08da-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f08da-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="f08da-109">위의 경우 여러 경로로 구성된 경로 테이블을 만들고 새 가상 허브에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="f08da-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="f08da-110">새 또는 기존 VirtualHub에 경로 테이블을 추가하는 데 사용할 수 있는 메모리 내 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f08da-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="f08da-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f08da-111">PARAMETERS</span></span>

### <span data-ttu-id="f08da-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f08da-112">-DefaultProfile</span></span>
<span data-ttu-id="f08da-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f08da-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f08da-114">-Route</span><span class="sxs-lookup"><span data-stu-id="f08da-114">-Route</span></span>
<span data-ttu-id="f08da-115">가상 허브 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f08da-115">List of virtual hub routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f08da-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f08da-116">CommonParameters</span></span>
<span data-ttu-id="f08da-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f08da-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f08da-118">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f08da-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f08da-119">입력</span><span class="sxs-lookup"><span data-stu-id="f08da-119">INPUTS</span></span>

### <span data-ttu-id="f08da-120">없음</span><span class="sxs-lookup"><span data-stu-id="f08da-120">None</span></span>

## <span data-ttu-id="f08da-121">출력</span><span class="sxs-lookup"><span data-stu-id="f08da-121">OUTPUTS</span></span>

### <span data-ttu-id="f08da-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f08da-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="f08da-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f08da-123">NOTES</span></span>

## <span data-ttu-id="f08da-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f08da-124">RELATED LINKS</span></span>

[<span data-ttu-id="f08da-125">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f08da-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
