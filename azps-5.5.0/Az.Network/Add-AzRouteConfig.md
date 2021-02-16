---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 326baa91b8da8f9bae67cf47dcc69246549d7c06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203176"
---
# <span data-ttu-id="e208f-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e208f-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="e208f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e208f-102">SYNOPSIS</span></span>
<span data-ttu-id="e208f-103">경로 테이블에 경로를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="e208f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e208f-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e208f-105">설명</span><span class="sxs-lookup"><span data-stu-id="e208f-105">DESCRIPTION</span></span>
<span data-ttu-id="e208f-106">**Add-AzRouteConfig** cmdlet은 Azure 경로 테이블에 경로를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="e208f-107">예제</span><span class="sxs-lookup"><span data-stu-id="e208f-107">EXAMPLES</span></span>

### <span data-ttu-id="e208f-108">예제 1: 경로 테이블에 경로 추가</span><span class="sxs-lookup"><span data-stu-id="e208f-108">Example 1: Add a route to a route table</span></span>
```powershell
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="e208f-109">첫 번째 명령은 Get-AzRouteTable cmdlet을 사용하여 RouteTable01이라는 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="e208f-110">이 명령은 테이블을 $RouteTable 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="e208f-111">두 번째 명령은 경로 13이라는 경로를 경로에 저장된 경로 테이블에 $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="e208f-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="e208f-112">이 경로는 로컬 가상 네트워크에 패킷을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="e208f-113">예제 2: 파이프라인을 사용하여 경로 테이블에 경로 추가</span><span class="sxs-lookup"><span data-stu-id="e208f-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```powershell
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="e208f-114">이 명령은 **Get-AzRouteTable을** 사용하여 RouteTable01이라는 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="e208f-115">이 명령은 파이프라인 연산자를 사용하여 테이블을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e208f-116">현재 cmdlet은 Route02라는 경로를 추가한 다음 결과를 **Set-AzRouteTable** cmdlet에 전달하여 변경 내용을 반영하기 위해 테이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="e208f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e208f-117">PARAMETERS</span></span>

### <span data-ttu-id="e208f-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e208f-118">-AddressPrefix</span></span>
<span data-ttu-id="e208f-119">경로가 적용되는 대상을 CIDR(CIDR(Classless Interdomain Routing)) 형식으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e208f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e208f-120">-DefaultProfile</span></span>
<span data-ttu-id="e208f-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e208f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e208f-122">-Name</span></span>
<span data-ttu-id="e208f-123">경로 테이블에 추가할 경로의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="e208f-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="e208f-124">-NextHopIpAddress</span></span>
<span data-ttu-id="e208f-125">Azure 가상 네트워크에 추가하는 가상 어플라이언스의 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="e208f-126">이 경로는 패킷을 해당 주소로 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="e208f-127">*NextHopType* 매개 변수에 대한 VirtualAppliance 값을 지정하는 경우 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e208f-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="e208f-128">-NextHopType</span></span>
<span data-ttu-id="e208f-129">이 경로가 패킷을 전달하는 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="e208f-130">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="e208f-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e208f-131">인터넷.</span><span class="sxs-lookup"><span data-stu-id="e208f-131">Internet.</span></span>
<span data-ttu-id="e208f-132">Azure에서 제공하는 기본 인터넷 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="e208f-133">없음.</span><span class="sxs-lookup"><span data-stu-id="e208f-133">None.</span></span>
<span data-ttu-id="e208f-134">이 값을 지정하면 경로가 패킷을 전달하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="e208f-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="e208f-135">VirtualAppliance.</span></span>
<span data-ttu-id="e208f-136">Azure 가상 네트워크에 추가하는 가상 어플라이언스입니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="e208f-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="e208f-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="e208f-138">Azure 서버-서버 가상 사설망 게이트웨이.</span><span class="sxs-lookup"><span data-stu-id="e208f-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="e208f-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="e208f-139">VnetLocal.</span></span>
<span data-ttu-id="e208f-140">로컬 가상 네트워크입니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-140">The local virtual network.</span></span>
<span data-ttu-id="e208f-141">동일한 가상 네트워크에 10.1.0.0/16 및 10.2.0.0/16의 두 서브넷이 있는 경우 다른 서브넷으로 전달할 각 서브넷에 대한 VnetLocal 값을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e208f-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e208f-142">-RouteTable</span></span>
<span data-ttu-id="e208f-143">이 cmdlet에서 경로를 추가하는 경로 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-143">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e208f-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e208f-144">-Confirm</span></span>
<span data-ttu-id="e208f-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e208f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e208f-146">-WhatIf</span></span>
<span data-ttu-id="e208f-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e208f-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e208f-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e208f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e208f-149">CommonParameters</span></span>
<span data-ttu-id="e208f-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e208f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e208f-151">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e208f-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e208f-152">입력</span><span class="sxs-lookup"><span data-stu-id="e208f-152">INPUTS</span></span>

### <span data-ttu-id="e208f-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e208f-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="e208f-154">System.String</span><span class="sxs-lookup"><span data-stu-id="e208f-154">System.String</span></span>

## <span data-ttu-id="e208f-155">출력</span><span class="sxs-lookup"><span data-stu-id="e208f-155">OUTPUTS</span></span>

### <span data-ttu-id="e208f-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e208f-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="e208f-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e208f-157">NOTES</span></span>

## <span data-ttu-id="e208f-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e208f-158">RELATED LINKS</span></span>

[<span data-ttu-id="e208f-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e208f-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="e208f-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e208f-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="e208f-161">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e208f-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="e208f-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e208f-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="e208f-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e208f-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="e208f-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e208f-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


