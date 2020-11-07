---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 93313b6a2d9623ed518d6e79fabcda8fea5cc7b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702594"
---
# <span data-ttu-id="60fb9-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="60fb9-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="60fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="60fb9-103">부하 분산 장치의 프런트 엔드 IP 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60fb9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60fb9-104">SYNTAX</span></span>

### <span data-ttu-id="60fb9-105">SetByResourceSubnet (기본값)</span><span class="sxs-lookup"><span data-stu-id="60fb9-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60fb9-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="60fb9-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60fb9-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="60fb9-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60fb9-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="60fb9-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60fb9-109">설명은</span><span class="sxs-lookup"><span data-stu-id="60fb9-109">DESCRIPTION</span></span>
<span data-ttu-id="60fb9-110">**AzureRmLoadBalancerFrontendIpConfig** Cmdlet은 Azure 부하 분산 장치에서 프런트 엔드 IP 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="60fb9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="60fb9-111">EXAMPLES</span></span>

### <span data-ttu-id="60fb9-112">예제 1: 부하 분산 장치의 프런트 엔드 IP 구성 수정</span><span class="sxs-lookup"><span data-stu-id="60fb9-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="60fb9-113">첫 번째 명령은 가상 서브넷 이라는 서브넷을 가져온 다음 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="60fb9-114">두 번째 명령은 MyLoadBalancer 라는 연결 된 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="60fb9-115">세 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산 장치를 Add-AzureRmLoadBalancerFrontendIpConfig에 전달 하 여 $slb에 대 한 NewFrontend 이라는 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="60fb9-116">네 번째 명령은 $slb에서 부하 분산 장치를 **Set-AzureRmLoadBalancerFrontendIpConfig** 에 전달 하 여 프런트 엔드 IP 구성을 저장 하 고 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="60fb9-117">변수</span><span class="sxs-lookup"><span data-stu-id="60fb9-117">PARAMETERS</span></span>

### <span data-ttu-id="60fb9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fb9-118">-DefaultProfile</span></span>
<span data-ttu-id="60fb9-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60fb9-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="60fb9-120">-LoadBalancer</span></span>
<span data-ttu-id="60fb9-121">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-121">Specifies a load balancer.</span></span>
<span data-ttu-id="60fb9-122">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 프런트 엔드 구성의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="60fb9-123">-이름</span><span class="sxs-lookup"><span data-stu-id="60fb9-123">-Name</span></span>
<span data-ttu-id="60fb9-124">설정할 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="60fb9-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="60fb9-125">-PrivateIpAddress</span></span>
<span data-ttu-id="60fb9-126">설정할 프런트 엔드 IP 구성에 연결 된 부하 분산 장치의 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="60fb9-127">*서브넷* 매개 변수도 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="60fb9-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="60fb9-128">-PublicIpAddress</span></span>
<span data-ttu-id="60fb9-129">설정할 프런트 엔드 IP 구성에 연결 된 **PublicIpAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="60fb9-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="60fb9-130">-PublicIpAddressId</span></span>
<span data-ttu-id="60fb9-131">이 cmdlet이 설정 하는 프런트 엔드 IP 구성과 연결 된 **PublicIpAddress** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="60fb9-132">-서브넷</span><span class="sxs-lookup"><span data-stu-id="60fb9-132">-Subnet</span></span>
<span data-ttu-id="60fb9-133">이 cmdlet이 설정 하는 프런트 엔드 IP 구성을 포함 하는 **Subnet** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="60fb9-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="60fb9-134">-SubnetId</span></span>
<span data-ttu-id="60fb9-135">이 cmdlet이 설정 하는 프런트 엔드 IP 구성을 포함 하는 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="60fb9-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="60fb9-136">-Zone</span></span>
<span data-ttu-id="60fb9-137">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="60fb9-138">-확인</span><span class="sxs-lookup"><span data-stu-id="60fb9-138">-Confirm</span></span>
<span data-ttu-id="60fb9-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60fb9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60fb9-140">-WhatIf</span></span>
<span data-ttu-id="60fb9-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60fb9-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60fb9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fb9-143">CommonParameters</span></span>
<span data-ttu-id="60fb9-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fb9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fb9-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60fb9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fb9-146">입력</span><span class="sxs-lookup"><span data-stu-id="60fb9-146">INPUTS</span></span>

### <span data-ttu-id="60fb9-147">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="60fb9-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="60fb9-148">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="60fb9-148">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="60fb9-149">System.webserver. 목록 \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="60fb9-149">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="60fb9-150">출력</span><span class="sxs-lookup"><span data-stu-id="60fb9-150">OUTPUTS</span></span>

### <span data-ttu-id="60fb9-151">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="60fb9-151">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="60fb9-152">상속자</span><span class="sxs-lookup"><span data-stu-id="60fb9-152">NOTES</span></span>

## <span data-ttu-id="60fb9-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60fb9-153">RELATED LINKS</span></span>

[<span data-ttu-id="60fb9-154">추가-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="60fb9-154">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="60fb9-155">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="60fb9-155">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="60fb9-156">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="60fb9-156">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="60fb9-157">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="60fb9-157">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="60fb9-158">새로운 AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="60fb9-158">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="60fb9-159">제거-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="60fb9-159">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


