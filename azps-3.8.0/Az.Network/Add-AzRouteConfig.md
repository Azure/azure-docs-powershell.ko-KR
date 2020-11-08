---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 3ab38da7005a8b96c344b0733c03d4b2fd265f46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044954"
---
# <span data-ttu-id="a73a7-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a73a7-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="a73a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a73a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a73a7-103">경로 테이블에 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="a73a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a73a7-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a73a7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a73a7-105">DESCRIPTION</span></span>
<span data-ttu-id="a73a7-106">**Add-AzRouteConfig** Cmdlet은 Azure 경로 테이블에 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="a73a7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a73a7-107">EXAMPLES</span></span>

### <span data-ttu-id="a73a7-108">예제 1: 경로 테이블에 경로 추가</span><span class="sxs-lookup"><span data-stu-id="a73a7-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="a73a7-109">첫 번째 명령은 Get-AzRouteTable cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="a73a7-110">명령이 $RouteTable 변수에 테이블을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="a73a7-111">두 번째 명령은 $RouteTable에 저장 된 경로 테이블에 Route13 이라는 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="a73a7-112">이 경로는 패킷을 로컬 가상 네트워크에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="a73a7-113">예제 2: 파이프라인을 사용 하 여 경로 테이블에 경로 추가</span><span class="sxs-lookup"><span data-stu-id="a73a7-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
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

<span data-ttu-id="a73a7-114">이 명령은 **Get-AzRouteTable** 를 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="a73a7-115">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a73a7-116">현재 cmdlet은 Route02 이라는 경로를 추가한 다음 결과를 **AzRouteTable** cmdlet에 전달 하 여 변경 내용을 반영 하도록 표를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="a73a7-117">변수</span><span class="sxs-lookup"><span data-stu-id="a73a7-117">PARAMETERS</span></span>

### <span data-ttu-id="a73a7-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a73a7-118">-AddressPrefix</span></span>
<span data-ttu-id="a73a7-119">경로가 적용 되는 대상을 클래스를 도메인간 라우팅 (CIDR) 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="a73a7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73a7-120">-DefaultProfile</span></span>
<span data-ttu-id="a73a7-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a73a7-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a73a7-122">-Name</span></span>
<span data-ttu-id="a73a7-123">경로 테이블에 추가할 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="a73a7-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="a73a7-124">-NextHopIpAddress</span></span>
<span data-ttu-id="a73a7-125">Azure 가상 네트워크에 추가 하는 가상 기기의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="a73a7-126">이 경로는 패킷을 해당 주소로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="a73a7-127">*NextHopType* 매개 변수에 virtualappliance 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="a73a7-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="a73a7-128">-NextHopType</span></span>
<span data-ttu-id="a73a7-129">이 경로에서 패킷을 전달 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="a73a7-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a73a7-131">인터넷.</span><span class="sxs-lookup"><span data-stu-id="a73a7-131">Internet.</span></span>
<span data-ttu-id="a73a7-132">Azure에서 제공 하는 기본 인터넷 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="a73a7-133">않아야.</span><span class="sxs-lookup"><span data-stu-id="a73a7-133">None.</span></span>
<span data-ttu-id="a73a7-134">이 값을 지정 하는 경우 경로는 패킷을 전달 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="a73a7-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="a73a7-135">VirtualAppliance.</span></span>
<span data-ttu-id="a73a7-136">Azure 가상 네트워크에 추가 하는 가상 어플라이언스</span><span class="sxs-lookup"><span data-stu-id="a73a7-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="a73a7-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="a73a7-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="a73a7-138">Azure 서버 간 가상 개인 네트워크 게이트웨이.</span><span class="sxs-lookup"><span data-stu-id="a73a7-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="a73a7-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="a73a7-139">VnetLocal.</span></span>
<span data-ttu-id="a73a7-140">로컬 가상 네트워크.</span><span class="sxs-lookup"><span data-stu-id="a73a7-140">The local virtual network.</span></span>
<span data-ttu-id="a73a7-141">동일한 가상 네트워크에 두 개의 서브넷, 10.1.0.0/16, 10.2.0.0/16이 있는 경우 각 서브넷에 대 한 VnetLocal 값을 선택 하 여 다른 서브넷으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="a73a7-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a73a7-142">-RouteTable</span></span>
<span data-ttu-id="a73a7-143">이 cmdlet이 경로를 추가 하는 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="a73a7-144">-확인</span><span class="sxs-lookup"><span data-stu-id="a73a7-144">-Confirm</span></span>
<span data-ttu-id="a73a7-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a73a7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a73a7-146">-WhatIf</span></span>
<span data-ttu-id="a73a7-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a73a7-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a73a7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73a7-149">CommonParameters</span></span>
<span data-ttu-id="a73a7-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a73a7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73a7-151">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a73a7-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73a7-152">입력</span><span class="sxs-lookup"><span data-stu-id="a73a7-152">INPUTS</span></span>

### <span data-ttu-id="a73a7-153">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a73a7-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="a73a7-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a73a7-154">System.String</span></span>

## <span data-ttu-id="a73a7-155">출력</span><span class="sxs-lookup"><span data-stu-id="a73a7-155">OUTPUTS</span></span>

### <span data-ttu-id="a73a7-156">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a73a7-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="a73a7-157">상속자</span><span class="sxs-lookup"><span data-stu-id="a73a7-157">NOTES</span></span>

## <span data-ttu-id="a73a7-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a73a7-158">RELATED LINKS</span></span>

[<span data-ttu-id="a73a7-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a73a7-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="a73a7-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a73a7-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="a73a7-161">새로운 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a73a7-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="a73a7-162">제거-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a73a7-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="a73a7-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a73a7-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="a73a7-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a73a7-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


