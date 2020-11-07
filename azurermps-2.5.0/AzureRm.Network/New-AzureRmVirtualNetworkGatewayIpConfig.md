---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 1a043b14ef957eed6ac4983c4a30edf6fc72521f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882889"
---
# <span data-ttu-id="acdc9-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="acdc9-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="acdc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acdc9-102">SYNOPSIS</span></span>
<span data-ttu-id="acdc9-103">가상 네트워크 게이트웨이에 대 한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acdc9-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acdc9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="acdc9-104">SYNTAX</span></span>

### <span data-ttu-id="acdc9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="acdc9-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acdc9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="acdc9-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acdc9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="acdc9-107">DESCRIPTION</span></span>
<span data-ttu-id="acdc9-108">**AzureRmVirtualNetworkGatewayIpConfig** Cmdlet은 서브넷 ID 기반 (이전에 만든) 공용 IP 주소를 사용 하 여 가상 네트워크 게이트웨이에 할당 된 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acdc9-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="acdc9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="acdc9-109">EXAMPLES</span></span>

### <span data-ttu-id="acdc9-110">1: 가상 네트워크 게이트웨이에 대 한 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="acdc9-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="acdc9-111">공용 IP 주소를 사용 하 여 가상 네트워크 게이트웨이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="acdc9-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="acdc9-112">변수 $myGWsubnet는 가상 네트워크 게이트웨이를 만들려는 가상 네트워크 내의 " **AzureRmVirtualNetworkSubnetConfig** cmdlet을 사용 하 여 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="acdc9-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="acdc9-113">**AzureRmPublicIpAddress** cmdlet을 사용 하 여 변수 $myGWpip를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="acdc9-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="acdc9-114">변수</span><span class="sxs-lookup"><span data-stu-id="acdc9-114">PARAMETERS</span></span>

### <span data-ttu-id="acdc9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acdc9-115">-DefaultProfile</span></span>
<span data-ttu-id="acdc9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="acdc9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acdc9-117">-이름</span><span class="sxs-lookup"><span data-stu-id="acdc9-117">-Name</span></span>
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

### <span data-ttu-id="acdc9-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="acdc9-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="acdc9-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="acdc9-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="acdc9-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="acdc9-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="acdc9-121">-서브넷</span><span class="sxs-lookup"><span data-stu-id="acdc9-121">-Subnet</span></span>
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

### <span data-ttu-id="acdc9-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="acdc9-122">-SubnetId</span></span>
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

### <span data-ttu-id="acdc9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acdc9-123">CommonParameters</span></span>
<span data-ttu-id="acdc9-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="acdc9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acdc9-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acdc9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acdc9-126">입력</span><span class="sxs-lookup"><span data-stu-id="acdc9-126">INPUTS</span></span>

## <span data-ttu-id="acdc9-127">출력</span><span class="sxs-lookup"><span data-stu-id="acdc9-127">OUTPUTS</span></span>

### <span data-ttu-id="acdc9-128">PSVirtualNetworkGatewayIpConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="acdc9-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="acdc9-129">상속자</span><span class="sxs-lookup"><span data-stu-id="acdc9-129">NOTES</span></span>

## <span data-ttu-id="acdc9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="acdc9-130">RELATED LINKS</span></span>

