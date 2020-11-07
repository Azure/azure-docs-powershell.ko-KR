---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 2dba7d00ea308225736de6714c90c74b0ce30837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700711"
---
# <span data-ttu-id="7e8d0-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e8d0-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="7e8d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="7e8d0-103">부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="7e8d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e8d0-104">SYNTAX</span></span>

### <span data-ttu-id="7e8d0-105">SetByResourceSubnet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7e8d0-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e8d0-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="7e8d0-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e8d0-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e8d0-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e8d0-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e8d0-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e8d0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="7e8d0-109">DESCRIPTION</span></span>
<span data-ttu-id="7e8d0-110">**Add-AzLoadBalancerFrontendIpConifg** Cmdlet은 Azure 부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-110">The **Add-AzLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="7e8d0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7e8d0-111">EXAMPLES</span></span>

### <span data-ttu-id="7e8d0-112">예제 1 동적 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="7e8d0-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="7e8d0-113">첫 번째 명령은 MyVnet 이라는 Azure 가상 네트워크를 가져오고 파이프라인을 사용 하 여 **AzVirtualNetworkSubnetConfig** cmdlet에 대 한 결과를 전달 하 여 myvnet 이라는 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="7e8d0-114">그런 다음 명령을 $Subnet 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="7e8d0-115">두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 **AzLoadBalancerFrontendIpConfig** cmdlet에 전달 하며,이는 $MySubnet 이라는 변수에 저장 된 서브넷의 동적 개인 ip 주소를 사용 하 여 로드 균형 조정기에 프런트 엔드 ip 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="7e8d0-116">예제 2 고정 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="7e8d0-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="7e8d0-117">첫 번째 명령은 MyVnet 이라는 Azure 가상 네트워크를 가져오고 파이프라인을 사용 하 여 **AzVirtualNetworkSubnetConfig** cmdlet에 대 한 결과를 전달 하 여 myvnet 이라는 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="7e8d0-118">그런 다음 명령을 $Subnet 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="7e8d0-119">두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 **AzLoadBalancerFrontendIpConfig** cmdlet에 전달 하며,이는 $Subnet 이라는 변수에 저장 된 서브넷의 고정 개인 ip 주소를 사용 하 여 로드 균형 조정기에 프런트 엔드 ip 구성을 추가 하는 것을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="7e8d0-120">예제 3 공용 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="7e8d0-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="7e8d0-121">첫 번째 명령은 MyPub 이라는 Azure 공개 IP 주소를 가져온 다음 그 결과를 $PublicIp 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="7e8d0-122">두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 AzLoadBalancerFrontendIpConfig cmdlet에 전달 하 고 공용 IP 주소가 $PublicIp 라는 변수에 저장 된 부하 분산에 프런트 엔드 IP 구성을 추가 하는 결과를 **추가** 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="7e8d0-123">변수</span><span class="sxs-lookup"><span data-stu-id="7e8d0-123">PARAMETERS</span></span>

### <span data-ttu-id="7e8d0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e8d0-124">-DefaultProfile</span></span>
<span data-ttu-id="7e8d0-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e8d0-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7e8d0-126">-LoadBalancer</span></span>
<span data-ttu-id="7e8d0-127">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="7e8d0-128">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="7e8d0-129">-이름</span><span class="sxs-lookup"><span data-stu-id="7e8d0-129">-Name</span></span>
<span data-ttu-id="7e8d0-130">추가할 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="7e8d0-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e8d0-131">-PrivateIpAddress</span></span>
<span data-ttu-id="7e8d0-132">프런트 엔드 IP 구성에 연결할 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7e8d0-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e8d0-133">-PublicIpAddress</span></span>
<span data-ttu-id="7e8d0-134">프런트 엔드 IP 구성과 연결할 공용 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7e8d0-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7e8d0-135">-PublicIpAddressId</span></span>
<span data-ttu-id="7e8d0-136">프런트 엔드 IP 구성을 추가할 공용 IP 주소의 ID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7e8d0-137">-서브넷</span><span class="sxs-lookup"><span data-stu-id="7e8d0-137">-Subnet</span></span>
<span data-ttu-id="7e8d0-138">프런트 엔드 IP 구성을 추가할 서브넷 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7e8d0-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7e8d0-139">-SubnetId</span></span>
<span data-ttu-id="7e8d0-140">프런트 엔드 IP 구성을 추가할 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7e8d0-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="7e8d0-141">-Zone</span></span>
<span data-ttu-id="7e8d0-142">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="7e8d0-143">-확인</span><span class="sxs-lookup"><span data-stu-id="7e8d0-143">-Confirm</span></span>
<span data-ttu-id="7e8d0-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e8d0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e8d0-145">-WhatIf</span></span>
<span data-ttu-id="7e8d0-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e8d0-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e8d0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e8d0-148">CommonParameters</span></span>
<span data-ttu-id="7e8d0-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e8d0-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e8d0-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e8d0-151">입력</span><span class="sxs-lookup"><span data-stu-id="7e8d0-151">INPUTS</span></span>

### <span data-ttu-id="7e8d0-152">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7e8d0-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="7e8d0-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e8d0-153">System.String</span></span>

### <span data-ttu-id="7e8d0-154">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="7e8d0-154">System.String[]</span></span>

### <span data-ttu-id="7e8d0-155">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7e8d0-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="7e8d0-156">PSPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7e8d0-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7e8d0-157">출력</span><span class="sxs-lookup"><span data-stu-id="7e8d0-157">OUTPUTS</span></span>

### <span data-ttu-id="7e8d0-158">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7e8d0-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7e8d0-159">상속자</span><span class="sxs-lookup"><span data-stu-id="7e8d0-159">NOTES</span></span>

## <span data-ttu-id="7e8d0-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e8d0-160">RELATED LINKS</span></span>

[<span data-ttu-id="7e8d0-161">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e8d0-161">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7e8d0-162">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e8d0-162">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7e8d0-163">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7e8d0-163">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7e8d0-164">새로운 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e8d0-164">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7e8d0-165">제거-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e8d0-165">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7e8d0-166">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e8d0-166">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)

