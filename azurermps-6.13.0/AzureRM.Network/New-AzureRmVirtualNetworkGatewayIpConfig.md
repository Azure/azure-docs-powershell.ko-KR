---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b00c3950140c0ebf158170a8ddd2396e62c2b2c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703146"
---
# <span data-ttu-id="e2d71-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2d71-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="e2d71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2d71-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d71-103">가상 네트워크 게이트웨이에 대 한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2d71-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2d71-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2d71-104">SYNTAX</span></span>

### <span data-ttu-id="e2d71-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2d71-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2d71-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e2d71-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2d71-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e2d71-107">DESCRIPTION</span></span>
<span data-ttu-id="e2d71-108">**AzureRmVirtualNetworkGatewayIpConfig** Cmdlet은 서브넷 ID 기반 (이전에 만든) 공용 IP 주소를 사용 하 여 가상 네트워크 게이트웨이에 할당 된 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2d71-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="e2d71-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e2d71-109">EXAMPLES</span></span>

### <span data-ttu-id="e2d71-110">1: 가상 네트워크 게이트웨이에 대 한 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="e2d71-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="e2d71-111">공용 IP 주소를 사용 하 여 가상 네트워크 게이트웨이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d71-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="e2d71-112">변수 $myGWsubnet는 가상 네트워크 게이트웨이를 만들려는 가상 네트워크 내의 " **AzureRmVirtualNetworkSubnetConfig** cmdlet을 사용 하 여 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e2d71-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="e2d71-113">**AzureRmPublicIpAddress** cmdlet을 사용 하 여 변수 $myGWpip를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e2d71-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="e2d71-114">변수</span><span class="sxs-lookup"><span data-stu-id="e2d71-114">PARAMETERS</span></span>

### <span data-ttu-id="e2d71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d71-115">-DefaultProfile</span></span>
<span data-ttu-id="e2d71-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d71-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2d71-117">-이름</span><span class="sxs-lookup"><span data-stu-id="e2d71-117">-Name</span></span>
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

### <span data-ttu-id="e2d71-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2d71-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="e2d71-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2d71-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="e2d71-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="e2d71-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="e2d71-121">-서브넷</span><span class="sxs-lookup"><span data-stu-id="e2d71-121">-Subnet</span></span>
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

### <span data-ttu-id="e2d71-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e2d71-122">-SubnetId</span></span>
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

### <span data-ttu-id="e2d71-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d71-123">CommonParameters</span></span>
<span data-ttu-id="e2d71-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d71-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d71-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d71-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d71-126">입력</span><span class="sxs-lookup"><span data-stu-id="e2d71-126">INPUTS</span></span>

### <span data-ttu-id="e2d71-127">않아야</span><span class="sxs-lookup"><span data-stu-id="e2d71-127">None</span></span>

## <span data-ttu-id="e2d71-128">출력</span><span class="sxs-lookup"><span data-stu-id="e2d71-128">OUTPUTS</span></span>

### <span data-ttu-id="e2d71-129">PSVirtualNetworkGatewayIpConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e2d71-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="e2d71-130">상속자</span><span class="sxs-lookup"><span data-stu-id="e2d71-130">NOTES</span></span>

## <span data-ttu-id="e2d71-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2d71-131">RELATED LINKS</span></span>
