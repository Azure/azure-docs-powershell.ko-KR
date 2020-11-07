---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: d3a309d99dff493e2440618d87c20b1a543e2ed9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880930"
---
# <span data-ttu-id="ea96e-101">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea96e-101">Set-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="ea96e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea96e-102">SYNOPSIS</span></span>
<span data-ttu-id="ea96e-103">응용 프로그램 게이트웨이에 대 한 IP 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-103">Modifies an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea96e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea96e-104">SYNTAX</span></span>

### <span data-ttu-id="ea96e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea96e-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea96e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ea96e-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea96e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ea96e-107">DESCRIPTION</span></span>
<span data-ttu-id="ea96e-108">**AzureRmApplicationGatewayIPConfiguration** CMDLET은 IP 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-108">The **Set-AzureRmApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="ea96e-109">IP 구성에는 응용 프로그램 게이트웨이가 배포 되는 서브넷이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="ea96e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ea96e-110">EXAMPLES</span></span>

### <span data-ttu-id="ea96e-111">예제 1: IP 구성의 목표 상태 설정</span><span class="sxs-lookup"><span data-stu-id="ea96e-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzureRmVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="ea96e-112">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>

<span data-ttu-id="ea96e-113">두 번째 명령은 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="ea96e-114">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하고이를 $AppGw 변수에 저장 하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="ea96e-115">위의 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이의 IP 구성을 $Subnet에 저장 된 서브넷 구성으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="ea96e-116">변수</span><span class="sxs-lookup"><span data-stu-id="ea96e-116">PARAMETERS</span></span>

### <span data-ttu-id="ea96e-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ea96e-117">-ApplicationGateway</span></span>
<span data-ttu-id="ea96e-118">이 cmdlet이 IP 구성을 연결 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="ea96e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea96e-119">-DefaultProfile</span></span>
<span data-ttu-id="ea96e-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea96e-121">-이름</span><span class="sxs-lookup"><span data-stu-id="ea96e-121">-Name</span></span>
<span data-ttu-id="ea96e-122">IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="ea96e-123">-서브넷</span><span class="sxs-lookup"><span data-stu-id="ea96e-123">-Subnet</span></span>
<span data-ttu-id="ea96e-124">서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-124">Specifies the subnet.</span></span>
<span data-ttu-id="ea96e-125">이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="ea96e-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ea96e-126">-SubnetId</span></span>
<span data-ttu-id="ea96e-127">서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="ea96e-128">이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="ea96e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea96e-129">CommonParameters</span></span>
<span data-ttu-id="ea96e-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea96e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea96e-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea96e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea96e-132">입력</span><span class="sxs-lookup"><span data-stu-id="ea96e-132">INPUTS</span></span>

### <span data-ttu-id="ea96e-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea96e-133">System.String</span></span>

## <span data-ttu-id="ea96e-134">출력</span><span class="sxs-lookup"><span data-stu-id="ea96e-134">OUTPUTS</span></span>

### <span data-ttu-id="ea96e-135">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ea96e-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ea96e-136">상속자</span><span class="sxs-lookup"><span data-stu-id="ea96e-136">NOTES</span></span>

## <span data-ttu-id="ea96e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea96e-137">RELATED LINKS</span></span>

[<span data-ttu-id="ea96e-138">추가-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea96e-138">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ea96e-139">추가-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea96e-139">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ea96e-140">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea96e-140">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ea96e-141">새로운 AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea96e-141">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ea96e-142">제거-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea96e-142">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)


