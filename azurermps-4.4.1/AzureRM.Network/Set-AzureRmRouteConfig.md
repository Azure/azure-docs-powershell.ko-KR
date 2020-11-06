---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
ms.openlocfilehash: a86e5346078bd1a8c9be924cdeac3b94fab907dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529267"
---
# <span data-ttu-id="b6f37-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b6f37-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="b6f37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f37-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f37-103">경로의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6f37-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6f37-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6f37-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b6f37-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f37-106">**AzureRmRouteConfig** Cmdlet은 Azure 경로에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="b6f37-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b6f37-107">EXAMPLES</span></span>

### <span data-ttu-id="b6f37-108">예제 1: 경로 수정</span><span class="sxs-lookup"><span data-stu-id="b6f37-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="b6f37-109">이 명령은 Get-AzureRmRouteTable cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="b6f37-110">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b6f37-111">현재 cmdlet은 Route02 이라는 경로를 수정한 다음 결과를 **AzureRmRouteTable** cmdlet에 전달 하 여 변경 내용을 반영 하도록 표를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="b6f37-112">변수</span><span class="sxs-lookup"><span data-stu-id="b6f37-112">PARAMETERS</span></span>

### <span data-ttu-id="b6f37-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b6f37-113">-AddressPrefix</span></span>
<span data-ttu-id="b6f37-114">경로가 적용 되는 대상을 클래스를 도메인간 라우팅 (CIDR) 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="b6f37-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b6f37-115">-Name</span></span>
<span data-ttu-id="b6f37-116">이 cmdlet이 수정 하는 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-116">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b6f37-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="b6f37-117">-NextHopIpAddress</span></span>
<span data-ttu-id="b6f37-118">Azure 가상 네트워크에 추가 하는 가상 기기의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-118">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="b6f37-119">이 경로는 패킷을 해당 주소로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="b6f37-120">*NextHopType* 매개 변수에 virtualappliance 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="b6f37-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="b6f37-121">-NextHopType</span></span>
<span data-ttu-id="b6f37-122">이 경로에서 패킷을 전달 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="b6f37-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6f37-124">인터넷.</span><span class="sxs-lookup"><span data-stu-id="b6f37-124">Internet.</span></span>
<span data-ttu-id="b6f37-125">Azure에서 제공 하는 기본 인터넷 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="b6f37-126">않아야.</span><span class="sxs-lookup"><span data-stu-id="b6f37-126">None.</span></span>
<span data-ttu-id="b6f37-127">이 값을 지정 하는 경우 경로는 패킷을 전달 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="b6f37-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="b6f37-128">VirtualAppliance.</span></span>
<span data-ttu-id="b6f37-129">Azure 가상 네트워크에 추가 하는 가상 어플라이언스</span><span class="sxs-lookup"><span data-stu-id="b6f37-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="b6f37-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="b6f37-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="b6f37-131">Azureserver 간 가상 개인 네트워크 게이트웨이.</span><span class="sxs-lookup"><span data-stu-id="b6f37-131">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="b6f37-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="b6f37-132">VnetLocal.</span></span>
<span data-ttu-id="b6f37-133">로컬 가상 네트워크.</span><span class="sxs-lookup"><span data-stu-id="b6f37-133">The local virtual network.</span></span>
<span data-ttu-id="b6f37-134">동일한 가상 네트워크에 두 개의 서브넷, 10.1.0.0/16, 10.2.0.0/16이 있는 경우 각 서브넷에 대 한 VnetLocal 값을 선택 하 여 다른 서브넷으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="b6f37-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="b6f37-135">-RouteTable</span></span>
<span data-ttu-id="b6f37-136">이 경로가 연결 된 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-136">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="b6f37-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f37-137">-DefaultProfile</span></span>
<span data-ttu-id="b6f37-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6f37-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f37-139">CommonParameters</span></span>
<span data-ttu-id="b6f37-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f37-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f37-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f37-142">입력</span><span class="sxs-lookup"><span data-stu-id="b6f37-142">INPUTS</span></span>

### <span data-ttu-id="b6f37-143">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6f37-143">PSRouteTable</span></span>
<span data-ttu-id="b6f37-144">' RouteTable ' 매개 변수는 파이프라인에서 ' PSRouteTable ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f37-144">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="b6f37-145">출력</span><span class="sxs-lookup"><span data-stu-id="b6f37-145">OUTPUTS</span></span>

### <span data-ttu-id="b6f37-146">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b6f37-146">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="b6f37-147">상속자</span><span class="sxs-lookup"><span data-stu-id="b6f37-147">NOTES</span></span>

## <span data-ttu-id="b6f37-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6f37-148">RELATED LINKS</span></span>

[<span data-ttu-id="b6f37-149">추가-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b6f37-149">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="b6f37-150">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b6f37-150">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="b6f37-151">새로운 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b6f37-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="b6f37-152">제거-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b6f37-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)


