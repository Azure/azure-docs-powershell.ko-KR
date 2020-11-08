---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 7dce18ce266bbd2e92f09039b1772acfc618dbdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203966"
---
# <span data-ttu-id="58c1a-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="58c1a-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="58c1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="58c1a-103">New-AzVHubRouteTable 명령에 매개 변수로 전달 될 수 있는 VHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58c1a-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="58c1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58c1a-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58c1a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="58c1a-105">DESCRIPTION</span></span>

<span data-ttu-id="58c1a-106">VHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58c1a-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="58c1a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="58c1a-107">EXAMPLES</span></span>

### <span data-ttu-id="58c1a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="58c1a-108">Example 1</span></span>

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

<span data-ttu-id="58c1a-109">위의 명령을 사용 하면 nextHop에서 지정한 방화벽으로 VHubRoute 개체를 만든 다음 VHubRouteTable 리소스에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58c1a-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="58c1a-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="58c1a-110">Example 2</span></span>

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

<span data-ttu-id="58c1a-111">위의 명령을 사용 하면 nextHop VHubRoute 개체가 생성 되어 VHubRouteTable 리소스에 추가 될 수 있는 지정 된 hubVnetConnection.</span><span class="sxs-lookup"><span data-stu-id="58c1a-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>

## <span data-ttu-id="58c1a-112">변수</span><span class="sxs-lookup"><span data-stu-id="58c1a-112">PARAMETERS</span></span>

### <span data-ttu-id="58c1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c1a-113">-DefaultProfile</span></span>
<span data-ttu-id="58c1a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58c1a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c1a-115">-대상</span><span class="sxs-lookup"><span data-stu-id="58c1a-115">-Destination</span></span>
<span data-ttu-id="58c1a-116">대상의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="58c1a-116">List of Destinations.</span></span>

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

### <span data-ttu-id="58c1a-117">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="58c1a-117">-DestinationType</span></span>
<span data-ttu-id="58c1a-118">대상의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="58c1a-118">Type of Destinations.</span></span>

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

### <span data-ttu-id="58c1a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="58c1a-119">-Name</span></span>
<span data-ttu-id="58c1a-120">경로 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58c1a-120">The route name.</span></span>

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

### <span data-ttu-id="58c1a-121">-NextHop</span><span class="sxs-lookup"><span data-stu-id="58c1a-121">-NextHop</span></span>
<span data-ttu-id="58c1a-122">다음 홉.</span><span class="sxs-lookup"><span data-stu-id="58c1a-122">The next hop.</span></span>

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

### <span data-ttu-id="58c1a-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="58c1a-123">-NextHopType</span></span>
<span data-ttu-id="58c1a-124">다음 홉 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="58c1a-124">The Next Hop type.</span></span>

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

### <span data-ttu-id="58c1a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c1a-125">CommonParameters</span></span>
<span data-ttu-id="58c1a-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c1a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c1a-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58c1a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c1a-128">입력</span><span class="sxs-lookup"><span data-stu-id="58c1a-128">INPUTS</span></span>

### <span data-ttu-id="58c1a-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58c1a-129">System.String</span></span>

## <span data-ttu-id="58c1a-130">출력</span><span class="sxs-lookup"><span data-stu-id="58c1a-130">OUTPUTS</span></span>

### <span data-ttu-id="58c1a-131">PSVHubRoute에 대 한.</span><span class="sxs-lookup"><span data-stu-id="58c1a-131">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="58c1a-132">상속자</span><span class="sxs-lookup"><span data-stu-id="58c1a-132">NOTES</span></span>

## <span data-ttu-id="58c1a-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58c1a-133">RELATED LINKS</span></span>

[<span data-ttu-id="58c1a-134">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="58c1a-134">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="58c1a-135">새로운 AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="58c1a-135">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="58c1a-136">제거-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="58c1a-136">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="58c1a-137">업데이트-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="58c1a-137">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)