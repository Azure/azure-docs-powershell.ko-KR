---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
ms.openlocfilehash: 4058f9a2ba0de1e5610773ad4af21c8bb788d58c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703153"
---
# <span data-ttu-id="d0adf-101">New-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d0adf-101">New-AzureRmVirtualHub</span></span>

## <span data-ttu-id="d0adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0adf-102">SYNOPSIS</span></span>
<span data-ttu-id="d0adf-103">Azure VirtualHub 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-103">Creates an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0adf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0adf-104">SYNTAX</span></span>

### <span data-ttu-id="d0adf-105">ByVirtualWanObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="d0adf-105">ByVirtualWanObject (Default)</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 -AddressPrefix <String> -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0adf-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="d0adf-106">ByVirtualWanResourceId</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0adf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d0adf-107">DESCRIPTION</span></span>
<span data-ttu-id="d0adf-108">Azure VirtualHub 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="d0adf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d0adf-109">EXAMPLES</span></span>

### <span data-ttu-id="d0adf-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d0adf-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="d0adf-111">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="d0adf-112">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="d0adf-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d0adf-113">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="d0adf-114">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="d0adf-115">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="d0adf-116">이 예제는 예제 1과 비슷하지만, 리소스 Id를 사용 하 여 가상 허브를 만드는 데 필요한 가상 WAN을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="d0adf-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="d0adf-117">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="d0adf-118">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="d0adf-119">가상 허브에는 주소 공간 "10.0.1.0/24"와 경로 테이블이 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="d0adf-120">이 예제는 예제 2와 유사 하지만, 가상 허브에도 경로 테이블을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="d0adf-121">변수</span><span class="sxs-lookup"><span data-stu-id="d0adf-121">PARAMETERS</span></span>

### <span data-ttu-id="d0adf-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d0adf-122">-AddressPrefix</span></span>
<span data-ttu-id="d0adf-123">이 가상 허브에 대 한 주소 공간 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-123">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0adf-124">-AsJob</span></span>
<span data-ttu-id="d0adf-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d0adf-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0adf-126">-DefaultProfile</span></span>
<span data-ttu-id="d0adf-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d0adf-128">-HubVnetConnection</span></span>
<span data-ttu-id="d0adf-129">이 가상 허브와 연결 된 허브 가상 네트워크 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-130">-위치</span><span class="sxs-lookup"><span data-stu-id="d0adf-130">-Location</span></span>
<span data-ttu-id="d0adf-131">location.</span><span class="sxs-lookup"><span data-stu-id="d0adf-131">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-132">-이름</span><span class="sxs-lookup"><span data-stu-id="d0adf-132">-Name</span></span>
<span data-ttu-id="d0adf-133">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0adf-134">-ResourceGroupName</span></span>
<span data-ttu-id="d0adf-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="d0adf-136">-RouteTable</span></span>
<span data-ttu-id="d0adf-137">이 가상 허브와 연결 된 경로 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-138">태그</span><span class="sxs-lookup"><span data-stu-id="d0adf-138">-Tag</span></span>
<span data-ttu-id="d0adf-139">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="d0adf-140">-VirtualWan</span></span>
<span data-ttu-id="d0adf-141">이 허브가 연결 된 가상 wan 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-141">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="d0adf-142">-VirtualWanId</span></span>
<span data-ttu-id="d0adf-143">이 허브가 연결 된 가상 wan 개체의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-143">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-144">-확인</span><span class="sxs-lookup"><span data-stu-id="d0adf-144">-Confirm</span></span>
<span data-ttu-id="d0adf-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0adf-146">-WhatIf</span></span>
<span data-ttu-id="d0adf-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0adf-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0adf-149">CommonParameters</span></span>
<span data-ttu-id="d0adf-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0adf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0adf-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0adf-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0adf-152">입력</span><span class="sxs-lookup"><span data-stu-id="d0adf-152">INPUTS</span></span>

### <span data-ttu-id="d0adf-153">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d0adf-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="d0adf-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d0adf-154">System.String</span></span>

## <span data-ttu-id="d0adf-155">출력</span><span class="sxs-lookup"><span data-stu-id="d0adf-155">OUTPUTS</span></span>

### <span data-ttu-id="d0adf-156">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d0adf-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="d0adf-157">상속자</span><span class="sxs-lookup"><span data-stu-id="d0adf-157">NOTES</span></span>

## <span data-ttu-id="d0adf-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0adf-158">RELATED LINKS</span></span>
