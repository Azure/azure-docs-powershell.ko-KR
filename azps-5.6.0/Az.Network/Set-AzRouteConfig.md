---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: a4cdcbf52dfb20f0282347d5dc1ce9a5aec14da0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990920"
---
# <span data-ttu-id="cfb97-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cfb97-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="cfb97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfb97-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb97-103">경로 테이블에 대한 경로 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="cfb97-104">구문</span><span class="sxs-lookup"><span data-stu-id="cfb97-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfb97-105">설명</span><span class="sxs-lookup"><span data-stu-id="cfb97-105">DESCRIPTION</span></span>
<span data-ttu-id="cfb97-106">**Set-AzRouteConfig** cmdlet은 경로 테이블에 대한 경로 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="cfb97-107">예제</span><span class="sxs-lookup"><span data-stu-id="cfb97-107">EXAMPLES</span></span>

### <span data-ttu-id="cfb97-108">예제 1: 경로 수정</span><span class="sxs-lookup"><span data-stu-id="cfb97-108">Example 1: Modify a route</span></span>
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

<span data-ttu-id="cfb97-109">이 명령은 Get-AzRouteTable cmdlet을 사용하여 RouteTable01이라는 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="cfb97-110">명령은 파이프라인 연산자를 사용하여 현재 cmdlet에 테이블을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cfb97-111">현재 cmdlet은 Route02라는 경로를 수정한 다음, **결과를 Set-AzRouteTable** cmdlet에 전달하여 변경 내용을 반영하기 위해 표를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="cfb97-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cfb97-112">PARAMETERS</span></span>

### <span data-ttu-id="cfb97-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cfb97-113">-AddressPrefix</span></span>
<span data-ttu-id="cfb97-114">경로가 적용되는 대상을 CIDR(Classless Interdomain Routing)(CIDR) 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="cfb97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb97-115">-DefaultProfile</span></span>
<span data-ttu-id="cfb97-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfb97-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cfb97-117">-Name</span></span>
<span data-ttu-id="cfb97-118">이 cmdlet이 수정하는 경로의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cfb97-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="cfb97-119">-NextHopIpAddress</span></span>
<span data-ttu-id="cfb97-120">Azure 가상 네트워크에 추가하는 가상 어플라이언스의 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="cfb97-121">이 경로는 패킷을 해당 주소로 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="cfb97-122">*NextHopType* 매개 변수에 대한 VirtualAppliance 값을 지정하는 경우만 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="cfb97-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="cfb97-123">-NextHopType</span></span>
<span data-ttu-id="cfb97-124">이 경로가 패킷을 전달하는 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="cfb97-125">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfb97-126">인터넷.</span><span class="sxs-lookup"><span data-stu-id="cfb97-126">Internet.</span></span>
<span data-ttu-id="cfb97-127">Azure에서 제공하는 기본 인터넷 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="cfb97-128">없음.</span><span class="sxs-lookup"><span data-stu-id="cfb97-128">None.</span></span>
<span data-ttu-id="cfb97-129">이 값을 지정하면 경로가 패킷을 전달하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="cfb97-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="cfb97-130">VirtualAppliance.</span></span>
<span data-ttu-id="cfb97-131">Azure 가상 네트워크에 추가하는 가상 어플라이언스입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="cfb97-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="cfb97-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="cfb97-133">Azureserver-to-server 가상 사설 네트워크 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="cfb97-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="cfb97-134">VnetLocal.</span></span>
<span data-ttu-id="cfb97-135">로컬 가상 네트워크입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-135">The local virtual network.</span></span>
<span data-ttu-id="cfb97-136">동일한 가상 네트워크에 10.1.0.0/16과 10.2.0.0/16의 서브넷이 있는 경우 각 서브넷에 대한 VnetLocal 값을 선택하여 다른 서브넷으로 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="cfb97-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="cfb97-137">-RouteTable</span></span>
<span data-ttu-id="cfb97-138">이 경로가 연결된 경로 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="cfb97-139">-확인</span><span class="sxs-lookup"><span data-stu-id="cfb97-139">-Confirm</span></span>
<span data-ttu-id="cfb97-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfb97-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfb97-141">-WhatIf</span></span>
<span data-ttu-id="cfb97-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfb97-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfb97-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb97-144">CommonParameters</span></span>
<span data-ttu-id="cfb97-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb97-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb97-146">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cfb97-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb97-147">입력</span><span class="sxs-lookup"><span data-stu-id="cfb97-147">INPUTS</span></span>

### <span data-ttu-id="cfb97-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfb97-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="cfb97-149">System.String</span><span class="sxs-lookup"><span data-stu-id="cfb97-149">System.String</span></span>

## <span data-ttu-id="cfb97-150">출력</span><span class="sxs-lookup"><span data-stu-id="cfb97-150">OUTPUTS</span></span>

### <span data-ttu-id="cfb97-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfb97-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="cfb97-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cfb97-152">NOTES</span></span>

## <span data-ttu-id="cfb97-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cfb97-153">RELATED LINKS</span></span>

[<span data-ttu-id="cfb97-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cfb97-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="cfb97-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cfb97-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="cfb97-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cfb97-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="cfb97-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cfb97-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


