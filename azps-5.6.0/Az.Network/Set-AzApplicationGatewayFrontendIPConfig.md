---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 17ef06c6f91f650da95ddcbfb87b09a60c1948d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956784"
---
# <span data-ttu-id="9b985-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9b985-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="9b985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b985-102">SYNOPSIS</span></span>
<span data-ttu-id="9b985-103">프런트 엔드 IP 주소 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="9b985-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b985-104">SYNTAX</span></span>

### <span data-ttu-id="9b985-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b985-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b985-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9b985-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b985-107">설명</span><span class="sxs-lookup"><span data-stu-id="9b985-107">DESCRIPTION</span></span>
<span data-ttu-id="9b985-108">**Set-AzApplicationGatewayFrontendIPConfig** cmdlet은 프런트 엔드 IP 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="9b985-109">애플리케이션 게이트웨이는 두 가지 유형의 프런트 엔드 IP 주소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="9b985-110">공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="9b985-110">Public IP addresses</span></span>
- <span data-ttu-id="9b985-111">구성이 ILB(내부 부하 분산)를 사용하는 개인 IP 주소는 애플리케이션 게이트웨이에 최대 하나의 공용 IP 주소와 하나의 개인 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="9b985-112">공용 IP 주소 및 개인 IP 주소는 프런트 엔드 IP 주소로 별도로 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="9b985-113">예제</span><span class="sxs-lookup"><span data-stu-id="9b985-113">EXAMPLES</span></span>

### <span data-ttu-id="9b985-114">예제 1: 애플리케이션 게이트웨이의 프런트 엔드 IP로 공용 IP 설정</span><span class="sxs-lookup"><span data-stu-id="9b985-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="9b985-115">첫 번째 명령은 공용 IP 주소 개체를 만들고 해당 개체를 $PublicIp 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="9b985-116">두 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9b985-117">세 번째 명령은 프런트 엔드 IP 구성인 FrontEndIp01을 업데이트하고 $AppGw 에 저장된 주소를 사용하여 $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="9b985-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="9b985-118">예제 2: 애플리케이션 게이트웨이의 프런트 엔드 IP로 정적 개인 IP 설정</span><span class="sxs-lookup"><span data-stu-id="9b985-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="9b985-119">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 얻게 $VNet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="9b985-120">두 번째 명령은 첫 번째 명령에서 $VNet 사용하여 Subnet01이라는 서브넷 구성을 $Subnet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="9b985-121">세 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9b985-122">네 번째 명령은 두 번째 명령 및 $Subnet IP 주소 10.0.1.1을 사용하여 FrontendIP02라는 프런트 엔드 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="9b985-123">예제 3: 동적 개인 IP를 애플리케이션 게이트웨이의 프런트 엔드 IP로 설정</span><span class="sxs-lookup"><span data-stu-id="9b985-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="9b985-124">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 얻게 $VNet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="9b985-125">두 번째 명령은 첫 번째 명령에서 $VNet 사용하여 Subnet01이라는 서브넷 구성을 $Subnet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="9b985-126">세 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9b985-127">네 번째 명령은 두 번째 명령의 $Subnet 사용하여 FrontendIP02라는 프런트 엔드 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="9b985-128">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9b985-128">PARAMETERS</span></span>

### <span data-ttu-id="9b985-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b985-129">-ApplicationGateway</span></span>
<span data-ttu-id="9b985-130">프런트 엔드 IP 구성을 수정할 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="9b985-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b985-131">-DefaultProfile</span></span>
<span data-ttu-id="9b985-132">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b985-133">-Name</span><span class="sxs-lookup"><span data-stu-id="9b985-133">-Name</span></span>
<span data-ttu-id="9b985-134">이 cmdlet이 수정하는 프런트 엔드 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9b985-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="9b985-135">-PrivateIPAddress</span></span>
<span data-ttu-id="9b985-136">개인 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-136">Specifies the private IP address.</span></span>
<span data-ttu-id="9b985-137">지정한 경우 이 IP는 서브넷에서 정적으로 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="9b985-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b985-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="9b985-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b985-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="9b985-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9b985-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="9b985-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9b985-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="9b985-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="9b985-142">-PublicIPAddress</span></span>
<span data-ttu-id="9b985-143">공용 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="9b985-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="9b985-144">-PublicIPAddressId</span></span>
<span data-ttu-id="9b985-145">공용 IP 주소의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="9b985-146">-서브넷</span><span class="sxs-lookup"><span data-stu-id="9b985-146">-Subnet</span></span>
<span data-ttu-id="9b985-147">애플리케이션 게이트웨이에서 사용하는 서브넷을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="9b985-148">게이트웨이에서 개인 IP 주소를 사용하는 경우 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="9b985-149">*PrivateIPAddress* 주소가 지정되어 있는 경우 이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="9b985-150">*PrivateIPAddress를* 지정하지 않으면 이 서브넷의 IP 주소 중 하나를 애플리케이션 게이트웨이의 프런트 엔드 IP 주소로 동적으로 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="9b985-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9b985-151">-SubnetId</span></span>
<span data-ttu-id="9b985-152">서브넷 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="9b985-153">게이트웨이에서 개인 IP 주소를 사용하는 경우 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="9b985-154">*PrivateIPAddress* 매개 변수를 지정하는 경우 이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="9b985-155">*PrivateIPAddress를* 지정하지 않으면 이 서브넷의 IP 주소 중 하나를 애플리케이션 게이트웨이의 프런트 엔드 IP 주소로 동적으로 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="9b985-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b985-156">CommonParameters</span></span>
<span data-ttu-id="9b985-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b985-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b985-158">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b985-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b985-159">입력</span><span class="sxs-lookup"><span data-stu-id="9b985-159">INPUTS</span></span>

### <span data-ttu-id="9b985-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b985-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b985-161">출력</span><span class="sxs-lookup"><span data-stu-id="9b985-161">OUTPUTS</span></span>

### <span data-ttu-id="9b985-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b985-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b985-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b985-163">NOTES</span></span>

## <span data-ttu-id="9b985-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b985-164">RELATED LINKS</span></span>

[<span data-ttu-id="9b985-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9b985-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9b985-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9b985-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9b985-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9b985-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9b985-168">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9b985-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9b985-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9b985-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


