---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: f54527b167fa15ea4c4e878b81d86a00079e28a0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883041"
---
# <span data-ttu-id="692a9-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="692a9-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="692a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="692a9-102">SYNOPSIS</span></span>
<span data-ttu-id="692a9-103">부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="692a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="692a9-104">SYNTAX</span></span>

### <span data-ttu-id="692a9-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="692a9-105">SetByResourceSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="692a9-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="692a9-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="692a9-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="692a9-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="692a9-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="692a9-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="692a9-109">설명은</span><span class="sxs-lookup"><span data-stu-id="692a9-109">DESCRIPTION</span></span>
<span data-ttu-id="692a9-110">**Add-AzureRmLoadBalancerFrontendIpConifg** Cmdlet은 Azure 부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="692a9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="692a9-111">EXAMPLES</span></span>

### <span data-ttu-id="692a9-112">예제 1 동적 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="692a9-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="692a9-113">첫 번째 명령은 MyVnet 이라는 Azure 가상 네트워크를 가져오고 파이프라인을 사용 하 여 **AzureRmVirtualNetworkSubnetConfig** cmdlet에 대 한 결과를 전달 하 여 myvnet 이라는 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="692a9-114">그런 다음 명령을 $Subnet 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="692a9-115">두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 **AzureRmLoadBalancerFrontendIpConfig** cmdlet에 전달 하며,이는 $MySubnet 이라는 변수에 저장 된 서브넷의 동적 개인 ip 주소를 사용 하 여 로드 균형 조정기에 프런트 엔드 ip 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="692a9-116">예제 2 고정 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="692a9-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="692a9-117">첫 번째 명령은 MyVnet 이라는 Azure 가상 네트워크를 가져오고 파이프라인을 사용 하 여 **AzureRmVirtualNetworkSubnetConfig** cmdlet에 대 한 결과를 전달 하 여 myvnet 이라는 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="692a9-118">그런 다음 명령을 $Subnet 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="692a9-119">두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 **AzureRmLoadBalancerFrontendIpConfig** cmdlet에 전달 하며,이는 $Subnet 이라는 변수에 저장 된 서브넷의 고정 개인 ip 주소를 사용 하 여 로드 균형 조정기에 프런트 엔드 ip 구성을 추가 하는 것을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="692a9-120">예제 3 공용 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="692a9-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="692a9-121">첫 번째 명령은 MyPub 이라는 Azure 공개 IP 주소를 가져온 다음 그 결과를 $PublicIp 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="692a9-122">두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 AzureRmLoadBalancerFrontendIpConfig cmdlet에 전달 하 고 공용 IP 주소가 $PublicIp 라는 변수에 저장 된 부하 분산에 프런트 엔드 IP 구성을 추가 하는 결과를 **추가** 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="692a9-123">변수</span><span class="sxs-lookup"><span data-stu-id="692a9-123">PARAMETERS</span></span>

### <span data-ttu-id="692a9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="692a9-124">-DefaultProfile</span></span>
<span data-ttu-id="692a9-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="692a9-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="692a9-126">-LoadBalancer</span></span>
<span data-ttu-id="692a9-127">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="692a9-128">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="692a9-129">-이름</span><span class="sxs-lookup"><span data-stu-id="692a9-129">-Name</span></span>
<span data-ttu-id="692a9-130">추가할 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="692a9-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="692a9-131">-PrivateIpAddress</span></span>
<span data-ttu-id="692a9-132">프런트 엔드 IP 구성에 연결할 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="692a9-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="692a9-133">-PublicIpAddress</span></span>
<span data-ttu-id="692a9-134">프런트 엔드 IP 구성과 연결할 공용 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="692a9-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="692a9-135">-PublicIpAddressId</span></span>
<span data-ttu-id="692a9-136">프런트 엔드 IP 구성을 추가할 공용 IP 주소의 ID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="692a9-137">-서브넷</span><span class="sxs-lookup"><span data-stu-id="692a9-137">-Subnet</span></span>
<span data-ttu-id="692a9-138">프런트 엔드 IP 구성을 추가할 서브넷 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="692a9-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="692a9-139">-SubnetId</span></span>
<span data-ttu-id="692a9-140">프런트 엔드 IP 구성을 추가할 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="692a9-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="692a9-141">-Zone</span></span>
<span data-ttu-id="692a9-142">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="692a9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692a9-143">CommonParameters</span></span>
<span data-ttu-id="692a9-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692a9-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="692a9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692a9-146">입력</span><span class="sxs-lookup"><span data-stu-id="692a9-146">INPUTS</span></span>

### <span data-ttu-id="692a9-147">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="692a9-147">PSLoadBalancer</span></span>
<span data-ttu-id="692a9-148">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="692a9-148">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="692a9-149">출력</span><span class="sxs-lookup"><span data-stu-id="692a9-149">OUTPUTS</span></span>

### <span data-ttu-id="692a9-150">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="692a9-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="692a9-151">상속자</span><span class="sxs-lookup"><span data-stu-id="692a9-151">NOTES</span></span>

## <span data-ttu-id="692a9-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="692a9-152">RELATED LINKS</span></span>

[<span data-ttu-id="692a9-153">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="692a9-153">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="692a9-154">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="692a9-154">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="692a9-155">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="692a9-155">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="692a9-156">새로운 AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="692a9-156">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="692a9-157">제거-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="692a9-157">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="692a9-158">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="692a9-158">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)

