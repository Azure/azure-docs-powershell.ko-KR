---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213026"
---
# <span data-ttu-id="10955-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10955-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="10955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10955-102">SYNOPSIS</span></span>
<span data-ttu-id="10955-103">응용 프로그램 게이트웨이에 대 한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10955-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="10955-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10955-104">SYNTAX</span></span>

### <span data-ttu-id="10955-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="10955-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10955-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="10955-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10955-107">설명은</span><span class="sxs-lookup"><span data-stu-id="10955-107">DESCRIPTION</span></span>
<span data-ttu-id="10955-108">**AzApplicationGatewayIPConfiguration** cmdlet은 응용 프로그램 게이트웨이에 대 한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10955-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="10955-109">IP 구성에는 응용 프로그램 게이트웨이가 배포 되는 서브넷이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10955-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="10955-110">예제의</span><span class="sxs-lookup"><span data-stu-id="10955-110">EXAMPLES</span></span>

### <span data-ttu-id="10955-111">예제 1: 응용 프로그램 게이트웨이에 대 한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10955-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="10955-112">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10955-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="10955-113">두 번째 명령은 이전 명령의 가상 네트워크가 속한 서브넷에 대 한 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="10955-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="10955-114">세 번째 명령은 $Subnet를 사용 하 여 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10955-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="10955-115">변수</span><span class="sxs-lookup"><span data-stu-id="10955-115">PARAMETERS</span></span>

### <span data-ttu-id="10955-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10955-116">-DefaultProfile</span></span>
<span data-ttu-id="10955-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10955-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10955-118">-이름</span><span class="sxs-lookup"><span data-stu-id="10955-118">-Name</span></span>
<span data-ttu-id="10955-119">만들려는 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10955-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="10955-120">-서브넷</span><span class="sxs-lookup"><span data-stu-id="10955-120">-Subnet</span></span>
<span data-ttu-id="10955-121">서브넷 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10955-121">Specifies the subnet object.</span></span>
<span data-ttu-id="10955-122">이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="10955-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="10955-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="10955-123">-SubnetId</span></span>
<span data-ttu-id="10955-124">서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10955-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="10955-125">이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="10955-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="10955-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10955-126">CommonParameters</span></span>
<span data-ttu-id="10955-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10955-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10955-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10955-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10955-129">입력</span><span class="sxs-lookup"><span data-stu-id="10955-129">INPUTS</span></span>

### <span data-ttu-id="10955-130">않아야</span><span class="sxs-lookup"><span data-stu-id="10955-130">None</span></span>

## <span data-ttu-id="10955-131">출력</span><span class="sxs-lookup"><span data-stu-id="10955-131">OUTPUTS</span></span>

### <span data-ttu-id="10955-132">Microsoft. \*. m i m. 모델. m m m m i m a.</span><span class="sxs-lookup"><span data-stu-id="10955-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="10955-133">상속자</span><span class="sxs-lookup"><span data-stu-id="10955-133">NOTES</span></span>

## <span data-ttu-id="10955-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10955-134">RELATED LINKS</span></span>

[<span data-ttu-id="10955-135">추가-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10955-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="10955-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10955-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="10955-137">제거-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10955-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="10955-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10955-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


