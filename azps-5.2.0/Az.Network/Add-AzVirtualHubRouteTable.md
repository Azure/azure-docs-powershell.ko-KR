---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359696"
---
# <span data-ttu-id="97ba9-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="97ba9-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="97ba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="97ba9-103">VirtualHub의 자식인 가상 허브 경로 테이블 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97ba9-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="97ba9-104">구문</span><span class="sxs-lookup"><span data-stu-id="97ba9-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97ba9-105">설명</span><span class="sxs-lookup"><span data-stu-id="97ba9-105">DESCRIPTION</span></span>
<span data-ttu-id="97ba9-106">가상 허브 경로 테이블 리소스에는 연결될 수 있는 경로 목록 및 연결 목록이 포함되어 있으며 가상 허브에서 트래픽을 라우팅하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="97ba9-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="97ba9-107">예제</span><span class="sxs-lookup"><span data-stu-id="97ba9-107">EXAMPLES</span></span>

### <span data-ttu-id="97ba9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="97ba9-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="97ba9-109">위의 명령은 전달된 경로에서 Virtual Hub 경로 테이블 리소스를 만들고 가상 허브에서 트래픽을 라우팅하는 데 이 개체를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97ba9-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="97ba9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97ba9-110">PARAMETERS</span></span>

### <span data-ttu-id="97ba9-111">-Connection</span><span class="sxs-lookup"><span data-stu-id="97ba9-111">-Connection</span></span>
<span data-ttu-id="97ba9-112">이 경로 테이블이 연결된 연결 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="97ba9-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="97ba9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ba9-113">-DefaultProfile</span></span>
<span data-ttu-id="97ba9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97ba9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97ba9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="97ba9-115">-Name</span></span>
<span data-ttu-id="97ba9-116">경로 테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97ba9-116">Name of the route table.</span></span>

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

### <span data-ttu-id="97ba9-117">-Route</span><span class="sxs-lookup"><span data-stu-id="97ba9-117">-Route</span></span>
<span data-ttu-id="97ba9-118">가상 허브 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="97ba9-118">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="97ba9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ba9-119">CommonParameters</span></span>
<span data-ttu-id="97ba9-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="97ba9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ba9-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="97ba9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ba9-122">입력</span><span class="sxs-lookup"><span data-stu-id="97ba9-122">INPUTS</span></span>

### <span data-ttu-id="97ba9-123">없음</span><span class="sxs-lookup"><span data-stu-id="97ba9-123">None</span></span>

## <span data-ttu-id="97ba9-124">출력</span><span class="sxs-lookup"><span data-stu-id="97ba9-124">OUTPUTS</span></span>

### <span data-ttu-id="97ba9-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="97ba9-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="97ba9-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="97ba9-126">NOTES</span></span>

## <span data-ttu-id="97ba9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97ba9-127">RELATED LINKS</span></span>
