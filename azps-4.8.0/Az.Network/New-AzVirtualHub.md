---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: d005ef841828dc1fe37915c4a7b0d28ad93e3b44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203965"
---
# <span data-ttu-id="788c9-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="788c9-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="788c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="788c9-102">SYNOPSIS</span></span>
<span data-ttu-id="788c9-103">Azure VirtualHub 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="788c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="788c9-104">SYNTAX</span></span>

### <span data-ttu-id="788c9-105">ByVirtualWanObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="788c9-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="788c9-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="788c9-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="788c9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="788c9-107">DESCRIPTION</span></span>
<span data-ttu-id="788c9-108">Azure VirtualHub 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="788c9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="788c9-109">EXAMPLES</span></span>

### <span data-ttu-id="788c9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="788c9-110">Example 1</span></span>

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

<span data-ttu-id="788c9-111">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="788c9-112">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="788c9-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="788c9-113">Example 2</span></span>

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

<span data-ttu-id="788c9-114">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="788c9-115">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="788c9-116">이 예제는 예제 1과 비슷하지만, 리소스 Id를 사용 하 여 가상 허브를 만드는 데 필요한 가상 WAN을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="788c9-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="788c9-117">Example 3</span></span>

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

<span data-ttu-id="788c9-118">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="788c9-119">가상 허브에는 주소 공간 "10.0.1.0/24"와 경로 테이블이 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="788c9-120">이 예제는 예제 2와 유사 하지만, 가상 허브에도 경로 테이블을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="788c9-121">변수</span><span class="sxs-lookup"><span data-stu-id="788c9-121">PARAMETERS</span></span>

### <span data-ttu-id="788c9-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="788c9-122">-AddressPrefix</span></span>
<span data-ttu-id="788c9-123">이 가상 허브에 대 한 주소 공간 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="788c9-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="788c9-124">-AsJob</span></span>
<span data-ttu-id="788c9-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="788c9-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="788c9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788c9-126">-DefaultProfile</span></span>
<span data-ttu-id="788c9-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="788c9-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="788c9-128">-HubVnetConnection</span></span>
<span data-ttu-id="788c9-129">이 가상 허브와 연결 된 허브 가상 네트워크 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="788c9-130">-위치</span><span class="sxs-lookup"><span data-stu-id="788c9-130">-Location</span></span>
<span data-ttu-id="788c9-131">location.</span><span class="sxs-lookup"><span data-stu-id="788c9-131">location.</span></span>

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

### <span data-ttu-id="788c9-132">-이름</span><span class="sxs-lookup"><span data-stu-id="788c9-132">-Name</span></span>
<span data-ttu-id="788c9-133">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-133">The resource name.</span></span>

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

### <span data-ttu-id="788c9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="788c9-134">-ResourceGroupName</span></span>
<span data-ttu-id="788c9-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-135">The resource group name.</span></span>

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

### <span data-ttu-id="788c9-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="788c9-136">-RouteTable</span></span>
<span data-ttu-id="788c9-137">이 가상 허브와 연결 된 경로 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-137">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="788c9-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="788c9-138">-Sku</span></span>
<span data-ttu-id="788c9-139">가상 허브의 sku입니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-139">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="788c9-140">태그</span><span class="sxs-lookup"><span data-stu-id="788c9-140">-Tag</span></span>
<span data-ttu-id="788c9-141">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="788c9-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="788c9-142">-VirtualWan</span></span>
<span data-ttu-id="788c9-143">이 허브가 연결 된 가상 wan 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-143">The virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="788c9-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="788c9-144">-VirtualWanId</span></span>
<span data-ttu-id="788c9-145">이 허브가 연결 된 가상 wan 개체의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-145">The id of virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="788c9-146">-확인</span><span class="sxs-lookup"><span data-stu-id="788c9-146">-Confirm</span></span>
<span data-ttu-id="788c9-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="788c9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="788c9-148">-WhatIf</span></span>
<span data-ttu-id="788c9-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="788c9-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="788c9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788c9-151">CommonParameters</span></span>
<span data-ttu-id="788c9-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="788c9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788c9-153">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="788c9-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788c9-154">입력</span><span class="sxs-lookup"><span data-stu-id="788c9-154">INPUTS</span></span>

### <span data-ttu-id="788c9-155">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="788c9-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="788c9-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="788c9-156">System.String</span></span>

## <span data-ttu-id="788c9-157">출력</span><span class="sxs-lookup"><span data-stu-id="788c9-157">OUTPUTS</span></span>

### <span data-ttu-id="788c9-158">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="788c9-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="788c9-159">상속자</span><span class="sxs-lookup"><span data-stu-id="788c9-159">NOTES</span></span>

## <span data-ttu-id="788c9-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="788c9-160">RELATED LINKS</span></span>

[<span data-ttu-id="788c9-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="788c9-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="788c9-162">제거-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="788c9-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="788c9-163">업데이트-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="788c9-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
