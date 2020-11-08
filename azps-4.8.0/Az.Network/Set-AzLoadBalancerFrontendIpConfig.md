---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b9f7767554efe6a91ea0989e4d37eec7c4832708
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048837"
---
# <span data-ttu-id="5bea8-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5bea8-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="5bea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bea8-102">SYNOPSIS</span></span>
<span data-ttu-id="5bea8-103">부하 분산 장치에 대 한 프런트 엔드 IP 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="5bea8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5bea8-104">SYNTAX</span></span>

### <span data-ttu-id="5bea8-105">SetByResourceSubnet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5bea8-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bea8-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="5bea8-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bea8-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5bea8-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bea8-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5bea8-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bea8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="5bea8-109">DESCRIPTION</span></span>
<span data-ttu-id="5bea8-110">**AzLoadBalancerFrontendIpConfig** cmdlet은 부하 분산 장치에 대 한 프런트 엔드 IP 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="5bea8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5bea8-111">EXAMPLES</span></span>

### <span data-ttu-id="5bea8-112">예제 1: 부하 분산 장치의 프런트 엔드 IP 구성 수정</span><span class="sxs-lookup"><span data-stu-id="5bea8-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="5bea8-113">첫 번째 명령은 가상 서브넷 이라는 서브넷을 가져온 다음 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="5bea8-114">두 번째 명령은 MyLoadBalancer 라는 연결 된 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="5bea8-115">세 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산 장치를 Add-AzLoadBalancerFrontendIpConfig에 전달 하 여 $slb에 대 한 NewFrontend 이라는 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="5bea8-116">네 번째 명령은 $slb에서 부하 분산 장치를 **Set-AzLoadBalancerFrontendIpConfig** 에 전달 하 여 프런트 엔드 IP 구성을 저장 하 고 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="5bea8-117">변수</span><span class="sxs-lookup"><span data-stu-id="5bea8-117">PARAMETERS</span></span>

### <span data-ttu-id="5bea8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bea8-118">-DefaultProfile</span></span>
<span data-ttu-id="5bea8-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bea8-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bea8-120">-LoadBalancer</span></span>
<span data-ttu-id="5bea8-121">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-121">Specifies a load balancer.</span></span>
<span data-ttu-id="5bea8-122">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 프런트 엔드 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-122">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-123">-이름</span><span class="sxs-lookup"><span data-stu-id="5bea8-123">-Name</span></span>
<span data-ttu-id="5bea8-124">설정할 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="5bea8-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="5bea8-125">-PrivateIpAddress</span></span>
<span data-ttu-id="5bea8-126">설정할 프런트 엔드 IP 구성에 연결 된 부하 분산 장치의 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="5bea8-127">*서브넷* 매개 변수도 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="5bea8-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="5bea8-129">IP 구성의 개인 IP 주소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-129">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5bea8-130">-PublicIpAddress</span></span>
<span data-ttu-id="5bea8-131">설정할 프런트 엔드 IP 구성에 연결 된 **PublicIpAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-131">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="5bea8-132">-PublicIpAddressId</span></span>
<span data-ttu-id="5bea8-133">이 cmdlet이 설정 하는 프런트 엔드 IP 구성과 연결 된 **PublicIpAddress** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-133">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-134">-서브넷</span><span class="sxs-lookup"><span data-stu-id="5bea8-134">-Subnet</span></span>
<span data-ttu-id="5bea8-135">이 cmdlet이 설정 하는 프런트 엔드 IP 구성을 포함 하는 **Subnet** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-135">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-136">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5bea8-136">-SubnetId</span></span>
<span data-ttu-id="5bea8-137">이 cmdlet이 설정 하는 프런트 엔드 IP 구성을 포함 하는 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-137">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-138">-Zone</span><span class="sxs-lookup"><span data-stu-id="5bea8-138">-Zone</span></span>
<span data-ttu-id="5bea8-139">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-139">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-140">-확인</span><span class="sxs-lookup"><span data-stu-id="5bea8-140">-Confirm</span></span>
<span data-ttu-id="5bea8-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bea8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bea8-142">-WhatIf</span></span>
<span data-ttu-id="5bea8-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bea8-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bea8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bea8-145">CommonParameters</span></span>
<span data-ttu-id="5bea8-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bea8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bea8-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5bea8-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bea8-148">입력</span><span class="sxs-lookup"><span data-stu-id="5bea8-148">INPUTS</span></span>

### <span data-ttu-id="5bea8-149">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bea8-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="5bea8-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5bea8-150">System.String</span></span>

### <span data-ttu-id="5bea8-151">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="5bea8-151">System.String[]</span></span>

### <span data-ttu-id="5bea8-152">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5bea8-152">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="5bea8-153">PSPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5bea8-153">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="5bea8-154">출력</span><span class="sxs-lookup"><span data-stu-id="5bea8-154">OUTPUTS</span></span>

### <span data-ttu-id="5bea8-155">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bea8-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5bea8-156">상속자</span><span class="sxs-lookup"><span data-stu-id="5bea8-156">NOTES</span></span>

## <span data-ttu-id="5bea8-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bea8-157">RELATED LINKS</span></span>

[<span data-ttu-id="5bea8-158">추가-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5bea8-158">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5bea8-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bea8-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5bea8-160">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5bea8-160">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5bea8-161">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5bea8-161">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="5bea8-162">새로운 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5bea8-162">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5bea8-163">제거-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5bea8-163">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


