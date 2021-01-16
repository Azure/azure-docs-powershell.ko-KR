---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7d90ffff788239996f7b79f7e56493611db86e04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344198"
---
# <span data-ttu-id="9f927-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9f927-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="9f927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f927-102">SYNOPSIS</span></span>
<span data-ttu-id="9f927-103">가상 네트워크에서 서브넷 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9f927-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="9f927-104">구문</span><span class="sxs-lookup"><span data-stu-id="9f927-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f927-105">설명</span><span class="sxs-lookup"><span data-stu-id="9f927-105">DESCRIPTION</span></span>
<span data-ttu-id="9f927-106">**Remove-AzVirtualNetworkSubnetConfig** cmdlet은 Azure 가상 네트워크에서 서브넷을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9f927-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="9f927-107">예제</span><span class="sxs-lookup"><span data-stu-id="9f927-107">EXAMPLES</span></span>

### <span data-ttu-id="9f927-108">1: 가상 네트워크에서 서브넷 제거 및 가상 네트워크 업데이트</span><span class="sxs-lookup"><span data-stu-id="9f927-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="9f927-109">이 예제에서는 두 개의 서브넷이 있는 리소스 그룹 및 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f927-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="9f927-110">그런 다음 Remove-AzVirtualNetworkSubnetConfig 명령을 사용하여 가상 네트워크의 메모리 내 표현에서 백end 서브넷을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9f927-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="9f927-111">Set-AzVirtualNetwork 서버 쪽에서 가상 네트워크를 수정하기 위해 호출됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f927-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="9f927-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f927-112">PARAMETERS</span></span>

### <span data-ttu-id="9f927-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f927-113">-DefaultProfile</span></span>
<span data-ttu-id="9f927-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f927-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f927-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9f927-115">-Name</span></span>
<span data-ttu-id="9f927-116">제거할 서브넷 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f927-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="9f927-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9f927-117">-VirtualNetwork</span></span>
<span data-ttu-id="9f927-118">제거할 서브넷 구성을 포함하는 **VirtualNetwork** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f927-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f927-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f927-119">CommonParameters</span></span>
<span data-ttu-id="9f927-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9f927-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f927-121">자세한 내용은 [about_CommonParameters]를 http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9f927-121">For more information, see [about_CommonParameters] (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f927-122">입력</span><span class="sxs-lookup"><span data-stu-id="9f927-122">INPUTS</span></span>

### <span data-ttu-id="9f927-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9f927-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9f927-124">출력</span><span class="sxs-lookup"><span data-stu-id="9f927-124">OUTPUTS</span></span>

### <span data-ttu-id="9f927-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9f927-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9f927-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f927-126">NOTES</span></span>

## <span data-ttu-id="9f927-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f927-127">RELATED LINKS</span></span>

[<span data-ttu-id="9f927-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9f927-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9f927-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9f927-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9f927-130">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9f927-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9f927-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9f927-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


