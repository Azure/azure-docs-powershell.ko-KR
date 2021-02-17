---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 023d50aaf32d894722e2167737703d24776a1fd5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193337"
---
# <span data-ttu-id="4cbb4-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4cbb4-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="4cbb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cbb4-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbb4-103">가상 네트워크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbb4-103">Updates a virtual network.</span></span>

## <span data-ttu-id="4cbb4-104">구문</span><span class="sxs-lookup"><span data-stu-id="4cbb4-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cbb4-105">설명</span><span class="sxs-lookup"><span data-stu-id="4cbb4-105">DESCRIPTION</span></span>
<span data-ttu-id="4cbb4-106">**Set-AzVirtualNetwork** cmdlet은 가상 네트워크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbb4-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="4cbb4-107">예제</span><span class="sxs-lookup"><span data-stu-id="4cbb4-107">EXAMPLES</span></span>

### <span data-ttu-id="4cbb4-108">1: 가상 네트워크를 만들고 해당 서브넷 중 하나를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbb4-108">1: Creates a virtual network and removes one of its subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus ## Create resource group 
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create frontend subnet 
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="4cbb4-109">이 예제에서는 두 개의 서브넷인 frontendSubnet 및 backendSubnet을 통해 TestResourceGroup이라는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4cbb4-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="4cbb4-110">그런 다음 가상 네트워크의 메모리 내 표현에서 backendSubnet 서브넷을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbb4-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="4cbb4-111">그런 Set-AzVirtualNetwork cmdlet은 서비스 쪽에서 수정된 가상 네트워크 상태를 작성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cbb4-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="4cbb4-112">Set-AzVirtualNetwork cmdlet이 실행되면 backendSubnet이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cbb4-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="4cbb4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cbb4-113">PARAMETERS</span></span>

### <span data-ttu-id="4cbb4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cbb4-114">-AsJob</span></span>
<span data-ttu-id="4cbb4-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4cbb4-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cbb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbb4-116">-DefaultProfile</span></span>
<span data-ttu-id="4cbb4-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cbb4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cbb4-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4cbb4-118">-VirtualNetwork</span></span>
<span data-ttu-id="4cbb4-119">가상 네트워크를 설정해야 하는 상태를 나타내는 가상 네트워크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbb4-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="4cbb4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbb4-120">CommonParameters</span></span>
<span data-ttu-id="4cbb4-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbb4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbb4-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4cbb4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbb4-123">입력</span><span class="sxs-lookup"><span data-stu-id="4cbb4-123">INPUTS</span></span>

### <span data-ttu-id="4cbb4-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4cbb4-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4cbb4-125">출력</span><span class="sxs-lookup"><span data-stu-id="4cbb4-125">OUTPUTS</span></span>

### <span data-ttu-id="4cbb4-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4cbb4-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4cbb4-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4cbb4-127">NOTES</span></span>

## <span data-ttu-id="4cbb4-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cbb4-128">RELATED LINKS</span></span>

[<span data-ttu-id="4cbb4-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4cbb4-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="4cbb4-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4cbb4-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="4cbb4-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4cbb4-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="4cbb4-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4cbb4-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


