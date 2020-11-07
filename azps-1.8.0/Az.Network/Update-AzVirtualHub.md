---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: 96ba4a6a80e7826b1cf95086f1410305322cf266
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699925"
---
# <span data-ttu-id="b6dc6-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b6dc6-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="b6dc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="b6dc6-103">가상 허브를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="b6dc6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6dc6-104">SYNTAX</span></span>

### <span data-ttu-id="b6dc6-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b6dc6-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6dc6-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="b6dc6-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6dc6-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b6dc6-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6dc6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b6dc6-108">DESCRIPTION</span></span>
<span data-ttu-id="b6dc6-109">**업데이트 AzVirtualHub** cmdlet은 가상 허브를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="b6dc6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b6dc6-110">EXAMPLES</span></span>

### <span data-ttu-id="b6dc6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6dc6-111">Example 1</span></span>

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
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="b6dc6-112">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="b6dc6-113">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="b6dc6-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="b6dc6-114">Example 2</span></span>

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
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="b6dc6-115">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="b6dc6-116">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="b6dc6-117">이 예제는 예제 1과 비슷하지만, 가상 허브에도 경로 테이블을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="b6dc6-118">변수</span><span class="sxs-lookup"><span data-stu-id="b6dc6-118">PARAMETERS</span></span>

### <span data-ttu-id="b6dc6-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b6dc6-119">-AddressPrefix</span></span>
<span data-ttu-id="b6dc6-120">이 가상 허브에 대 한 주소 공간 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="b6dc6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6dc6-121">-AsJob</span></span>
<span data-ttu-id="b6dc6-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b6dc6-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6dc6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6dc6-123">-DefaultProfile</span></span>
<span data-ttu-id="b6dc6-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6dc6-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b6dc6-125">-HubVnetConnection</span></span>
<span data-ttu-id="b6dc6-126">이 가상 허브와 연결 된 허브 가상 네트워크 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="b6dc6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6dc6-127">-InputObject</span></span>
<span data-ttu-id="b6dc6-128">수정할 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="b6dc6-129">-이름</span><span class="sxs-lookup"><span data-stu-id="b6dc6-129">-Name</span></span>
<span data-ttu-id="b6dc6-130">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-130">The resource name.</span></span>

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

### <span data-ttu-id="b6dc6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6dc6-131">-ResourceGroupName</span></span>
<span data-ttu-id="b6dc6-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-132">The resource group name.</span></span>

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

### <span data-ttu-id="b6dc6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6dc6-133">-ResourceId</span></span>
<span data-ttu-id="b6dc6-134">수정할 가상 허브의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="b6dc6-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="b6dc6-135">-RouteTable</span></span>
<span data-ttu-id="b6dc6-136">이 가상 허브와 연결 된 경로 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="b6dc6-137">태그</span><span class="sxs-lookup"><span data-stu-id="b6dc6-137">-Tag</span></span>
<span data-ttu-id="b6dc6-138">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b6dc6-139">-확인</span><span class="sxs-lookup"><span data-stu-id="b6dc6-139">-Confirm</span></span>
<span data-ttu-id="b6dc6-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6dc6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6dc6-141">-WhatIf</span></span>
<span data-ttu-id="b6dc6-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6dc6-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6dc6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6dc6-144">CommonParameters</span></span>
<span data-ttu-id="b6dc6-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6dc6-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6dc6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6dc6-147">입력</span><span class="sxs-lookup"><span data-stu-id="b6dc6-147">INPUTS</span></span>

### <span data-ttu-id="b6dc6-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b6dc6-148">System.String</span></span>

### <span data-ttu-id="b6dc6-149">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b6dc6-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="b6dc6-150">출력</span><span class="sxs-lookup"><span data-stu-id="b6dc6-150">OUTPUTS</span></span>

### <span data-ttu-id="b6dc6-151">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b6dc6-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="b6dc6-152">상속자</span><span class="sxs-lookup"><span data-stu-id="b6dc6-152">NOTES</span></span>

## <span data-ttu-id="b6dc6-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6dc6-153">RELATED LINKS</span></span>

[<span data-ttu-id="b6dc6-154">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b6dc6-154">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="b6dc6-155">새로운 AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b6dc6-155">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="b6dc6-156">제거-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b6dc6-156">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)
