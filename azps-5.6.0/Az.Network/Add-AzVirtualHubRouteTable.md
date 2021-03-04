---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5cf2756297a932269f2aee87a248a1ba0eeed20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979744"
---
# <span data-ttu-id="49c9c-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="49c9c-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="49c9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="49c9c-103">VirtualHub의 자식인 Virtual Hub 경로 테이블 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49c9c-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="49c9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="49c9c-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49c9c-105">설명</span><span class="sxs-lookup"><span data-stu-id="49c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="49c9c-106">가상 허브 경로 테이블 리소스에는 경로 목록과 연결될 수 있는 연결 목록이 포함되어 있으며 Virtual Hub에서 트래픽을 라우팅하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="49c9c-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="49c9c-107">예제</span><span class="sxs-lookup"><span data-stu-id="49c9c-107">EXAMPLES</span></span>

### <span data-ttu-id="49c9c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="49c9c-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="49c9c-109">위의 명령은 전달된 경로에서 Virtual Hub 경로 테이블 리소스를 만들고 이 개체를 가상 허브에서 트래픽 라우팅에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49c9c-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="49c9c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49c9c-110">PARAMETERS</span></span>

### <span data-ttu-id="49c9c-111">-Connection</span><span class="sxs-lookup"><span data-stu-id="49c9c-111">-Connection</span></span>
<span data-ttu-id="49c9c-112">이 경로 테이블에 연결된 연결 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="49c9c-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="49c9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c9c-113">-DefaultProfile</span></span>
<span data-ttu-id="49c9c-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49c9c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49c9c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="49c9c-115">-Name</span></span>
<span data-ttu-id="49c9c-116">경로 테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49c9c-116">Name of the route table.</span></span>

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

### <span data-ttu-id="49c9c-117">-Route</span><span class="sxs-lookup"><span data-stu-id="49c9c-117">-Route</span></span>
<span data-ttu-id="49c9c-118">가상 허브 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="49c9c-118">List of virtual hub routes.</span></span>

```yaml
Type: PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c9c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c9c-119">CommonParameters</span></span>
<span data-ttu-id="49c9c-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49c9c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c9c-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49c9c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c9c-122">입력</span><span class="sxs-lookup"><span data-stu-id="49c9c-122">INPUTS</span></span>

### <span data-ttu-id="49c9c-123">없음</span><span class="sxs-lookup"><span data-stu-id="49c9c-123">None</span></span>

## <span data-ttu-id="49c9c-124">출력</span><span class="sxs-lookup"><span data-stu-id="49c9c-124">OUTPUTS</span></span>

### <span data-ttu-id="49c9c-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="49c9c-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="49c9c-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49c9c-126">NOTES</span></span>

## <span data-ttu-id="49c9c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49c9c-127">RELATED LINKS</span></span>
