---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: a07df2c6330757bf9e5b4f211429f6e2918fea39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186817"
---
# <span data-ttu-id="e1847-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e1847-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="e1847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1847-102">SYNOPSIS</span></span>
<span data-ttu-id="e1847-103">가상 허브를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="e1847-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1847-104">SYNTAX</span></span>

### <span data-ttu-id="e1847-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e1847-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1847-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e1847-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1847-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e1847-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1847-108">설명</span><span class="sxs-lookup"><span data-stu-id="e1847-108">DESCRIPTION</span></span>
<span data-ttu-id="e1847-109">**Update-AzVirtualHub** cmdlet은 가상 허브를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="e1847-110">예제</span><span class="sxs-lookup"><span data-stu-id="e1847-110">EXAMPLES</span></span>

### <span data-ttu-id="e1847-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e1847-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="e1847-112">위의 경우 Azure의 해당 리소스 그룹에 리소스 그룹 "testRG", Virtual WAN 및 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e1847-113">가상 허브의 주소 공간은 "10.0.1.0/24"입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="e1847-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="e1847-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="e1847-115">위의 경우 Azure의 해당 리소스 그룹에 리소스 그룹 "testRG", Virtual WAN 및 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e1847-116">가상 허브의 주소 공간은 "10.0.1.0/24"입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="e1847-117">이 예제는 예제 1과 유사하지만 가상 허브에 경로 테이블을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="e1847-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1847-118">PARAMETERS</span></span>

### <span data-ttu-id="e1847-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e1847-119">-AddressPrefix</span></span>
<span data-ttu-id="e1847-120">이 가상 허브에 대한 주소 공간 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="e1847-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1847-121">-AsJob</span></span>
<span data-ttu-id="e1847-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e1847-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1847-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1847-123">-DefaultProfile</span></span>
<span data-ttu-id="e1847-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1847-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e1847-125">-HubVnetConnection</span></span>
<span data-ttu-id="e1847-126">이 가상 허브와 연결된 허브 가상 네트워크 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="e1847-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1847-127">-InputObject</span></span>
<span data-ttu-id="e1847-128">수정할 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="e1847-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e1847-129">-Name</span></span>
<span data-ttu-id="e1847-130">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1847-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1847-131">-ResourceGroupName</span></span>
<span data-ttu-id="e1847-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-132">The resource group name.</span></span>

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

### <span data-ttu-id="e1847-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1847-133">-ResourceId</span></span>
<span data-ttu-id="e1847-134">수정할 가상 허브의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="e1847-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e1847-135">-RouteTable</span></span>
<span data-ttu-id="e1847-136">이 가상 허브와 연결된 경로 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="e1847-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="e1847-137">-Sku</span></span>
<span data-ttu-id="e1847-138">가상 허브의 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-138">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="e1847-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1847-139">-Tag</span></span>
<span data-ttu-id="e1847-140">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e1847-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1847-141">-Confirm</span></span>
<span data-ttu-id="e1847-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1847-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1847-143">-WhatIf</span></span>
<span data-ttu-id="e1847-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e1847-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1847-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1847-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1847-146">CommonParameters</span></span>
<span data-ttu-id="e1847-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1847-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1847-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1847-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1847-149">입력</span><span class="sxs-lookup"><span data-stu-id="e1847-149">INPUTS</span></span>

### <span data-ttu-id="e1847-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e1847-150">System.String</span></span>

### <span data-ttu-id="e1847-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e1847-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e1847-152">출력</span><span class="sxs-lookup"><span data-stu-id="e1847-152">OUTPUTS</span></span>

### <span data-ttu-id="e1847-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e1847-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e1847-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1847-154">NOTES</span></span>

## <span data-ttu-id="e1847-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1847-155">RELATED LINKS</span></span>

[<span data-ttu-id="e1847-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e1847-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="e1847-157">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e1847-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="e1847-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e1847-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)
