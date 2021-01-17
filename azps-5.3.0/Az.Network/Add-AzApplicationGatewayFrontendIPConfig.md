---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380346"
---
# <span data-ttu-id="385f4-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="385f4-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="385f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="385f4-102">SYNOPSIS</span></span>
<span data-ttu-id="385f4-103">애플리케이션 게이트웨이에 프런트 엔드 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="385f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="385f4-104">SYNTAX</span></span>

### <span data-ttu-id="385f4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="385f4-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="385f4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="385f4-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="385f4-107">설명</span><span class="sxs-lookup"><span data-stu-id="385f4-107">DESCRIPTION</span></span>
<span data-ttu-id="385f4-108">**Add-AzApplicationGatewayFrontendIPConfig** cmdlet은 애플리케이션 게이트웨이에 프런트 엔드 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="385f4-109">애플리케이션 게이트웨이는 두 가지 유형의 프런트 엔드 IP 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="385f4-110">공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="385f4-110">Public IP addresses</span></span>
- <span data-ttu-id="385f4-111">ILB(내부 부하 분산)를 사용하는 개인 IP 주소는 애플리케이션 게이트웨이에 최대 하나의 공용 IP와 하나의 개인 IP를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="385f4-112">공용 IP 주소 및 개인 IP 주소를 별도의 프런트 엔드 IP로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="385f4-113">예제</span><span class="sxs-lookup"><span data-stu-id="385f4-113">EXAMPLES</span></span>

### <span data-ttu-id="385f4-114">예제 1: 공용 IP를 프런트 엔드 IP 주소로 추가</span><span class="sxs-lookup"><span data-stu-id="385f4-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="385f4-115">첫 번째 명령은 공용 IP 주소 개체를 만들고 공용 ip 주소 $PublicIp 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="385f4-116">두 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 사용하여 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="385f4-117">세 번째 명령은 $AppGw 저장된 주소를 사용하여 FrontEndIp01이라는 프런트 엔드 IP 구성을 $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="385f4-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="385f4-118">예제 2: 정적 개인 IP를 프런트 엔드 IP 주소로 추가</span><span class="sxs-lookup"><span data-stu-id="385f4-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="385f4-119">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 $VNet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="385f4-120">두 번째 명령은 첫 번째 명령에서 $VNet 사용하여 Subnet01이라는 서브넷 구성을 $Subnet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="385f4-121">세 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 사용하여 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="385f4-122">네 번째 명령은 두 번째 명령의 $Subnet 개인 IP 주소 10.0.1.1을 사용하여 FrontendIP02라는 프런트 엔드 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="385f4-123">예제 3: 동적 개인 IP를 프런트 엔드 IP 주소로 추가</span><span class="sxs-lookup"><span data-stu-id="385f4-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="385f4-124">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 $VNet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="385f4-125">두 번째 명령은 첫 번째 명령에서 $VNet 사용하여 Subnet01이라는 서브넷 구성을 $Subnet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="385f4-126">세 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 사용하여 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="385f4-127">네 번째 명령은 두 번째 명령의 명령을 사용하여 FrontendIP02라는 $Subnet IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="385f4-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="385f4-128">PARAMETERS</span></span>

### <span data-ttu-id="385f4-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="385f4-129">-ApplicationGateway</span></span>
<span data-ttu-id="385f4-130">이 cmdlet이 프런트 엔드 IP 구성을 추가하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="385f4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385f4-131">-DefaultProfile</span></span>
<span data-ttu-id="385f4-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385f4-133">-Name</span><span class="sxs-lookup"><span data-stu-id="385f4-133">-Name</span></span>
<span data-ttu-id="385f4-134">추가할 프런트 엔드 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="385f4-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="385f4-135">-PrivateIPAddress</span></span>
<span data-ttu-id="385f4-136">애플리케이션 게이트웨이에 대한 프런트 엔드 IP로 추가할 개인 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="385f4-137">지정된 경우 이 IP는 서브넷에서 정적으로 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="385f4-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="385f4-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="385f4-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="385f4-139">PrivateLinkConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385f4-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="385f4-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="385f4-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="385f4-141">PrivateLinkConfigurationId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385f4-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="385f4-142">-PublicIPAddress</span></span>
<span data-ttu-id="385f4-143">이 cmdlet이 애플리케이션 게이트웨이에 대한 프런트 엔드 IP 주소로 추가하는 공용 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385f4-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="385f4-144">-PublicIPAddressId</span></span>
<span data-ttu-id="385f4-145">이 cmdlet이 애플리케이션 게이트웨이에 대한 프런트 엔드 IP 주소로 추가하는 공용 IP 주소의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385f4-146">-Subnet</span><span class="sxs-lookup"><span data-stu-id="385f4-146">-Subnet</span></span>
<span data-ttu-id="385f4-147">이 cmdlet이 프런트 엔드 IP 구성으로 추가하는 서브넷을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="385f4-148">이 매개 변수를 지정하는 경우 애플리케이션 게이트웨이가 개인 IP 기반 구성을 지원하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="385f4-149">*PrivateIPAddress* 매개 변수가 지정된 경우 이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="385f4-150">*PrivateIPAddress를* 지정하지 않으면 이 서브넷의 IP 주소 중 하나는 애플리케이션 게이트웨이의 프런트 엔드 IP 주소로 동적으로 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385f4-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="385f4-151">-SubnetId</span></span>
<span data-ttu-id="385f4-152">이 cmdlet이 프런트 엔드 IP 구성으로 추가하는 서브넷 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="385f4-153">서브넷 전달은 개인 IP를 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="385f4-154">*PrivateIPAddress* 매개 변수가 지정된 경우 이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="385f4-155">그렇지 않은 경우 이 서브넷의 IP 중 하나는 애플리케이션 게이트웨이의 프런트 엔드 IP로 동적으로 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385f4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385f4-156">CommonParameters</span></span>
<span data-ttu-id="385f4-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="385f4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385f4-158">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="385f4-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385f4-159">입력</span><span class="sxs-lookup"><span data-stu-id="385f4-159">INPUTS</span></span>

### <span data-ttu-id="385f4-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="385f4-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="385f4-161">출력</span><span class="sxs-lookup"><span data-stu-id="385f4-161">OUTPUTS</span></span>

### <span data-ttu-id="385f4-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="385f4-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="385f4-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="385f4-163">NOTES</span></span>

## <span data-ttu-id="385f4-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="385f4-164">RELATED LINKS</span></span>

[<span data-ttu-id="385f4-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="385f4-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="385f4-166">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="385f4-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="385f4-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="385f4-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="385f4-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="385f4-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


