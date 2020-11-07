---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 8de9d162ceba8dc436d5244f75011b79a949ddeb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882562"
---
# <span data-ttu-id="ae010-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae010-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="ae010-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae010-102">SYNOPSIS</span></span>
<span data-ttu-id="ae010-103">부하 분산 장치의 프런트 엔드 IP 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae010-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae010-104">SYNTAX</span></span>

### <span data-ttu-id="ae010-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="ae010-105">SetByResourceSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae010-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="ae010-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae010-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ae010-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae010-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ae010-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae010-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ae010-109">DESCRIPTION</span></span>
<span data-ttu-id="ae010-110">**AzureRmLoadBalancerFrontendIpConfig** Cmdlet은 Azure 부하 분산 장치에서 프런트 엔드 IP 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="ae010-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ae010-111">EXAMPLES</span></span>

### <span data-ttu-id="ae010-112">예제 1: 부하 분산 장치의 프런트 엔드 IP 구성 수정</span><span class="sxs-lookup"><span data-stu-id="ae010-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="ae010-113">첫 번째 명령은 가상 서브넷 이라는 서브넷을 가져온 다음 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="ae010-114">두 번째 명령은 MyLoadBalancer 라는 연결 된 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="ae010-115">세 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산 장치를 Add-AzureRmLoadBalancerFrontendIpConfig에 전달 하 여 $slb에 대 한 NewFrontend 이라는 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="ae010-116">네 번째 명령은 $slb에서 부하 분산 장치를 **Set-AzureRmLoadBalancerFrontendIpConfig** 에 전달 하 여 프런트 엔드 IP 구성을 저장 하 고 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="ae010-117">변수</span><span class="sxs-lookup"><span data-stu-id="ae010-117">PARAMETERS</span></span>

### <span data-ttu-id="ae010-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae010-118">-DefaultProfile</span></span>
<span data-ttu-id="ae010-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae010-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae010-120">-LoadBalancer</span></span>
<span data-ttu-id="ae010-121">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-121">Specifies a load balancer.</span></span>
<span data-ttu-id="ae010-122">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 프런트 엔드 구성의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae010-123">-이름</span><span class="sxs-lookup"><span data-stu-id="ae010-123">-Name</span></span>
<span data-ttu-id="ae010-124">설정할 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-124">Specifies the name of the front-end IP configuration to set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae010-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ae010-125">-PrivateIpAddress</span></span>
<span data-ttu-id="ae010-126">설정할 프런트 엔드 IP 구성에 연결 된 부하 분산 장치의 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="ae010-127">*서브넷* 매개 변수도 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae010-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ae010-128">-PublicIpAddress</span></span>
<span data-ttu-id="ae010-129">설정할 프런트 엔드 IP 구성에 연결 된 **PublicIpAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae010-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="ae010-130">-PublicIpAddressId</span></span>
<span data-ttu-id="ae010-131">이 cmdlet이 설정 하는 프런트 엔드 IP 구성과 연결 된 **PublicIpAddress** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae010-132">-서브넷</span><span class="sxs-lookup"><span data-stu-id="ae010-132">-Subnet</span></span>
<span data-ttu-id="ae010-133">이 cmdlet이 설정 하는 프런트 엔드 IP 구성을 포함 하는 **Subnet** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae010-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ae010-134">-SubnetId</span></span>
<span data-ttu-id="ae010-135">이 cmdlet이 설정 하는 프런트 엔드 IP 구성을 포함 하는 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae010-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="ae010-136">-Zone</span></span>
<span data-ttu-id="ae010-137">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae010-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae010-138">CommonParameters</span></span>
<span data-ttu-id="ae010-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae010-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae010-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae010-141">입력</span><span class="sxs-lookup"><span data-stu-id="ae010-141">INPUTS</span></span>

### <span data-ttu-id="ae010-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae010-142">PSLoadBalancer</span></span>
<span data-ttu-id="ae010-143">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae010-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ae010-144">출력</span><span class="sxs-lookup"><span data-stu-id="ae010-144">OUTPUTS</span></span>

### <span data-ttu-id="ae010-145">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae010-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ae010-146">상속자</span><span class="sxs-lookup"><span data-stu-id="ae010-146">NOTES</span></span>

## <span data-ttu-id="ae010-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae010-147">RELATED LINKS</span></span>

[<span data-ttu-id="ae010-148">추가-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae010-148">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ae010-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae010-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ae010-150">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae010-150">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ae010-151">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ae010-151">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ae010-152">새로운 AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae010-152">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ae010-153">제거-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae010-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


