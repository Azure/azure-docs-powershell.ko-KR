---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218114"
---
# <span data-ttu-id="9e010-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e010-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="9e010-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e010-102">SYNOPSIS</span></span>
<span data-ttu-id="9e010-103">가상 네트워크 게이트웨이에 대 한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e010-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="9e010-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e010-104">SYNTAX</span></span>

### <span data-ttu-id="9e010-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e010-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e010-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9e010-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e010-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9e010-107">DESCRIPTION</span></span>
<span data-ttu-id="9e010-108">**AzVirtualNetworkGatewayIpConfig** Cmdlet은 서브넷 ID 기반 (이전에 만든) 공용 IP 주소를 사용 하 여 가상 네트워크 게이트웨이에 할당 된 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e010-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="9e010-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9e010-109">EXAMPLES</span></span>

### <span data-ttu-id="9e010-110">1: 가상 네트워크 게이트웨이에 대 한 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="9e010-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="9e010-111">공용 IP 주소를 사용 하 여 가상 네트워크 게이트웨이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e010-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="9e010-112">변수 $myGWsubnet는 가상 네트워크 게이트웨이를 만들려는 가상 네트워크 내의 " **AzVirtualNetworkSubnetConfig** cmdlet을 사용 하 여 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e010-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="9e010-113">**AzPublicIpAddress** cmdlet을 사용 하 여 변수 $myGWpip를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e010-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="9e010-114">변수</span><span class="sxs-lookup"><span data-stu-id="9e010-114">PARAMETERS</span></span>

### <span data-ttu-id="9e010-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e010-115">-DefaultProfile</span></span>
<span data-ttu-id="9e010-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e010-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e010-117">-이름</span><span class="sxs-lookup"><span data-stu-id="9e010-117">-Name</span></span>
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

### <span data-ttu-id="9e010-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e010-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="9e010-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e010-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="9e010-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="9e010-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="9e010-121">-서브넷</span><span class="sxs-lookup"><span data-stu-id="9e010-121">-Subnet</span></span>
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

### <span data-ttu-id="9e010-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9e010-122">-SubnetId</span></span>
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

### <span data-ttu-id="9e010-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e010-123">CommonParameters</span></span>
<span data-ttu-id="9e010-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e010-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e010-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e010-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e010-126">입력</span><span class="sxs-lookup"><span data-stu-id="9e010-126">INPUTS</span></span>

### <span data-ttu-id="9e010-127">않아야</span><span class="sxs-lookup"><span data-stu-id="9e010-127">None</span></span>

## <span data-ttu-id="9e010-128">출력</span><span class="sxs-lookup"><span data-stu-id="9e010-128">OUTPUTS</span></span>

### <span data-ttu-id="9e010-129">PSVirtualNetworkGatewayIpConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9e010-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="9e010-130">상속자</span><span class="sxs-lookup"><span data-stu-id="9e010-130">NOTES</span></span>

## <span data-ttu-id="9e010-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e010-131">RELATED LINKS</span></span>

[<span data-ttu-id="9e010-132">추가-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e010-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="9e010-133">제거-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e010-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
