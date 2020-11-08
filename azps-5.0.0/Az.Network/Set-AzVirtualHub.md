---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218504"
---
# <span data-ttu-id="ea6c6-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ea6c6-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="ea6c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea6c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ea6c6-103">가상 허브에 가상 허브 경로 테이블을 추가 하려면이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="ea6c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea6c6-104">SYNTAX</span></span>

### <span data-ttu-id="ea6c6-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea6c6-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea6c6-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ea6c6-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea6c6-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ea6c6-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea6c6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ea6c6-108">DESCRIPTION</span></span>
<span data-ttu-id="ea6c6-109">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="ea6c6-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="ea6c6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ea6c6-110">EXAMPLES</span></span>

### <span data-ttu-id="ea6c6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ea6c6-111">Example 1</span></span>
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

<span data-ttu-id="ea6c6-112">먼저 가상 허브 경로 개체를 만들고이를 사용 하 여 가상 허브 라우팅 테이블 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="ea6c6-113">그런 다음 Set-AzVirtualHub 명령을 사용 하 여이 경로 테이블 리소스를 가상 허브로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="ea6c6-114">변수</span><span class="sxs-lookup"><span data-stu-id="ea6c6-114">PARAMETERS</span></span>

### <span data-ttu-id="ea6c6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea6c6-115">-AsJob</span></span>
<span data-ttu-id="ea6c6-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ea6c6-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea6c6-117">-DefaultProfile</span></span>
<span data-ttu-id="ea6c6-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea6c6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea6c6-119">-InputObject</span></span>
<span data-ttu-id="ea6c6-120">수정할 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-120">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c6-121">-이름</span><span class="sxs-lookup"><span data-stu-id="ea6c6-121">-Name</span></span>
<span data-ttu-id="ea6c6-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea6c6-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea6c6-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea6c6-125">-ResourceId</span></span>
<span data-ttu-id="ea6c6-126">수정할 가상 허브의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-126">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c6-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ea6c6-127">-RouteTable</span></span>
<span data-ttu-id="ea6c6-128">이 가상 허브와 연결 된 경로 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-128">The route tables associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c6-129">태그</span><span class="sxs-lookup"><span data-stu-id="ea6c6-129">-Tag</span></span>
<span data-ttu-id="ea6c6-130">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c6-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ea6c6-131">-Confirm</span></span>
<span data-ttu-id="ea6c6-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea6c6-133">-WhatIf</span></span>
<span data-ttu-id="ea6c6-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea6c6-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea6c6-136">CommonParameters</span></span>
<span data-ttu-id="ea6c6-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea6c6-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea6c6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea6c6-139">입력</span><span class="sxs-lookup"><span data-stu-id="ea6c6-139">INPUTS</span></span>

### <span data-ttu-id="ea6c6-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea6c6-140">System.String</span></span>

### <span data-ttu-id="ea6c6-141">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ea6c6-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="ea6c6-142">출력</span><span class="sxs-lookup"><span data-stu-id="ea6c6-142">OUTPUTS</span></span>

### <span data-ttu-id="ea6c6-143">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ea6c6-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="ea6c6-144">상속자</span><span class="sxs-lookup"><span data-stu-id="ea6c6-144">NOTES</span></span>

## <span data-ttu-id="ea6c6-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea6c6-145">RELATED LINKS</span></span>
