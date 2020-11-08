---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4b3a3303e8ade93b5c6945dae7650f7a9d16bbff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215948"
---
# <span data-ttu-id="7788e-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7788e-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="7788e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7788e-102">SYNOPSIS</span></span>
<span data-ttu-id="7788e-103">응용 프로그램 게이트웨이에 대 한 IP 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="7788e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7788e-104">SYNTAX</span></span>

### <span data-ttu-id="7788e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7788e-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7788e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7788e-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7788e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7788e-107">DESCRIPTION</span></span>
<span data-ttu-id="7788e-108">**AzApplicationGatewayIPConfiguration** CMDLET은 IP 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="7788e-109">IP 구성에는 응용 프로그램 게이트웨이가 배포 되는 서브넷이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="7788e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7788e-110">EXAMPLES</span></span>

### <span data-ttu-id="7788e-111">예제 1: 응용 프로그램 게이트웨이에 대 한 IP 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="7788e-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="7788e-112">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="7788e-113">두 번째 명령은 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="7788e-114">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하고이를 $AppGw 변수에 저장 하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7788e-115">위의 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이의 IP 구성을 $Subnet에 저장 된 서브넷 구성으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="7788e-116">변수</span><span class="sxs-lookup"><span data-stu-id="7788e-116">PARAMETERS</span></span>

### <span data-ttu-id="7788e-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7788e-117">-ApplicationGateway</span></span>
<span data-ttu-id="7788e-118">이 cmdlet이 IP 구성을 연결 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="7788e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7788e-119">-DefaultProfile</span></span>
<span data-ttu-id="7788e-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7788e-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7788e-121">-Name</span></span>
<span data-ttu-id="7788e-122">IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="7788e-123">-서브넷</span><span class="sxs-lookup"><span data-stu-id="7788e-123">-Subnet</span></span>
<span data-ttu-id="7788e-124">서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-124">Specifies the subnet.</span></span>
<span data-ttu-id="7788e-125">이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="7788e-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7788e-126">-SubnetId</span></span>
<span data-ttu-id="7788e-127">서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="7788e-128">이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="7788e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7788e-129">CommonParameters</span></span>
<span data-ttu-id="7788e-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7788e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7788e-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7788e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7788e-132">입력</span><span class="sxs-lookup"><span data-stu-id="7788e-132">INPUTS</span></span>

### <span data-ttu-id="7788e-133">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7788e-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7788e-134">출력</span><span class="sxs-lookup"><span data-stu-id="7788e-134">OUTPUTS</span></span>

### <span data-ttu-id="7788e-135">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7788e-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7788e-136">상속자</span><span class="sxs-lookup"><span data-stu-id="7788e-136">NOTES</span></span>

## <span data-ttu-id="7788e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7788e-137">RELATED LINKS</span></span>

[<span data-ttu-id="7788e-138">추가-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7788e-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7788e-139">추가-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7788e-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7788e-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7788e-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7788e-141">새로운 AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7788e-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7788e-142">제거-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7788e-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


