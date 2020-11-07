---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 3ccf321a089dbb519293fe6407581aecf32b8157
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700268"
---
# <span data-ttu-id="c6437-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6437-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="c6437-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6437-102">SYNOPSIS</span></span>
<span data-ttu-id="c6437-103">Azure 가상 허브 경로 테이블 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6437-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="c6437-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6437-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6437-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c6437-105">DESCRIPTION</span></span>
<span data-ttu-id="c6437-106">Azure 가상 허브 경로 테이블 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6437-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="c6437-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c6437-107">EXAMPLES</span></span>

### <span data-ttu-id="c6437-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6437-108">Example 1</span></span>

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

<span data-ttu-id="c6437-109">위의 방법을 통해 여러 경로로 구성 되 고 새 가상 허브에 연결 된 경로 테이블을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6437-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="c6437-110">이것은 새 또는 기존 VirtualHub에 경로 테이블을 추가 하는 데 사용할 수 있는 메모리 내 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c6437-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="c6437-111">변수</span><span class="sxs-lookup"><span data-stu-id="c6437-111">PARAMETERS</span></span>

### <span data-ttu-id="c6437-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6437-112">-DefaultProfile</span></span>
<span data-ttu-id="c6437-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6437-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6437-114">-경로</span><span class="sxs-lookup"><span data-stu-id="c6437-114">-Route</span></span>
<span data-ttu-id="c6437-115">가상 허브 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c6437-115">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="c6437-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6437-116">CommonParameters</span></span>
<span data-ttu-id="c6437-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6437-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6437-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6437-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6437-119">입력</span><span class="sxs-lookup"><span data-stu-id="c6437-119">INPUTS</span></span>

### <span data-ttu-id="c6437-120">않아야</span><span class="sxs-lookup"><span data-stu-id="c6437-120">None</span></span>

## <span data-ttu-id="c6437-121">출력</span><span class="sxs-lookup"><span data-stu-id="c6437-121">OUTPUTS</span></span>

### <span data-ttu-id="c6437-122">PSVirtualHubRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c6437-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="c6437-123">상속자</span><span class="sxs-lookup"><span data-stu-id="c6437-123">NOTES</span></span>

## <span data-ttu-id="c6437-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6437-124">RELATED LINKS</span></span>

[<span data-ttu-id="c6437-125">새로운 AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="c6437-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
