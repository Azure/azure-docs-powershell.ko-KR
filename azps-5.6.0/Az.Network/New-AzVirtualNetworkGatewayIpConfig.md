---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: cfbfd8df28cf4f0d9c11e654694172b86a549141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964139"
---
# <span data-ttu-id="df9c2-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="df9c2-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="df9c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df9c2-102">SYNOPSIS</span></span>
<span data-ttu-id="df9c2-103">Virtual Network Gateway에 대한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df9c2-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="df9c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="df9c2-104">SYNTAX</span></span>

### <span data-ttu-id="df9c2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="df9c2-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df9c2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="df9c2-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df9c2-107">설명</span><span class="sxs-lookup"><span data-stu-id="df9c2-107">DESCRIPTION</span></span>
<span data-ttu-id="df9c2-108">**New-AzVirtualNetworkGatewayIpConfig** cmdlet은 서브넷 ID를 기반으로 (이전에 만든) 공용 IP 주소를 통해 Virtual Network Gateway에 할당된 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df9c2-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="df9c2-109">예제</span><span class="sxs-lookup"><span data-stu-id="df9c2-109">EXAMPLES</span></span>

### <span data-ttu-id="df9c2-110">1: 가상 네트워크 게이트웨이에 대한 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="df9c2-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="df9c2-111">공용 IP 주소로 Virtual Network Gateway를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="df9c2-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="df9c2-112">가상 $myGWsubnet 만들 가상 네트워크 내의 "GatewaySubnet"에서 **Get-AzVirtualNetworkSubnetConfig** cmdlet을 사용하여 변수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="df9c2-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="df9c2-113">변수 $myGWpip **New-AzPublicIpAddress** cmdlet을 사용하여 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df9c2-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="df9c2-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="df9c2-114">PARAMETERS</span></span>

### <span data-ttu-id="df9c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9c2-115">-DefaultProfile</span></span>
<span data-ttu-id="df9c2-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df9c2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df9c2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="df9c2-117">-Name</span></span>
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

### <span data-ttu-id="df9c2-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="df9c2-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="df9c2-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="df9c2-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="df9c2-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="df9c2-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="df9c2-121">-서브넷</span><span class="sxs-lookup"><span data-stu-id="df9c2-121">-Subnet</span></span>
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

### <span data-ttu-id="df9c2-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="df9c2-122">-SubnetId</span></span>
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

### <span data-ttu-id="df9c2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9c2-123">CommonParameters</span></span>
<span data-ttu-id="df9c2-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df9c2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9c2-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="df9c2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9c2-126">입력</span><span class="sxs-lookup"><span data-stu-id="df9c2-126">INPUTS</span></span>

### <span data-ttu-id="df9c2-127">없음</span><span class="sxs-lookup"><span data-stu-id="df9c2-127">None</span></span>

## <span data-ttu-id="df9c2-128">출력</span><span class="sxs-lookup"><span data-stu-id="df9c2-128">OUTPUTS</span></span>

### <span data-ttu-id="df9c2-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="df9c2-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="df9c2-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df9c2-130">NOTES</span></span>

## <span data-ttu-id="df9c2-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df9c2-131">RELATED LINKS</span></span>

[<span data-ttu-id="df9c2-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="df9c2-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="df9c2-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="df9c2-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
