---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385568"
---
# <span data-ttu-id="112d9-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="112d9-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="112d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="112d9-102">SYNOPSIS</span></span>
<span data-ttu-id="112d9-103">애플리케이션 게이트웨이에 대한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="112d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="112d9-104">SYNTAX</span></span>

### <span data-ttu-id="112d9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="112d9-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112d9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="112d9-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="112d9-107">설명</span><span class="sxs-lookup"><span data-stu-id="112d9-107">DESCRIPTION</span></span>
<span data-ttu-id="112d9-108">**New-AzApplicationGatewayFrontendIPConfig** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="112d9-109">애플리케이션 게이트웨이는 두 가지 유형의 프런트 엔드 IP 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="112d9-110">공용 IP 주소 - ILB(내부 부하 분산)를 사용하는 개인 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="112d9-111">애플리케이션 게이트웨이에는 공용 IP 주소와 개인 IP 주소가 하나씩 있습니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="112d9-112">공용 IP 주소 및 개인 IP 주소는 프런트 엔드 IP 주소로 별도로 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="112d9-113">예제</span><span class="sxs-lookup"><span data-stu-id="112d9-113">EXAMPLES</span></span>

### <span data-ttu-id="112d9-114">예제 1: 공용 IP 리소스 개체를 사용하여 프런트 엔드 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="112d9-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="112d9-115">첫 번째 명령은 공용 IP 리소스 개체를 만들고 해당 $PublicIP 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="112d9-116">두 번째 명령은 $PublicIP FrontEndIP01이라는 새 프런트 엔드 IP 구성을 만들고 $FrontEnd 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="112d9-117">예제 2: 정적 개인 IP를 프런트 엔드 IP 주소로 만들기</span><span class="sxs-lookup"><span data-stu-id="112d9-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="112d9-118">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 $VNet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="112d9-119">두 번째 명령은 첫 번째 명령에서 $VNet 사용하여 Subnet01이라는 서브넷 구성을 $Subnet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="112d9-120">세 번째 명령은 두 번째 명령의 $Subnet 및 개인 IP 주소 10.0.1.1을 사용하여 FrontEndIP02라는 프런트 엔드 IP 구성을 만든 다음 $FrontEnd 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="112d9-121">예제 3: 동적 개인 IP를 프런트 엔드 IP 주소로 만들기</span><span class="sxs-lookup"><span data-stu-id="112d9-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="112d9-122">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 $VNet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="112d9-123">두 번째 명령은 첫 번째 명령에서 $VNet 사용하여 Subnet01이라는 서브넷 구성을 $Subnet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="112d9-124">세 번째 명령은 두 번째 명령의 $Subnet 사용하여 FrontEndIP03이라는 프런트 엔드 IP 구성을 만들고 $FrontEnd 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="112d9-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="112d9-125">PARAMETERS</span></span>

### <span data-ttu-id="112d9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112d9-126">-DefaultProfile</span></span>
<span data-ttu-id="112d9-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="112d9-128">-Name</span><span class="sxs-lookup"><span data-stu-id="112d9-128">-Name</span></span>
<span data-ttu-id="112d9-129">이 cmdlet에서 만드는 프런트 엔드 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="112d9-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="112d9-130">-PrivateIPAddress</span></span>
<span data-ttu-id="112d9-131">이 cmdlet이 애플리케이션 게이트웨이의 프런트 엔드 IP 주소와 연결되는 개인 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="112d9-132">이 지정은 서브넷이 지정된 경우만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="112d9-133">이 IP는 서브넷에서 정적으로 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="112d9-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="112d9-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="112d9-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="112d9-135">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="112d9-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="112d9-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="112d9-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="112d9-137">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="112d9-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="112d9-138">-PublicIPAddress</span></span>
<span data-ttu-id="112d9-139">이 cmdlet이 애플리케이션 게이트웨이의 프런트 엔드 IP 주소와 연결되는 공용 IP 주소 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="112d9-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="112d9-140">-PublicIPAddressId</span></span>
<span data-ttu-id="112d9-141">이 cmdlet이 애플리케이션 게이트웨이의 프런트 엔드 IP와 연결되는 공용 IP 주소 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="112d9-142">-Subnet</span><span class="sxs-lookup"><span data-stu-id="112d9-142">-Subnet</span></span>
<span data-ttu-id="112d9-143">이 cmdlet이 애플리케이션 게이트웨이의 프런트 엔드 IP 주소와 연결되는 서브넷 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="112d9-144">이 매개 변수를 지정하면 게이트웨이가 개인 IP 주소를 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="112d9-145">*PrivateIPAddress* 매개 변수가 지정된 경우 이 매개 변수에 지정된 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="112d9-146">*PrivateIPAddress를* 지정하지 않으면 이 서브넷의 IP 주소 중 하나는 애플리케이션 게이트웨이의 프런트 엔드 IP 주소로 동적으로 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="112d9-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="112d9-147">-SubnetId</span></span>
<span data-ttu-id="112d9-148">이 cmdlet이 애플리케이션 게이트웨이의 프런트 엔드 IP 구성과 연결되는 서브넷 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="112d9-149">서브넷 매개 *변수를* 지정하는 경우 게이트웨이가 개인 IP 주소를 사용함을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="112d9-150">*PrivateIPAddress* 매개 변수가 지정된 경우 서브넷에서 지정한 서브넷에 *속해야 합니다.*</span><span class="sxs-lookup"><span data-stu-id="112d9-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="112d9-151">*PrivateIPAddress를* 지정하지 않으면 이 서브넷의 IP 주소 중 하나는 애플리케이션 게이트웨이의 프런트 엔드 IP 주소로 동적으로 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="112d9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112d9-152">CommonParameters</span></span>
<span data-ttu-id="112d9-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="112d9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112d9-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="112d9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112d9-155">입력</span><span class="sxs-lookup"><span data-stu-id="112d9-155">INPUTS</span></span>

### <span data-ttu-id="112d9-156">없음</span><span class="sxs-lookup"><span data-stu-id="112d9-156">None</span></span>

## <span data-ttu-id="112d9-157">출력</span><span class="sxs-lookup"><span data-stu-id="112d9-157">OUTPUTS</span></span>

### <span data-ttu-id="112d9-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="112d9-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="112d9-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="112d9-159">NOTES</span></span>

## <span data-ttu-id="112d9-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="112d9-160">RELATED LINKS</span></span>

[<span data-ttu-id="112d9-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="112d9-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="112d9-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="112d9-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="112d9-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="112d9-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="112d9-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="112d9-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


