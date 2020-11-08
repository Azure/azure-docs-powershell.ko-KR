---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034376"
---
# <span data-ttu-id="8e5c2-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e5c2-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="8e5c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5c2-103">응용 프로그램 게이트웨이에 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="8e5c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e5c2-104">SYNTAX</span></span>

### <span data-ttu-id="8e5c2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e5c2-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e5c2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8e5c2-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e5c2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8e5c2-107">DESCRIPTION</span></span>
<span data-ttu-id="8e5c2-108">**Add-AzApplicationGatewayIPConfiguration** cmdlet은 응용 프로그램 게이트웨이에 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="8e5c2-109">IP 구성에는 응용 프로그램 게이트웨이가 배포 된 서브넷이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="8e5c2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8e5c2-110">EXAMPLES</span></span>

### <span data-ttu-id="8e5c2-111">예제 1: 응용 프로그램 게이트웨이에 가상 네트워크 구성 추가</span><span class="sxs-lookup"><span data-stu-id="8e5c2-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="8e5c2-112">첫 번째 명령은 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="8e5c2-113">두 번째 명령은 이전에 만든 가상 네트워크를 사용 하 여 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="8e5c2-114">세 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8e5c2-115">네 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="8e5c2-116">변수</span><span class="sxs-lookup"><span data-stu-id="8e5c2-116">PARAMETERS</span></span>

### <span data-ttu-id="8e5c2-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e5c2-117">-ApplicationGateway</span></span>
<span data-ttu-id="8e5c2-118">이 cmdlet이 IP 구성을 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="8e5c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5c2-119">-DefaultProfile</span></span>
<span data-ttu-id="8e5c2-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e5c2-121">-이름</span><span class="sxs-lookup"><span data-stu-id="8e5c2-121">-Name</span></span>
<span data-ttu-id="8e5c2-122">추가할 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="8e5c2-123">-서브넷</span><span class="sxs-lookup"><span data-stu-id="8e5c2-123">-Subnet</span></span>
<span data-ttu-id="8e5c2-124">서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-124">Specifies a subnet.</span></span>
<span data-ttu-id="8e5c2-125">이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="8e5c2-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8e5c2-126">-SubnetId</span></span>
<span data-ttu-id="8e5c2-127">서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="8e5c2-128">이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="8e5c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5c2-129">CommonParameters</span></span>
<span data-ttu-id="8e5c2-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5c2-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e5c2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5c2-132">입력</span><span class="sxs-lookup"><span data-stu-id="8e5c2-132">INPUTS</span></span>

### <span data-ttu-id="8e5c2-133">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e5c2-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e5c2-134">출력</span><span class="sxs-lookup"><span data-stu-id="8e5c2-134">OUTPUTS</span></span>

### <span data-ttu-id="8e5c2-135">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e5c2-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e5c2-136">상속자</span><span class="sxs-lookup"><span data-stu-id="8e5c2-136">NOTES</span></span>

## <span data-ttu-id="8e5c2-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e5c2-137">RELATED LINKS</span></span>

[<span data-ttu-id="8e5c2-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e5c2-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8e5c2-139">새로운 AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e5c2-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8e5c2-140">제거-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e5c2-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8e5c2-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e5c2-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


