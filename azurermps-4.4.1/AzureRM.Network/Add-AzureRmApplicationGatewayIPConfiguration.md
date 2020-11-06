---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 98e2249c3577d49a140d31b4287507e0e46185f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534003"
---
# <span data-ttu-id="50a15-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="50a15-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="50a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50a15-102">SYNOPSIS</span></span>
<span data-ttu-id="50a15-103">응용 프로그램 게이트웨이에 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50a15-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50a15-104">SYNTAX</span></span>

### <span data-ttu-id="50a15-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="50a15-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50a15-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="50a15-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50a15-107">설명은</span><span class="sxs-lookup"><span data-stu-id="50a15-107">DESCRIPTION</span></span>
<span data-ttu-id="50a15-108">**Add-AzureRmApplicationGatewayIPConfiguration** cmdlet은 응용 프로그램 게이트웨이에 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="50a15-109">IP 구성에는 응용 프로그램 게이트웨이가 배포 된 서브넷이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="50a15-110">예제의</span><span class="sxs-lookup"><span data-stu-id="50a15-110">EXAMPLES</span></span>

### <span data-ttu-id="50a15-111">예제 1: 응용 프로그램 게이트웨이에 가상 네트워크 구성 추가</span><span class="sxs-lookup"><span data-stu-id="50a15-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="50a15-112">첫 번째 명령은 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="50a15-113">두 번째 명령은 이전에 만든 가상 네트워크를 사용 하 여 서브넷을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="50a15-114">세 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="50a15-115">Fouth 명령은 IP 구성을 $AppGw에 저장 된 응용 프로그램 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="50a15-116">변수</span><span class="sxs-lookup"><span data-stu-id="50a15-116">PARAMETERS</span></span>

### <span data-ttu-id="50a15-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50a15-117">-ApplicationGateway</span></span>
<span data-ttu-id="50a15-118">이 cmdlet이 IP 구성을 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="50a15-119">-이름</span><span class="sxs-lookup"><span data-stu-id="50a15-119">-Name</span></span>
<span data-ttu-id="50a15-120">추가할 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-120">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="50a15-121">-서브넷</span><span class="sxs-lookup"><span data-stu-id="50a15-121">-Subnet</span></span>
<span data-ttu-id="50a15-122">서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-122">Specifies a subnet.</span></span>
<span data-ttu-id="50a15-123">이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-123">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="50a15-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="50a15-124">-SubnetId</span></span>
<span data-ttu-id="50a15-125">서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-125">Specifies a subnet ID.</span></span>
<span data-ttu-id="50a15-126">이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-126">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="50a15-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a15-127">-DefaultProfile</span></span>
<span data-ttu-id="50a15-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50a15-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a15-129">CommonParameters</span></span>
<span data-ttu-id="50a15-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a15-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a15-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50a15-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a15-132">입력</span><span class="sxs-lookup"><span data-stu-id="50a15-132">INPUTS</span></span>

### <span data-ttu-id="50a15-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="50a15-133">System.String</span></span>

## <span data-ttu-id="50a15-134">출력</span><span class="sxs-lookup"><span data-stu-id="50a15-134">OUTPUTS</span></span>

### <span data-ttu-id="50a15-135">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50a15-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50a15-136">상속자</span><span class="sxs-lookup"><span data-stu-id="50a15-136">NOTES</span></span>

## <span data-ttu-id="50a15-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50a15-137">RELATED LINKS</span></span>

[<span data-ttu-id="50a15-138">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="50a15-138">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="50a15-139">새로운 AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="50a15-139">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="50a15-140">제거-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="50a15-140">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="50a15-141">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="50a15-141">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


