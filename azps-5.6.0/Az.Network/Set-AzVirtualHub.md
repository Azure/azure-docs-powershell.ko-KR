---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: a23b2ce975a67a87a5edd58b21835e16f812055b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971888"
---
# <span data-ttu-id="33464-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="33464-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="33464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33464-102">SYNOPSIS</span></span>
<span data-ttu-id="33464-103">Virtual Hub를 수정하여 Virtual HUb 경로 테이블을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="33464-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="33464-104">구문</span><span class="sxs-lookup"><span data-stu-id="33464-104">SYNTAX</span></span>

### <span data-ttu-id="33464-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="33464-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33464-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="33464-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33464-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="33464-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33464-108">설명</span><span class="sxs-lookup"><span data-stu-id="33464-108">DESCRIPTION</span></span>
<span data-ttu-id="33464-109">{{ 설명 }} 채우기</span><span class="sxs-lookup"><span data-stu-id="33464-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="33464-110">예제</span><span class="sxs-lookup"><span data-stu-id="33464-110">EXAMPLES</span></span>

### <span data-ttu-id="33464-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="33464-111">Example 1</span></span>
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

<span data-ttu-id="33464-112">먼저 가상 허브 경로 개체를 만들고 이를 사용하여 Virtual Hub 경로 테이블 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33464-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="33464-113">그런 다음, 이 경로 테이블 리소스를 Set-AzVirtualHub 가상 허브로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="33464-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="33464-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="33464-114">PARAMETERS</span></span>

### <span data-ttu-id="33464-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33464-115">-AsJob</span></span>
<span data-ttu-id="33464-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="33464-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33464-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33464-117">-DefaultProfile</span></span>
<span data-ttu-id="33464-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33464-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33464-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33464-119">-InputObject</span></span>
<span data-ttu-id="33464-120">수정할 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="33464-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="33464-121">-Name</span><span class="sxs-lookup"><span data-stu-id="33464-121">-Name</span></span>
<span data-ttu-id="33464-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33464-122">The resource name.</span></span>

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

### <span data-ttu-id="33464-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33464-123">-ResourceGroupName</span></span>
<span data-ttu-id="33464-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33464-124">The resource group name.</span></span>

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

### <span data-ttu-id="33464-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33464-125">-ResourceId</span></span>
<span data-ttu-id="33464-126">수정할 가상 허브의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="33464-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="33464-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="33464-127">-RouteTable</span></span>
<span data-ttu-id="33464-128">이 Virtual Hub와 연결된 경로 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="33464-128">The route tables associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="33464-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="33464-129">-Tag</span></span>
<span data-ttu-id="33464-130">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="33464-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="33464-131">-확인</span><span class="sxs-lookup"><span data-stu-id="33464-131">-Confirm</span></span>
<span data-ttu-id="33464-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="33464-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33464-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33464-133">-WhatIf</span></span>
<span data-ttu-id="33464-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="33464-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33464-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33464-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33464-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33464-136">CommonParameters</span></span>
<span data-ttu-id="33464-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="33464-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33464-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33464-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33464-139">입력</span><span class="sxs-lookup"><span data-stu-id="33464-139">INPUTS</span></span>

### <span data-ttu-id="33464-140">System.String</span><span class="sxs-lookup"><span data-stu-id="33464-140">System.String</span></span>

### <span data-ttu-id="33464-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="33464-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="33464-142">출력</span><span class="sxs-lookup"><span data-stu-id="33464-142">OUTPUTS</span></span>

### <span data-ttu-id="33464-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="33464-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="33464-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="33464-144">NOTES</span></span>

## <span data-ttu-id="33464-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33464-145">RELATED LINKS</span></span>
