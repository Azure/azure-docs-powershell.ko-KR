---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: aa5f8f71765118a2fb95117709a7fcfc83b1edcb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880405"
---
# <span data-ttu-id="4e010-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4e010-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="4e010-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e010-102">SYNOPSIS</span></span>
<span data-ttu-id="4e010-103">경로 테이블에 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e010-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4e010-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e010-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4e010-105">DESCRIPTION</span></span>
<span data-ttu-id="4e010-106">**Add-AzureRmRouteConfig** Cmdlet은 Azure 경로 테이블에 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="4e010-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4e010-107">EXAMPLES</span></span>

### <span data-ttu-id="4e010-108">예제 1: 경로 테이블에 경로 추가</span><span class="sxs-lookup"><span data-stu-id="4e010-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="4e010-109">첫 번째 명령은 Get-AzureRmRouteTable cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="4e010-110">명령이 $RouteTable 변수에 테이블을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="4e010-111">두 번째 명령은 $RouteTable에 저장 된 경로 테이블에 Route13 이라는 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="4e010-112">이 경로는 패킷을 로컬 가상 네트워크에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="4e010-113">예제 2: 파이프라인을 사용 하 여 경로 테이블에 경로 추가</span><span class="sxs-lookup"><span data-stu-id="4e010-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="4e010-114">이 명령은 **Get-AzureRmRouteTable** 를 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="4e010-115">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4e010-116">현재 cmdlet은 Route02 이라는 경로를 추가한 다음 결과를 **AzureRmRouteTable** cmdlet에 전달 하 여 변경 내용을 반영 하도록 표를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="4e010-117">변수</span><span class="sxs-lookup"><span data-stu-id="4e010-117">PARAMETERS</span></span>

### <span data-ttu-id="4e010-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4e010-118">-AddressPrefix</span></span>
<span data-ttu-id="4e010-119">경로가 적용 되는 대상을 클래스를 도메인간 라우팅 (CIDR) 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e010-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e010-120">-DefaultProfile</span></span>
<span data-ttu-id="4e010-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e010-122">-이름</span><span class="sxs-lookup"><span data-stu-id="4e010-122">-Name</span></span>
<span data-ttu-id="4e010-123">경로 테이블에 추가할 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="4e010-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="4e010-124">-NextHopIpAddress</span></span>
<span data-ttu-id="4e010-125">Azure 가상 네트워크에 추가 하는 가상 기기의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="4e010-126">이 경로는 패킷을 해당 주소로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="4e010-127">*NextHopType* 매개 변수에 virtualappliance 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e010-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="4e010-128">-NextHopType</span></span>
<span data-ttu-id="4e010-129">이 경로에서 패킷을 전달 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="4e010-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e010-131">인터넷.</span><span class="sxs-lookup"><span data-stu-id="4e010-131">Internet.</span></span>
<span data-ttu-id="4e010-132">Azure에서 제공 하는 기본 인터넷 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="4e010-133">않아야.</span><span class="sxs-lookup"><span data-stu-id="4e010-133">None.</span></span>
<span data-ttu-id="4e010-134">이 값을 지정 하는 경우 경로는 패킷을 전달 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="4e010-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="4e010-135">VirtualAppliance.</span></span>
<span data-ttu-id="4e010-136">Azure 가상 네트워크에 추가 하는 가상 어플라이언스</span><span class="sxs-lookup"><span data-stu-id="4e010-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="4e010-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="4e010-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="4e010-138">Azure 서버 간 가상 개인 네트워크 게이트웨이.</span><span class="sxs-lookup"><span data-stu-id="4e010-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="4e010-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="4e010-139">VnetLocal.</span></span>
<span data-ttu-id="4e010-140">로컬 가상 네트워크.</span><span class="sxs-lookup"><span data-stu-id="4e010-140">The local virtual network.</span></span>
<span data-ttu-id="4e010-141">동일한 가상 네트워크에 두 개의 서브넷, 10.1.0.0/16, 10.2.0.0/16이 있는 경우 각 서브넷에 대 한 VnetLocal 값을 선택 하 여 다른 서브넷으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e010-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4e010-142">-RouteTable</span></span>
<span data-ttu-id="4e010-143">이 cmdlet이 경로를 추가 하는 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-143">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e010-144">-확인</span><span class="sxs-lookup"><span data-stu-id="4e010-144">-Confirm</span></span>
<span data-ttu-id="4e010-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e010-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e010-146">-WhatIf</span></span>
<span data-ttu-id="4e010-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e010-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e010-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e010-149">CommonParameters</span></span>
<span data-ttu-id="4e010-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e010-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e010-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e010-152">입력</span><span class="sxs-lookup"><span data-stu-id="4e010-152">INPUTS</span></span>

### <span data-ttu-id="4e010-153">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e010-153">PSRouteTable</span></span>
<span data-ttu-id="4e010-154">' RouteTable ' 매개 변수는 파이프라인에서 ' PSRouteTable ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e010-154">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="4e010-155">출력</span><span class="sxs-lookup"><span data-stu-id="4e010-155">OUTPUTS</span></span>

### <span data-ttu-id="4e010-156">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4e010-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4e010-157">상속자</span><span class="sxs-lookup"><span data-stu-id="4e010-157">NOTES</span></span>

## <span data-ttu-id="4e010-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e010-158">RELATED LINKS</span></span>

[<span data-ttu-id="4e010-159">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4e010-159">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="4e010-160">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e010-160">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="4e010-161">새로운 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4e010-161">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="4e010-162">제거-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4e010-162">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="4e010-163">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4e010-163">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="4e010-164">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e010-164">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


