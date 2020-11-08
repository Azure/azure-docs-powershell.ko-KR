---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 30238f9466e87ab732b1b2b6d30bba26bcd4c83a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044325"
---
# <span data-ttu-id="ebb03-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ebb03-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="ebb03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebb03-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb03-103">응용 프로그램 게이트웨이에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="ebb03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebb03-104">SYNTAX</span></span>

### <span data-ttu-id="ebb03-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ebb03-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb03-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ebb03-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebb03-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ebb03-107">DESCRIPTION</span></span>
<span data-ttu-id="ebb03-108">**Add-AzApplicationGatewayFrontendIPConfig** cmdlet은 응용 프로그램 게이트웨이에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="ebb03-109">응용 프로그램 게이트웨이는 두 가지 유형의 프런트 엔드 IP 구성을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="ebb03-110">공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="ebb03-110">Public IP addresses</span></span>
- <span data-ttu-id="ebb03-111">내부 부하 분산 (ILB)을 사용 하는 개인 IP 주소 응용 프로그램 게이트웨이에는 공용 IP와 개인 IP가 각각 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="ebb03-112">공용 IP 주소와 개인 IP 주소를 별도의 프런트 엔드 IPs로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="ebb03-113">예제의</span><span class="sxs-lookup"><span data-stu-id="ebb03-113">EXAMPLES</span></span>

### <span data-ttu-id="ebb03-114">예제 1: 공용 IP를 프런트 엔드 IP 주소로 추가</span><span class="sxs-lookup"><span data-stu-id="ebb03-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="ebb03-115">첫 번째 명령은 공용 IP 주소 개체를 만들고이를 $PublicIp 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="ebb03-116">두 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ebb03-117">세 번째 명령은 FrontEndIp01 이라는 프런트 엔드 IP 구성을 $PublicIp에 저장 된 주소를 사용 하 여 $AppGw의 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="ebb03-118">예제 2: 고정 개인 IP를 프런트 엔드 IP 주소로 추가</span><span class="sxs-lookup"><span data-stu-id="ebb03-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="ebb03-119">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="ebb03-120">두 번째 명령은 첫 번째 명령의 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ebb03-121">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ebb03-122">네 번째 명령은 두번째 명령 및 개인 IP 주소 10.0.1.1에서 $Subnet를 사용 하 여 FrontendIP02 라는 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="ebb03-123">예제 3: 동적 개인 IP를 프런트 엔드 IP 주소로 추가</span><span class="sxs-lookup"><span data-stu-id="ebb03-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="ebb03-124">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="ebb03-125">두 번째 명령은 첫 번째 명령의 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ebb03-126">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ebb03-127">네 번째 명령은 $Subnet를 사용 하 여 FrontendIP02 라는 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="ebb03-128">변수</span><span class="sxs-lookup"><span data-stu-id="ebb03-128">PARAMETERS</span></span>

### <span data-ttu-id="ebb03-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebb03-129">-ApplicationGateway</span></span>
<span data-ttu-id="ebb03-130">이 cmdlet이 프런트 엔드 IP 구성을 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb03-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb03-131">-DefaultProfile</span></span>
<span data-ttu-id="ebb03-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebb03-133">-이름</span><span class="sxs-lookup"><span data-stu-id="ebb03-133">-Name</span></span>
<span data-ttu-id="ebb03-134">추가할 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="ebb03-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="ebb03-135">-PrivateIPAddress</span></span>
<span data-ttu-id="ebb03-136">응용 프로그램 게이트웨이에 대 한 프런트 엔드 IP로 추가할 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="ebb03-137">지정 된 경우이 IP가 서브넷에서 정적으로 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="ebb03-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="ebb03-138">-PublicIPAddress</span></span>
<span data-ttu-id="ebb03-139">이 cmdlet이 응용 프로그램 게이트웨이에 대 한 프런트 엔드 IP 주소로 추가 하는 공용 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-139">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb03-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="ebb03-140">-PublicIPAddressId</span></span>
<span data-ttu-id="ebb03-141">이 cmdlet이 응용 프로그램 게이트웨이에 대 한 프런트 엔드 IP 주소로 추가 하는 공용 IP 주소의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-141">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb03-142">-서브넷</span><span class="sxs-lookup"><span data-stu-id="ebb03-142">-Subnet</span></span>
<span data-ttu-id="ebb03-143">이 cmdlet이 프런트 엔드 IP 구성으로 추가 하는 서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-143">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="ebb03-144">이 매개 변수를 지정 하는 경우 응용 프로그램 게이트웨이가 개인 IP 기반 구성을 지원함을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-144">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="ebb03-145">*PrivateIPAddress* 매개 변수를 지정한 경우이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-145">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="ebb03-146">*PrivateIPAddress* 가 지정 되지 않은 경우이 서브넷의 ip 주소 중 하나가 동적으로 응용 프로그램 게이트웨이의 프런트 엔드 IP 주소로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb03-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ebb03-147">-SubnetId</span></span>
<span data-ttu-id="ebb03-148">이 cmdlet이 프런트 엔드 IP 구성으로 추가 하는 서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-148">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="ebb03-149">서브넷 전달은 개인 IP를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-149">Passing subnet implies private IP.</span></span>
<span data-ttu-id="ebb03-150">*PrivateIPAddress* 매개 변수를 지정한 경우이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-150">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="ebb03-151">그렇지 않으면이 서브넷의 IP 중 하나가 동적으로 응용 프로그램 게이트웨이의 프런트 엔드 IP로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-151">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb03-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb03-152">CommonParameters</span></span>
<span data-ttu-id="ebb03-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb03-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb03-154">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebb03-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb03-155">입력</span><span class="sxs-lookup"><span data-stu-id="ebb03-155">INPUTS</span></span>

### <span data-ttu-id="ebb03-156">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebb03-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ebb03-157">출력</span><span class="sxs-lookup"><span data-stu-id="ebb03-157">OUTPUTS</span></span>

### <span data-ttu-id="ebb03-158">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebb03-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ebb03-159">상속자</span><span class="sxs-lookup"><span data-stu-id="ebb03-159">NOTES</span></span>

## <span data-ttu-id="ebb03-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebb03-160">RELATED LINKS</span></span>

[<span data-ttu-id="ebb03-161">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ebb03-161">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ebb03-162">새로운 AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ebb03-162">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ebb03-163">제거-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ebb03-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ebb03-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ebb03-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


