---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: 7b28c50cfc53fee03d5715697a88e9356ea7664b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533991"
---
# <span data-ttu-id="1d38d-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1d38d-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="1d38d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d38d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d38d-103">경로 테이블에 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d38d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d38d-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d38d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1d38d-105">DESCRIPTION</span></span>
<span data-ttu-id="1d38d-106">**Add-AzureRmRouteConfig** Cmdlet은 Azure 경로 테이블에 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="1d38d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1d38d-107">EXAMPLES</span></span>

### <span data-ttu-id="1d38d-108">예제 1: 경로 테이블에 경로 추가</span><span class="sxs-lookup"><span data-stu-id="1d38d-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="1d38d-109">첫 번째 명령은 Get-AzureRmRouteTable cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="1d38d-110">명령이 $RouteTable 변수에 테이블을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="1d38d-111">두 번째 명령은 $RouteTable에 저장 된 경로 테이블에 Route13 이라는 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="1d38d-112">이 경로는 패킷을 로컬 가상 네트워크에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="1d38d-113">예제 2: 파이프라인을 사용 하 여 경로 테이블에 경로 추가</span><span class="sxs-lookup"><span data-stu-id="1d38d-113">Example 2: Add a route to a route table by using the pipeline</span></span>
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

<span data-ttu-id="1d38d-114">이 명령은 **Get-AzureRmRouteTable** 를 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="1d38d-115">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1d38d-116">현재 cmdlet은 Route02 이라는 경로를 추가한 다음 결과를 **AzureRmRouteTable** cmdlet에 전달 하 여 변경 내용을 반영 하도록 표를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="1d38d-117">변수</span><span class="sxs-lookup"><span data-stu-id="1d38d-117">PARAMETERS</span></span>

### <span data-ttu-id="1d38d-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1d38d-118">-AddressPrefix</span></span>
<span data-ttu-id="1d38d-119">경로가 적용 되는 대상을 클래스를 도메인간 라우팅 (CIDR) 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="1d38d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="1d38d-120">-Name</span></span>
<span data-ttu-id="1d38d-121">경로 테이블에 추가할 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-121">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="1d38d-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="1d38d-122">-NextHopIpAddress</span></span>
<span data-ttu-id="1d38d-123">Azure 가상 네트워크에 추가 하는 가상 기기의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-123">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="1d38d-124">이 경로는 패킷을 해당 주소로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-124">This route forwards packets to that address.</span></span>
<span data-ttu-id="1d38d-125">*NextHopType* 매개 변수에 virtualappliance 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-125">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="1d38d-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="1d38d-126">-NextHopType</span></span>
<span data-ttu-id="1d38d-127">이 경로에서 패킷을 전달 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-127">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="1d38d-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d38d-129">인터넷.</span><span class="sxs-lookup"><span data-stu-id="1d38d-129">Internet.</span></span>
<span data-ttu-id="1d38d-130">Azure에서 제공 하는 기본 인터넷 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-130">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="1d38d-131">않아야.</span><span class="sxs-lookup"><span data-stu-id="1d38d-131">None.</span></span>
<span data-ttu-id="1d38d-132">이 값을 지정 하는 경우 경로는 패킷을 전달 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-132">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="1d38d-133">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="1d38d-133">VirtualAppliance.</span></span>
<span data-ttu-id="1d38d-134">Azure 가상 네트워크에 추가 하는 가상 어플라이언스</span><span class="sxs-lookup"><span data-stu-id="1d38d-134">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="1d38d-135">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="1d38d-135">VirtualNetworkGateway.</span></span>
<span data-ttu-id="1d38d-136">Azure 서버 간 가상 개인 네트워크 게이트웨이.</span><span class="sxs-lookup"><span data-stu-id="1d38d-136">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="1d38d-137">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="1d38d-137">VnetLocal.</span></span>
<span data-ttu-id="1d38d-138">로컬 가상 네트워크.</span><span class="sxs-lookup"><span data-stu-id="1d38d-138">The local virtual network.</span></span>
<span data-ttu-id="1d38d-139">동일한 가상 네트워크에 두 개의 서브넷, 10.1.0.0/16, 10.2.0.0/16이 있는 경우 각 서브넷에 대 한 VnetLocal 값을 선택 하 여 다른 서브넷으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-139">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, None, VirtualAppliance, VirtualNetworkGateway, VnetLocal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d38d-140">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1d38d-140">-RouteTable</span></span>
<span data-ttu-id="1d38d-141">이 cmdlet이 경로를 추가 하는 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-141">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d38d-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d38d-142">-DefaultProfile</span></span>
<span data-ttu-id="1d38d-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d38d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d38d-144">CommonParameters</span></span>
<span data-ttu-id="1d38d-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d38d-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d38d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d38d-147">입력</span><span class="sxs-lookup"><span data-stu-id="1d38d-147">INPUTS</span></span>

### <span data-ttu-id="1d38d-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d38d-148">PSRouteTable</span></span>
<span data-ttu-id="1d38d-149">' RouteTable ' 매개 변수는 파이프라인에서 ' PSRouteTable ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d38d-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="1d38d-150">출력</span><span class="sxs-lookup"><span data-stu-id="1d38d-150">OUTPUTS</span></span>

### <span data-ttu-id="1d38d-151">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1d38d-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="1d38d-152">상속자</span><span class="sxs-lookup"><span data-stu-id="1d38d-152">NOTES</span></span>

## <span data-ttu-id="1d38d-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d38d-153">RELATED LINKS</span></span>

[<span data-ttu-id="1d38d-154">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1d38d-154">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="1d38d-155">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d38d-155">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="1d38d-156">새로운 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1d38d-156">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="1d38d-157">제거-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1d38d-157">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="1d38d-158">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1d38d-158">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="1d38d-159">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d38d-159">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


