---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: ca7335abfd8fe2dc9591dcb7d96fb6ca71dda4fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311330"
---
# <span data-ttu-id="aa40c-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="aa40c-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="aa40c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa40c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa40c-103">경로 테이블에 대 한 경로 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="aa40c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa40c-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa40c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aa40c-105">DESCRIPTION</span></span>
<span data-ttu-id="aa40c-106">**Set-AzRouteConfig** cmdlet은 경로 테이블에 대 한 경로 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="aa40c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aa40c-107">EXAMPLES</span></span>

### <span data-ttu-id="aa40c-108">예제 1: 경로 수정</span><span class="sxs-lookup"><span data-stu-id="aa40c-108">Example 1: Modify a route</span></span>
```powershell
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : Routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"58c2922e-9efe-4554-a457-956ef44bc718"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/Routetable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.4.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="aa40c-109">이 명령은 Get-AzRouteTable cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="aa40c-110">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="aa40c-111">현재 cmdlet은 Route02 이라는 경로를 수정한 다음 결과를 **AzRouteTable** cmdlet에 전달 하 여 변경 내용을 반영 하도록 표를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="aa40c-112">변수</span><span class="sxs-lookup"><span data-stu-id="aa40c-112">PARAMETERS</span></span>

### <span data-ttu-id="aa40c-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="aa40c-113">-AddressPrefix</span></span>
<span data-ttu-id="aa40c-114">경로가 적용 되는 대상을 클래스를 도메인간 라우팅 (CIDR) 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="aa40c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa40c-115">-DefaultProfile</span></span>
<span data-ttu-id="aa40c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa40c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="aa40c-117">-Name</span></span>
<span data-ttu-id="aa40c-118">이 cmdlet이 수정 하는 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="aa40c-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="aa40c-119">-NextHopIpAddress</span></span>
<span data-ttu-id="aa40c-120">Azure 가상 네트워크에 추가 하는 가상 기기의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="aa40c-121">이 경로는 패킷을 해당 주소로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="aa40c-122">*NextHopType* 매개 변수에 virtualappliance 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="aa40c-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="aa40c-123">-NextHopType</span></span>
<span data-ttu-id="aa40c-124">이 경로에서 패킷을 전달 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="aa40c-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aa40c-126">인터넷.</span><span class="sxs-lookup"><span data-stu-id="aa40c-126">Internet.</span></span>
<span data-ttu-id="aa40c-127">Azure에서 제공 하는 기본 인터넷 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="aa40c-128">않아야.</span><span class="sxs-lookup"><span data-stu-id="aa40c-128">None.</span></span>
<span data-ttu-id="aa40c-129">이 값을 지정 하는 경우 경로는 패킷을 전달 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="aa40c-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="aa40c-130">VirtualAppliance.</span></span>
<span data-ttu-id="aa40c-131">Azure 가상 네트워크에 추가 하는 가상 어플라이언스</span><span class="sxs-lookup"><span data-stu-id="aa40c-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="aa40c-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="aa40c-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="aa40c-133">Azureserver 간 가상 개인 네트워크 게이트웨이.</span><span class="sxs-lookup"><span data-stu-id="aa40c-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="aa40c-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="aa40c-134">VnetLocal.</span></span>
<span data-ttu-id="aa40c-135">로컬 가상 네트워크.</span><span class="sxs-lookup"><span data-stu-id="aa40c-135">The local virtual network.</span></span>
<span data-ttu-id="aa40c-136">동일한 가상 네트워크에 두 개의 서브넷, 10.1.0.0/16, 10.2.0.0/16이 있는 경우 각 서브넷에 대 한 VnetLocal 값을 선택 하 여 다른 서브넷으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="aa40c-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="aa40c-137">-RouteTable</span></span>
<span data-ttu-id="aa40c-138">이 경로가 연결 된 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="aa40c-139">-확인</span><span class="sxs-lookup"><span data-stu-id="aa40c-139">-Confirm</span></span>
<span data-ttu-id="aa40c-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa40c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa40c-141">-WhatIf</span></span>
<span data-ttu-id="aa40c-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa40c-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa40c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa40c-144">CommonParameters</span></span>
<span data-ttu-id="aa40c-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa40c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa40c-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa40c-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa40c-147">입력</span><span class="sxs-lookup"><span data-stu-id="aa40c-147">INPUTS</span></span>

### <span data-ttu-id="aa40c-148">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="aa40c-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="aa40c-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aa40c-149">System.String</span></span>

## <span data-ttu-id="aa40c-150">출력</span><span class="sxs-lookup"><span data-stu-id="aa40c-150">OUTPUTS</span></span>

### <span data-ttu-id="aa40c-151">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="aa40c-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="aa40c-152">상속자</span><span class="sxs-lookup"><span data-stu-id="aa40c-152">NOTES</span></span>

## <span data-ttu-id="aa40c-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa40c-153">RELATED LINKS</span></span>

[<span data-ttu-id="aa40c-154">추가-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="aa40c-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="aa40c-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="aa40c-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="aa40c-156">새로운 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="aa40c-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="aa40c-157">제거-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="aa40c-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


