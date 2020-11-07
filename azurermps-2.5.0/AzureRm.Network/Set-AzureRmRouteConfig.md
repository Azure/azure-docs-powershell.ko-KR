---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: 5aa84098c19595ac1c7d6b33c56dca20d08a475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881294"
---
# <span data-ttu-id="30fdf-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="30fdf-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="30fdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="30fdf-103">경로의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30fdf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30fdf-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30fdf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30fdf-105">DESCRIPTION</span></span>
<span data-ttu-id="30fdf-106">**AzureRmRouteConfig** Cmdlet은 Azure 경로에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="30fdf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="30fdf-107">EXAMPLES</span></span>

### <span data-ttu-id="30fdf-108">예제 1: 경로 수정</span><span class="sxs-lookup"><span data-stu-id="30fdf-108">Example 1: Modify a route</span></span>
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

<span data-ttu-id="30fdf-109">이 명령은 Get-AzureRmRouteTable cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="30fdf-110">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="30fdf-111">현재 cmdlet은 Route02 이라는 경로를 수정한 다음 결과를 **AzureRmRouteTable** cmdlet에 전달 하 여 변경 내용을 반영 하도록 표를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="30fdf-112">변수</span><span class="sxs-lookup"><span data-stu-id="30fdf-112">PARAMETERS</span></span>

### <span data-ttu-id="30fdf-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="30fdf-113">-AddressPrefix</span></span>
<span data-ttu-id="30fdf-114">경로가 적용 되는 대상을 클래스를 도메인간 라우팅 (CIDR) 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="30fdf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30fdf-115">-DefaultProfile</span></span>
<span data-ttu-id="30fdf-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30fdf-117">-이름</span><span class="sxs-lookup"><span data-stu-id="30fdf-117">-Name</span></span>
<span data-ttu-id="30fdf-118">이 cmdlet이 수정 하는 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="30fdf-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="30fdf-119">-NextHopIpAddress</span></span>
<span data-ttu-id="30fdf-120">Azure 가상 네트워크에 추가 하는 가상 기기의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="30fdf-121">이 경로는 패킷을 해당 주소로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="30fdf-122">*NextHopType* 매개 변수에 virtualappliance 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="30fdf-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="30fdf-123">-NextHopType</span></span>
<span data-ttu-id="30fdf-124">이 경로에서 패킷을 전달 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="30fdf-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30fdf-126">인터넷.</span><span class="sxs-lookup"><span data-stu-id="30fdf-126">Internet.</span></span>
<span data-ttu-id="30fdf-127">Azure에서 제공 하는 기본 인터넷 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="30fdf-128">않아야.</span><span class="sxs-lookup"><span data-stu-id="30fdf-128">None.</span></span>
<span data-ttu-id="30fdf-129">이 값을 지정 하는 경우 경로는 패킷을 전달 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="30fdf-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="30fdf-130">VirtualAppliance.</span></span>
<span data-ttu-id="30fdf-131">Azure 가상 네트워크에 추가 하는 가상 어플라이언스</span><span class="sxs-lookup"><span data-stu-id="30fdf-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="30fdf-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="30fdf-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="30fdf-133">Azureserver 간 가상 개인 네트워크 게이트웨이.</span><span class="sxs-lookup"><span data-stu-id="30fdf-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="30fdf-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="30fdf-134">VnetLocal.</span></span>
<span data-ttu-id="30fdf-135">로컬 가상 네트워크.</span><span class="sxs-lookup"><span data-stu-id="30fdf-135">The local virtual network.</span></span>
<span data-ttu-id="30fdf-136">동일한 가상 네트워크에 두 개의 서브넷, 10.1.0.0/16, 10.2.0.0/16이 있는 경우 각 서브넷에 대 한 VnetLocal 값을 선택 하 여 다른 서브넷으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="30fdf-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="30fdf-137">-RouteTable</span></span>
<span data-ttu-id="30fdf-138">이 경로가 연결 된 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="30fdf-139">-확인</span><span class="sxs-lookup"><span data-stu-id="30fdf-139">-Confirm</span></span>
<span data-ttu-id="30fdf-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30fdf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30fdf-141">-WhatIf</span></span>
<span data-ttu-id="30fdf-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30fdf-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30fdf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30fdf-144">CommonParameters</span></span>
<span data-ttu-id="30fdf-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30fdf-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30fdf-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30fdf-147">입력</span><span class="sxs-lookup"><span data-stu-id="30fdf-147">INPUTS</span></span>

### <span data-ttu-id="30fdf-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="30fdf-148">PSRouteTable</span></span>
<span data-ttu-id="30fdf-149">' RouteTable ' 매개 변수는 파이프라인에서 ' PSRouteTable ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="30fdf-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="30fdf-150">출력</span><span class="sxs-lookup"><span data-stu-id="30fdf-150">OUTPUTS</span></span>

### <span data-ttu-id="30fdf-151">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="30fdf-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="30fdf-152">상속자</span><span class="sxs-lookup"><span data-stu-id="30fdf-152">NOTES</span></span>

## <span data-ttu-id="30fdf-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30fdf-153">RELATED LINKS</span></span>

[<span data-ttu-id="30fdf-154">추가-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="30fdf-154">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="30fdf-155">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="30fdf-155">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="30fdf-156">새로운 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="30fdf-156">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="30fdf-157">제거-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="30fdf-157">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)


