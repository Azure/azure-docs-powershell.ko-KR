---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: 5bacd7c1b98bf7996ee8e6a8f7b188d67cf32073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016171"
---
# <span data-ttu-id="74dfc-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74dfc-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="74dfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="74dfc-103">개인 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74dfc-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="74dfc-104">구문</span><span class="sxs-lookup"><span data-stu-id="74dfc-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74dfc-105">설명</span><span class="sxs-lookup"><span data-stu-id="74dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="74dfc-106">**Set-AzPrivateEndpoint** cmdlet은 개인 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74dfc-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="74dfc-107">예제</span><span class="sxs-lookup"><span data-stu-id="74dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="74dfc-108">1: 개인 엔드포인트를 만들고 해당 서브넷 중 하나를 다른 엔드포인트로 바 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="74dfc-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="74dfc-109">이 예제에서는 하나의 서브넷이 있는 개인 엔드포인트를 만든 다음 가상 네트워크의 메모리 내 표현에서 다른 서브넷으로 바 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="74dfc-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="74dfc-110">그런 Set-PrivateEndpoint cmdlet은 서비스 쪽에서 수정된 개인 엔드포인트 상태를 작성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="74dfc-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="74dfc-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="74dfc-111">PARAMETERS</span></span>

### <span data-ttu-id="74dfc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74dfc-112">-AsJob</span></span>
<span data-ttu-id="74dfc-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="74dfc-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74dfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74dfc-114">-DefaultProfile</span></span>
<span data-ttu-id="74dfc-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74dfc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74dfc-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74dfc-116">-PrivateEndpoint</span></span>
<span data-ttu-id="74dfc-117">개인 엔드포인트를 설정해야 하는 상태를 나타내는 개인 엔드포인트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74dfc-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74dfc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74dfc-118">CommonParameters</span></span>
<span data-ttu-id="74dfc-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74dfc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74dfc-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74dfc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74dfc-121">입력</span><span class="sxs-lookup"><span data-stu-id="74dfc-121">INPUTS</span></span>

### <span data-ttu-id="74dfc-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74dfc-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="74dfc-123">출력</span><span class="sxs-lookup"><span data-stu-id="74dfc-123">OUTPUTS</span></span>

### <span data-ttu-id="74dfc-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74dfc-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="74dfc-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="74dfc-125">NOTES</span></span>

## <span data-ttu-id="74dfc-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74dfc-126">RELATED LINKS</span></span>

[<span data-ttu-id="74dfc-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74dfc-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="74dfc-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74dfc-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="74dfc-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74dfc-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


