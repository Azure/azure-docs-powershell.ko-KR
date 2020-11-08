---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042539"
---
# <span data-ttu-id="69163-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="69163-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="69163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69163-102">SYNOPSIS</span></span>
<span data-ttu-id="69163-103">VirtualHub의 자식인 가상 허브 경로 테이블 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69163-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="69163-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69163-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69163-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69163-105">DESCRIPTION</span></span>
<span data-ttu-id="69163-106">가상 허브 경로 테이블 리소스에는 경로 목록과 연결 될 수 있는 연결 목록이 포함 되며, 가상 허브에서 트래픽을 라우팅하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69163-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="69163-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69163-107">EXAMPLES</span></span>

### <span data-ttu-id="69163-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="69163-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="69163-109">위의 명령으로 전달 된 경로에서 가상 허브 경로 테이블 리소스를 만들고,이 개체를 사용 하 여 가상 허브에서 트래픽 라우팅에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69163-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="69163-110">변수</span><span class="sxs-lookup"><span data-stu-id="69163-110">PARAMETERS</span></span>

### <span data-ttu-id="69163-111">-연결</span><span class="sxs-lookup"><span data-stu-id="69163-111">-Connection</span></span>
<span data-ttu-id="69163-112">이 경로 테이블이 연결 된 연결 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="69163-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="69163-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69163-113">-DefaultProfile</span></span>
<span data-ttu-id="69163-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69163-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69163-115">-이름</span><span class="sxs-lookup"><span data-stu-id="69163-115">-Name</span></span>
<span data-ttu-id="69163-116">경로 테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69163-116">Name of the route table.</span></span>

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

### <span data-ttu-id="69163-117">-경로</span><span class="sxs-lookup"><span data-stu-id="69163-117">-Route</span></span>
<span data-ttu-id="69163-118">가상 허브 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="69163-118">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="69163-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69163-119">CommonParameters</span></span>
<span data-ttu-id="69163-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69163-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69163-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69163-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69163-122">입력</span><span class="sxs-lookup"><span data-stu-id="69163-122">INPUTS</span></span>

### <span data-ttu-id="69163-123">않아야</span><span class="sxs-lookup"><span data-stu-id="69163-123">None</span></span>

## <span data-ttu-id="69163-124">출력</span><span class="sxs-lookup"><span data-stu-id="69163-124">OUTPUTS</span></span>

### <span data-ttu-id="69163-125">PSVirtualHubRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="69163-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="69163-126">상속자</span><span class="sxs-lookup"><span data-stu-id="69163-126">NOTES</span></span>

## <span data-ttu-id="69163-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69163-127">RELATED LINKS</span></span>
