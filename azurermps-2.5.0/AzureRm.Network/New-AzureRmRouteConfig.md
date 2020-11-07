---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: ab528e837f6f2e45db5e68430d973e0d8f019850
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882610"
---
# <span data-ttu-id="3cb31-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3cb31-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="3cb31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cb31-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb31-103">경로 테이블에 대 한 경로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cb31-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3cb31-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig [-AddressPrefix <String>] [-NextHopType <String>] [-NextHopIpAddress <String>]
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cb31-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3cb31-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb31-106">**AzureRmRouteConfig** Cmdlet은 Azure 경로 테이블에 대 한 경로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="3cb31-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3cb31-107">EXAMPLES</span></span>

### <span data-ttu-id="3cb31-108">예제 1: 경로 만들기</span><span class="sxs-lookup"><span data-stu-id="3cb31-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="3cb31-109">첫 번째 명령은 Route07 이라는 경로를 만든 다음이를 $Route 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="3cb31-110">이 경로는 패킷을 로컬 가상 네트워크에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="3cb31-111">두 번째 명령은 경로의 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="3cb31-112">변수</span><span class="sxs-lookup"><span data-stu-id="3cb31-112">PARAMETERS</span></span>

### <span data-ttu-id="3cb31-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3cb31-113">-AddressPrefix</span></span>
<span data-ttu-id="3cb31-114">경로가 적용 되는 대상을 클래스를 도메인간 라우팅 (CIDR) 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="3cb31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb31-115">-DefaultProfile</span></span>
<span data-ttu-id="3cb31-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cb31-117">-이름</span><span class="sxs-lookup"><span data-stu-id="3cb31-117">-Name</span></span>
<span data-ttu-id="3cb31-118">경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="3cb31-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="3cb31-119">-NextHopIpAddress</span></span>
<span data-ttu-id="3cb31-120">Azurevirtual 네트워크에 추가 하는 가상 기기의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="3cb31-121">이 경로는 패킷을 해당 주소로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="3cb31-122">*NextHopType* 매개 변수에 virtualappliance 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="3cb31-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="3cb31-123">-NextHopType</span></span>
<span data-ttu-id="3cb31-124">이 경로에서 패킷을 전달 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="3cb31-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3cb31-126">인터넷.</span><span class="sxs-lookup"><span data-stu-id="3cb31-126">Internet.</span></span>
<span data-ttu-id="3cb31-127">Azure에서 제공 하는 기본 인터넷 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="3cb31-128">않아야.</span><span class="sxs-lookup"><span data-stu-id="3cb31-128">None.</span></span>
<span data-ttu-id="3cb31-129">이 값을 지정 하는 경우 경로는 패킷을 전달 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="3cb31-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="3cb31-130">VirtualAppliance.</span></span>
<span data-ttu-id="3cb31-131">Azure 가상 네트워크에 추가 하는 가상 어플라이언스</span><span class="sxs-lookup"><span data-stu-id="3cb31-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="3cb31-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="3cb31-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="3cb31-133">Azure 서버 간 가상 개인 네트워크 게이트웨이.</span><span class="sxs-lookup"><span data-stu-id="3cb31-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="3cb31-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="3cb31-134">VnetLocal.</span></span>
<span data-ttu-id="3cb31-135">로컬 가상 네트워크.</span><span class="sxs-lookup"><span data-stu-id="3cb31-135">The local virtual network.</span></span>
<span data-ttu-id="3cb31-136">동일한 가상 네트워크에 두 개의 서브넷, 10.1.0.0/16, 10.2.0.0/16이 있는 경우 각 서브넷에 대 한 VnetLocal 값을 선택 하 여 다른 서브넷으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="3cb31-137">-확인</span><span class="sxs-lookup"><span data-stu-id="3cb31-137">-Confirm</span></span>
<span data-ttu-id="3cb31-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cb31-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb31-139">-WhatIf</span></span>
<span data-ttu-id="3cb31-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cb31-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cb31-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb31-142">CommonParameters</span></span>
<span data-ttu-id="3cb31-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb31-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb31-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cb31-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb31-145">입력</span><span class="sxs-lookup"><span data-stu-id="3cb31-145">INPUTS</span></span>

## <span data-ttu-id="3cb31-146">출력</span><span class="sxs-lookup"><span data-stu-id="3cb31-146">OUTPUTS</span></span>

### <span data-ttu-id="3cb31-147">Microsoft. 네트워크 모델. PSRoute</span><span class="sxs-lookup"><span data-stu-id="3cb31-147">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="3cb31-148">상속자</span><span class="sxs-lookup"><span data-stu-id="3cb31-148">NOTES</span></span>

## <span data-ttu-id="3cb31-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cb31-149">RELATED LINKS</span></span>

[<span data-ttu-id="3cb31-150">추가-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3cb31-150">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="3cb31-151">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3cb31-151">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="3cb31-152">제거-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3cb31-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="3cb31-153">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3cb31-153">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


