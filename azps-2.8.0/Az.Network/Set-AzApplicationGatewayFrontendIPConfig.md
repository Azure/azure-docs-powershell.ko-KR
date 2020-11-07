---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 128621265766f921a2c7b052f4fe276c8f67e03f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871129"
---
# <span data-ttu-id="a3825-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a3825-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="a3825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3825-102">SYNOPSIS</span></span>
<span data-ttu-id="a3825-103">프런트 엔드 IP 주소 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="a3825-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3825-104">SYNTAX</span></span>

### <span data-ttu-id="a3825-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a3825-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3825-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a3825-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3825-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a3825-107">DESCRIPTION</span></span>
<span data-ttu-id="a3825-108">**Set-AzApplicationGatewayFrontendIPConfig** cmdlet은 프런트 엔드 IP 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="a3825-109">응용 프로그램 게이트웨이는 프런트 엔드 IP 주소를 두 가지 유형으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="a3825-110">공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="a3825-110">Public IP addresses</span></span>
- <span data-ttu-id="a3825-111">구성이 내부 부하 분산을 사용 하는 개인 IP 주소 (ILB) 응용 프로그램 게이트웨이에는 공용 IP 주소와 개인 IP 주소가 최대 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="a3825-112">공용 IP 주소와 개인 IP 주소는 프런트 엔드 IP 주소와 별도로 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="a3825-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a3825-113">EXAMPLES</span></span>

### <span data-ttu-id="a3825-114">예제 1: 공용 IP를 응용 프로그램 게이트웨이의 프런트 엔드 IP로 설정</span><span class="sxs-lookup"><span data-stu-id="a3825-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="a3825-115">첫 번째 명령은 공용 IP 주소 개체를 만들고이를 $PublicIp 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="a3825-116">두 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a3825-117">세 번째 명령은 $PublicIp에 저장 된 주소를 사용 하 여 $AppGw의 게이트웨이에 대 한 FrontEndIp01 라는 프런트 엔드 IP 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="a3825-118">예제 2: 정적 개인 IP를 응용 프로그램 게이트웨이의 프런트 엔드 IP로 설정</span><span class="sxs-lookup"><span data-stu-id="a3825-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="a3825-119">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="a3825-120">두 번째 명령은 첫 번째 명령의 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="a3825-121">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a3825-122">네 번째 명령은 두번째 명령 및 개인 IP 주소 10.0.1.1에서 $Subnet를 사용 하 여 FrontendIP02 라는 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="a3825-123">예제 3: 동적 개인 IP를 응용 프로그램 게이트웨이의 프런트 엔드 IP로 설정</span><span class="sxs-lookup"><span data-stu-id="a3825-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="a3825-124">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="a3825-125">두 번째 명령은 첫 번째 명령의 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="a3825-126">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a3825-127">네 번째 명령은 $Subnet를 사용 하 여 FrontendIP02 라는 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="a3825-128">변수</span><span class="sxs-lookup"><span data-stu-id="a3825-128">PARAMETERS</span></span>

### <span data-ttu-id="a3825-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3825-129">-ApplicationGateway</span></span>
<span data-ttu-id="a3825-130">프런트 엔드 IP 구성을 수정할 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="a3825-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3825-131">-DefaultProfile</span></span>
<span data-ttu-id="a3825-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3825-133">-이름</span><span class="sxs-lookup"><span data-stu-id="a3825-133">-Name</span></span>
<span data-ttu-id="a3825-134">이 cmdlet이 수정 하는 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a3825-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="a3825-135">-PrivateIPAddress</span></span>
<span data-ttu-id="a3825-136">개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-136">Specifies the private IP address.</span></span>
<span data-ttu-id="a3825-137">지정 된 경우이 IP가 서브넷에서 정적으로 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="a3825-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="a3825-138">-PublicIPAddress</span></span>
<span data-ttu-id="a3825-139">공용 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-139">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="a3825-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="a3825-140">-PublicIPAddressId</span></span>
<span data-ttu-id="a3825-141">공용 IP 주소의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-141">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="a3825-142">-서브넷</span><span class="sxs-lookup"><span data-stu-id="a3825-142">-Subnet</span></span>
<span data-ttu-id="a3825-143">응용 프로그램 게이트웨이에서 사용 하는 서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-143">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="a3825-144">게이트웨이에서 개인 IP 주소를 사용 하는 경우이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-144">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="a3825-145">*PrivateIPAddress* address가 지정 된 경우이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-145">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="a3825-146">*PrivateIPAddress* 가 지정 되지 않은 경우이 서브넷의 ip 주소 중 하나가 동적으로 응용 프로그램 게이트웨이의 프런트 엔드 IP 주소로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a3825-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a3825-147">-SubnetId</span></span>
<span data-ttu-id="a3825-148">서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-148">Specifies the subnet ID.</span></span>
<span data-ttu-id="a3825-149">게이트웨이에서 개인 IP 주소를 사용 하는 경우이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-149">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="a3825-150">*PrivateIPAddress* 매개 변수를 지정한 경우이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-150">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="a3825-151">*PrivateIPAddress* 가 지정 되지 않은 경우이 서브넷의 ip 주소 중 하나가 동적으로 응용 프로그램 게이트웨이의 프런트 엔드 IP 주소로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a3825-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3825-152">CommonParameters</span></span>
<span data-ttu-id="a3825-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3825-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3825-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3825-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3825-155">입력</span><span class="sxs-lookup"><span data-stu-id="a3825-155">INPUTS</span></span>

### <span data-ttu-id="a3825-156">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3825-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3825-157">출력</span><span class="sxs-lookup"><span data-stu-id="a3825-157">OUTPUTS</span></span>

### <span data-ttu-id="a3825-158">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3825-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3825-159">상속자</span><span class="sxs-lookup"><span data-stu-id="a3825-159">NOTES</span></span>

## <span data-ttu-id="a3825-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3825-160">RELATED LINKS</span></span>

[<span data-ttu-id="a3825-161">추가-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a3825-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a3825-162">추가-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a3825-162">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a3825-163">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a3825-163">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a3825-164">새로운 AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a3825-164">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a3825-165">제거-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a3825-165">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


