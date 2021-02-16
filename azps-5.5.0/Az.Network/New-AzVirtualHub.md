---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: d005ef841828dc1fe37915c4a7b0d28ad93e3b44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179572"
---
# <span data-ttu-id="0dee1-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0dee1-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="0dee1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dee1-102">SYNOPSIS</span></span>
<span data-ttu-id="0dee1-103">Azure VirtualHub 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="0dee1-104">구문</span><span class="sxs-lookup"><span data-stu-id="0dee1-104">SYNTAX</span></span>

### <span data-ttu-id="0dee1-105">ByVirtualWanObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="0dee1-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dee1-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="0dee1-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dee1-107">설명</span><span class="sxs-lookup"><span data-stu-id="0dee1-107">DESCRIPTION</span></span>
<span data-ttu-id="0dee1-108">Azure VirtualHub 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="0dee1-109">예제</span><span class="sxs-lookup"><span data-stu-id="0dee1-109">EXAMPLES</span></span>

### <span data-ttu-id="0dee1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0dee1-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="0dee1-111">위의 경우 Azure의 해당 리소스 그룹에 리소스 그룹 "testRG", Virtual WAN 및 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="0dee1-112">가상 허브의 주소 공간은 "10.0.1.0/24"입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="0dee1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0dee1-113">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="0dee1-114">위의 경우 Azure의 해당 리소스 그룹에 리소스 그룹 "testRG", Virtual WAN 및 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="0dee1-115">가상 허브의 주소 공간은 "10.0.1.0/24"입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="0dee1-116">이 예제는 예제 1과 유사하지만 리소스 ID를 사용하여 가상 허브를 만드는 데 필요한 Virtual WAN을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="0dee1-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="0dee1-117">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="0dee1-118">위의 경우 Azure의 해당 리소스 그룹에 리소스 그룹 "testRG", Virtual WAN 및 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="0dee1-119">가상 허브에는 주소 공간 "10.0.1.0/24"가 있으며 경로 테이블이 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="0dee1-120">이 예제는 예제 2와 유사하지만 가상 허브에 경로 테이블을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="0dee1-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dee1-121">PARAMETERS</span></span>

### <span data-ttu-id="0dee1-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0dee1-122">-AddressPrefix</span></span>
<span data-ttu-id="0dee1-123">이 가상 허브에 대한 주소 공간 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="0dee1-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0dee1-124">-AsJob</span></span>
<span data-ttu-id="0dee1-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0dee1-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0dee1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dee1-126">-DefaultProfile</span></span>
<span data-ttu-id="0dee1-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dee1-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0dee1-128">-HubVnetConnection</span></span>
<span data-ttu-id="0dee1-129">이 가상 허브와 연결된 허브 가상 네트워크 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dee1-130">-Location</span><span class="sxs-lookup"><span data-stu-id="0dee1-130">-Location</span></span>
<span data-ttu-id="0dee1-131">위치.</span><span class="sxs-lookup"><span data-stu-id="0dee1-131">location.</span></span>

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

### <span data-ttu-id="0dee1-132">-Name</span><span class="sxs-lookup"><span data-stu-id="0dee1-132">-Name</span></span>
<span data-ttu-id="0dee1-133">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dee1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dee1-134">-ResourceGroupName</span></span>
<span data-ttu-id="0dee1-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-135">The resource group name.</span></span>

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

### <span data-ttu-id="0dee1-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="0dee1-136">-RouteTable</span></span>
<span data-ttu-id="0dee1-137">이 가상 허브와 연결된 경로 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dee1-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="0dee1-138">-Sku</span></span>
<span data-ttu-id="0dee1-139">가상 허브의 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-139">The sku of the Virtual Hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dee1-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="0dee1-140">-Tag</span></span>
<span data-ttu-id="0dee1-141">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0dee1-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="0dee1-142">-VirtualWan</span></span>
<span data-ttu-id="0dee1-143">이 허브가 연결된 가상 wan 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-143">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dee1-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="0dee1-144">-VirtualWanId</span></span>
<span data-ttu-id="0dee1-145">이 허브가 연결된 가상 wan 개체의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-145">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dee1-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dee1-146">-Confirm</span></span>
<span data-ttu-id="0dee1-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dee1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dee1-148">-WhatIf</span></span>
<span data-ttu-id="0dee1-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0dee1-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dee1-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dee1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dee1-151">CommonParameters</span></span>
<span data-ttu-id="0dee1-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dee1-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0dee1-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dee1-154">입력</span><span class="sxs-lookup"><span data-stu-id="0dee1-154">INPUTS</span></span>

### <span data-ttu-id="0dee1-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0dee1-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="0dee1-156">System.String</span><span class="sxs-lookup"><span data-stu-id="0dee1-156">System.String</span></span>

## <span data-ttu-id="0dee1-157">출력</span><span class="sxs-lookup"><span data-stu-id="0dee1-157">OUTPUTS</span></span>

### <span data-ttu-id="0dee1-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0dee1-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="0dee1-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0dee1-159">NOTES</span></span>

## <span data-ttu-id="0dee1-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0dee1-160">RELATED LINKS</span></span>

[<span data-ttu-id="0dee1-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0dee1-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="0dee1-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0dee1-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="0dee1-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0dee1-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
