---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualHub.md
ms.openlocfilehash: 188d449e47155739b4bc532c12b0e9193781c7c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531369"
---
# <span data-ttu-id="1fdc8-101">Update-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1fdc8-101">Update-AzureRmVirtualHub</span></span>

## <span data-ttu-id="1fdc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fdc8-102">SYNOPSIS</span></span>
<span data-ttu-id="1fdc8-103">가상 허브를 원하는 목표 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-103">Updates a Virtual Hub to an intended goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fdc8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1fdc8-104">SYNTAX</span></span>

### <span data-ttu-id="1fdc8-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1fdc8-105">ByVirtualHubName (Default)</span></span>
```
Update-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fdc8-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="1fdc8-106">ByVirtualHubResourceId</span></span>
```
Update-AzureRmVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fdc8-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="1fdc8-107">ByVirtualHubObject</span></span>
```
Update-AzureRmVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1fdc8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1fdc8-108">DESCRIPTION</span></span>
<span data-ttu-id="1fdc8-109">가상 허브를 원하는 목표 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-109">Updates a Virtual Hub to an intended goal state.</span></span>

## <span data-ttu-id="1fdc8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1fdc8-110">EXAMPLES</span></span>

### <span data-ttu-id="1fdc8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1fdc8-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="1fdc8-112">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="1fdc8-113">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="1fdc8-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="1fdc8-114">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="1fdc8-115">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="1fdc8-116">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="1fdc8-117">이 예제는 예제 1과 비슷하지만, 가상 허브에도 경로 테이블을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="1fdc8-118">변수</span><span class="sxs-lookup"><span data-stu-id="1fdc8-118">PARAMETERS</span></span>

### <span data-ttu-id="1fdc8-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1fdc8-119">-AddressPrefix</span></span>
<span data-ttu-id="1fdc8-120">이 가상 허브에 대 한 주소 공간 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-120">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fdc8-121">-AsJob</span></span>
<span data-ttu-id="1fdc8-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1fdc8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fdc8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fdc8-123">-DefaultProfile</span></span>
<span data-ttu-id="1fdc8-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fdc8-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1fdc8-125">-HubVnetConnection</span></span>
<span data-ttu-id="1fdc8-126">이 가상 허브와 연결 된 허브 가상 네트워크 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="1fdc8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fdc8-127">-InputObject</span></span>
<span data-ttu-id="1fdc8-128">수정할 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc8-129">-이름</span><span class="sxs-lookup"><span data-stu-id="1fdc8-129">-Name</span></span>
<span data-ttu-id="1fdc8-130">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fdc8-131">-ResourceGroupName</span></span>
<span data-ttu-id="1fdc8-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fdc8-133">-ResourceId</span></span>
<span data-ttu-id="1fdc8-134">수정할 가상 허브의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc8-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1fdc8-135">-RouteTable</span></span>
<span data-ttu-id="1fdc8-136">이 가상 허브와 연결 된 경로 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="1fdc8-137">태그</span><span class="sxs-lookup"><span data-stu-id="1fdc8-137">-Tag</span></span>
<span data-ttu-id="1fdc8-138">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1fdc8-139">-확인</span><span class="sxs-lookup"><span data-stu-id="1fdc8-139">-Confirm</span></span>
<span data-ttu-id="1fdc8-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fdc8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fdc8-141">-WhatIf</span></span>
<span data-ttu-id="1fdc8-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fdc8-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fdc8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fdc8-144">CommonParameters</span></span>
<span data-ttu-id="1fdc8-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fdc8-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fdc8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fdc8-147">입력</span><span class="sxs-lookup"><span data-stu-id="1fdc8-147">INPUTS</span></span>

### <span data-ttu-id="1fdc8-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1fdc8-148">System.String</span></span>

### <span data-ttu-id="1fdc8-149">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1fdc8-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="1fdc8-150">출력</span><span class="sxs-lookup"><span data-stu-id="1fdc8-150">OUTPUTS</span></span>

### <span data-ttu-id="1fdc8-151">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1fdc8-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="1fdc8-152">상속자</span><span class="sxs-lookup"><span data-stu-id="1fdc8-152">NOTES</span></span>

## <span data-ttu-id="1fdc8-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fdc8-153">RELATED LINKS</span></span>
