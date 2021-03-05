---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: a7b8e790892b14e053a07f83e6a27c4ce82c00ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984405"
---
# <span data-ttu-id="08ec0-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="08ec0-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="08ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="08ec0-103">Azure VirtualHub 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="08ec0-104">구문</span><span class="sxs-lookup"><span data-stu-id="08ec0-104">SYNTAX</span></span>

### <span data-ttu-id="08ec0-105">ByVirtualWanObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="08ec0-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08ec0-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="08ec0-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08ec0-107">설명</span><span class="sxs-lookup"><span data-stu-id="08ec0-107">DESCRIPTION</span></span>
<span data-ttu-id="08ec0-108">Azure VirtualHub 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="08ec0-109">예제</span><span class="sxs-lookup"><span data-stu-id="08ec0-109">EXAMPLES</span></span>

### <span data-ttu-id="08ec0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="08ec0-110">Example 1</span></span>

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

<span data-ttu-id="08ec0-111">위의 리소스 그룹 "testRG", Virtual WAN 및 Azure의 해당 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="08ec0-112">가상 허브에는 주소 공간이 "10.0.1.0/24"가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="08ec0-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="08ec0-113">Example 2</span></span>

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

<span data-ttu-id="08ec0-114">위의 리소스 그룹 "testRG", Virtual WAN 및 Azure의 해당 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="08ec0-115">가상 허브에는 주소 공간이 "10.0.1.0/24"가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="08ec0-116">이 예제는 예제 1과 비슷하지만 리소스 ID를 사용하여 가상 허브를 만드는 데 필요한 Virtual WAN을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="08ec0-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="08ec0-117">Example 3</span></span>

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

<span data-ttu-id="08ec0-118">위의 리소스 그룹 "testRG", Virtual WAN 및 Azure의 해당 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="08ec0-119">가상 허브에는 주소 공간 "10.0.1.0/24" 및 경로 테이블이 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="08ec0-120">이 예제는 예제 2와 비슷하지만 가상 허브에 경로 테이블을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="08ec0-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="08ec0-121">PARAMETERS</span></span>

### <span data-ttu-id="08ec0-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="08ec0-122">-AddressPrefix</span></span>
<span data-ttu-id="08ec0-123">이 가상 허브의 주소 공간 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="08ec0-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08ec0-124">-AsJob</span></span>
<span data-ttu-id="08ec0-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="08ec0-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08ec0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ec0-126">-DefaultProfile</span></span>
<span data-ttu-id="08ec0-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08ec0-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="08ec0-128">-HubVnetConnection</span></span>
<span data-ttu-id="08ec0-129">이 Virtual Hub와 연결된 허브 가상 네트워크 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="08ec0-130">-Location</span><span class="sxs-lookup"><span data-stu-id="08ec0-130">-Location</span></span>
<span data-ttu-id="08ec0-131">위치.</span><span class="sxs-lookup"><span data-stu-id="08ec0-131">location.</span></span>

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

### <span data-ttu-id="08ec0-132">-Name</span><span class="sxs-lookup"><span data-stu-id="08ec0-132">-Name</span></span>
<span data-ttu-id="08ec0-133">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-133">The resource name.</span></span>

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

### <span data-ttu-id="08ec0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08ec0-134">-ResourceGroupName</span></span>
<span data-ttu-id="08ec0-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-135">The resource group name.</span></span>

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

### <span data-ttu-id="08ec0-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="08ec0-136">-RouteTable</span></span>
<span data-ttu-id="08ec0-137">이 Virtual Hub와 연결된 경로 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-137">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="08ec0-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="08ec0-138">-Sku</span></span>
<span data-ttu-id="08ec0-139">Virtual Hub의 sku입니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-139">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="08ec0-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="08ec0-140">-Tag</span></span>
<span data-ttu-id="08ec0-141">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="08ec0-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="08ec0-142">-VirtualWan</span></span>
<span data-ttu-id="08ec0-143">이 허브가 연결된 가상 wan 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-143">The virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="08ec0-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="08ec0-144">-VirtualWanId</span></span>
<span data-ttu-id="08ec0-145">이 허브가 연결된 가상 wan 개체의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-145">The id of virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="08ec0-146">-확인</span><span class="sxs-lookup"><span data-stu-id="08ec0-146">-Confirm</span></span>
<span data-ttu-id="08ec0-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08ec0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08ec0-148">-WhatIf</span></span>
<span data-ttu-id="08ec0-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08ec0-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08ec0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ec0-151">CommonParameters</span></span>
<span data-ttu-id="08ec0-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="08ec0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ec0-153">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08ec0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ec0-154">입력</span><span class="sxs-lookup"><span data-stu-id="08ec0-154">INPUTS</span></span>

### <span data-ttu-id="08ec0-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="08ec0-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="08ec0-156">System.String</span><span class="sxs-lookup"><span data-stu-id="08ec0-156">System.String</span></span>

## <span data-ttu-id="08ec0-157">출력</span><span class="sxs-lookup"><span data-stu-id="08ec0-157">OUTPUTS</span></span>

### <span data-ttu-id="08ec0-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="08ec0-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="08ec0-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="08ec0-159">NOTES</span></span>

## <span data-ttu-id="08ec0-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08ec0-160">RELATED LINKS</span></span>

[<span data-ttu-id="08ec0-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="08ec0-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="08ec0-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="08ec0-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="08ec0-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="08ec0-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
