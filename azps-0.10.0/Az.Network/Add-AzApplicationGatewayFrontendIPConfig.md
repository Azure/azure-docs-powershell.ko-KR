---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 4b0fd2fd55b255a9734a0c6b0c325f7ac113b4e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875703"
---
# <span data-ttu-id="32cad-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="32cad-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="32cad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32cad-102">SYNOPSIS</span></span>
<span data-ttu-id="32cad-103">응용 프로그램 게이트웨이에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="32cad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32cad-104">SYNTAX</span></span>

### <span data-ttu-id="32cad-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="32cad-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32cad-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="32cad-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32cad-107">설명은</span><span class="sxs-lookup"><span data-stu-id="32cad-107">DESCRIPTION</span></span>
<span data-ttu-id="32cad-108">**Add-AzApplicationGatewayFrontendIPConfig** cmdlet은 응용 프로그램 게이트웨이에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="32cad-109">응용 프로그램 게이트웨이는 두 가지 유형의 프런트 엔드 IP 구성을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-109">An application gateway supports two types of front-end IP configurations:</span></span> 

- <span data-ttu-id="32cad-110">공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="32cad-110">Public IP addresses</span></span>
- <span data-ttu-id="32cad-111">내부 부하 분산을 사용 하는 개인 IP 주소 (ILB)</span><span class="sxs-lookup"><span data-stu-id="32cad-111">Private IP addresses using internal load-balancing (ILB)</span></span>

<span data-ttu-id="32cad-112">응용 프로그램 게이트웨이에는 공용 IP와 개인 IP가 각각 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-112">An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="32cad-113">공용 IP 주소와 개인 IP 주소를 별도의 프런트 엔드 IPs로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-113">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="32cad-114">예제의</span><span class="sxs-lookup"><span data-stu-id="32cad-114">EXAMPLES</span></span>

### <span data-ttu-id="32cad-115">예제 1: 공용 IP를 프런트 엔드 IP 주소로 추가</span><span class="sxs-lookup"><span data-stu-id="32cad-115">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="32cad-116">첫 번째 명령은 공용 IP 주소 개체를 만들고이를 $PublicIp 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="32cad-117">두 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="32cad-118">세 번째 명령은 FrontEndIp01 이라는 프런트 엔드 IP 구성을 $PublicIp에 저장 된 주소를 사용 하 여 $AppGw의 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-118">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="32cad-119">예제 2: 고정 개인 IP를 프런트 엔드 IP 주소로 추가</span><span class="sxs-lookup"><span data-stu-id="32cad-119">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="32cad-120">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="32cad-121">두 번째 명령은 첫 번째 명령의 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="32cad-122">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="32cad-123">네 번째 명령은 두번째 명령 및 개인 IP 주소 10.0.1.1에서 $Subnet를 사용 하 여 FrontendIP02 라는 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="32cad-124">예제 3: 동적 개인 IP를 프런트 엔드 IP 주소로 추가</span><span class="sxs-lookup"><span data-stu-id="32cad-124">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="32cad-125">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="32cad-126">두 번째 명령은 첫 번째 명령의 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="32cad-127">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="32cad-128">네 번째 명령은 $Subnet를 사용 하 여 FrontendIP02 라는 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="32cad-129">변수</span><span class="sxs-lookup"><span data-stu-id="32cad-129">PARAMETERS</span></span>

### <span data-ttu-id="32cad-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="32cad-130">-ApplicationGateway</span></span>
<span data-ttu-id="32cad-131">이 cmdlet이 프런트 엔드 IP 구성을 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-131">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="32cad-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32cad-132">-DefaultProfile</span></span>
<span data-ttu-id="32cad-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32cad-134">-이름</span><span class="sxs-lookup"><span data-stu-id="32cad-134">-Name</span></span>
<span data-ttu-id="32cad-135">추가할 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="32cad-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="32cad-136">-PrivateIPAddress</span></span>
<span data-ttu-id="32cad-137">응용 프로그램 게이트웨이에 대 한 프런트 엔드 IP로 추가할 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-137">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="32cad-138">지정 된 경우이 IP가 서브넷에서 정적으로 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="32cad-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="32cad-139">-PublicIPAddress</span></span>
<span data-ttu-id="32cad-140">이 cmdlet이 응용 프로그램 게이트웨이에 대 한 프런트 엔드 IP 주소로 추가 하는 공용 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-140">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="32cad-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="32cad-141">-PublicIPAddressId</span></span>
<span data-ttu-id="32cad-142">이 cmdlet이 응용 프로그램 게이트웨이에 대 한 프런트 엔드 IP 주소로 추가 하는 공용 IP 주소의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-142">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="32cad-143">-서브넷</span><span class="sxs-lookup"><span data-stu-id="32cad-143">-Subnet</span></span>
<span data-ttu-id="32cad-144">이 cmdlet이 프런트 엔드 IP 구성으로 추가 하는 서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-144">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="32cad-145">이 매개 변수를 지정 하는 경우 응용 프로그램 게이트웨이가 개인 IP 기반 구성을 지원함을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-145">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="32cad-146">*PrivateIPAddress* 매개 변수를 지정한 경우이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-146">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="32cad-147">*PrivateIPAddress* 가 지정 되지 않은 경우이 서브넷의 ip 주소 중 하나가 동적으로 응용 프로그램 게이트웨이의 프런트 엔드 IP 주소로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="32cad-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="32cad-148">-SubnetId</span></span>
<span data-ttu-id="32cad-149">이 cmdlet이 프런트 엔드 IP 구성으로 추가 하는 서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-149">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="32cad-150">서브넷 전달은 개인 IP를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-150">Passing subnet implies private IP.</span></span>
<span data-ttu-id="32cad-151">*PrivateIPAddresss* 매개 변수를 지정한 경우이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-151">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="32cad-152">그렇지 않으면이 서브넷의 IP 중 하나가 동적으로 응용 프로그램 게이트웨이의 프런트 엔드 IP로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-152">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="32cad-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32cad-153">CommonParameters</span></span>
<span data-ttu-id="32cad-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cad-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32cad-155">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32cad-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32cad-156">입력</span><span class="sxs-lookup"><span data-stu-id="32cad-156">INPUTS</span></span>

### <span data-ttu-id="32cad-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="32cad-157">System.String</span></span>

## <span data-ttu-id="32cad-158">출력</span><span class="sxs-lookup"><span data-stu-id="32cad-158">OUTPUTS</span></span>

### <span data-ttu-id="32cad-159">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="32cad-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="32cad-160">상속자</span><span class="sxs-lookup"><span data-stu-id="32cad-160">NOTES</span></span>

## <span data-ttu-id="32cad-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32cad-161">RELATED LINKS</span></span>

[<span data-ttu-id="32cad-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="32cad-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="32cad-163">새로운 AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="32cad-163">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="32cad-164">제거-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="32cad-164">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="32cad-165">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="32cad-165">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


