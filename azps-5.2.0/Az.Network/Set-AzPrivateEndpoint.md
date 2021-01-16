---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: c90332967621d4dad35594cc5080143d42a47693
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344162"
---
# <span data-ttu-id="e6f2a-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6f2a-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="e6f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f2a-103">개인 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="e6f2a-104">구문</span><span class="sxs-lookup"><span data-stu-id="e6f2a-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6f2a-105">설명</span><span class="sxs-lookup"><span data-stu-id="e6f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="e6f2a-106">**Set-AzPrivateEndpoint** cmdlet은 개인 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="e6f2a-107">예제</span><span class="sxs-lookup"><span data-stu-id="e6f2a-107">EXAMPLES</span></span>

### <span data-ttu-id="e6f2a-108">1: 개인 엔드포인트를 만들고 해당 서브넷 중 하나를 다른 엔드포인트로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="e6f2a-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="e6f2a-109">이 예제에서는 하나의 서브넷이 있는 개인 엔드포인트를 만든 다음 가상 네트워크의 메모리 내 표현에서 다른 서브넷으로 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="e6f2a-110">그런 Set-PrivateEndpoint cmdlet은 서비스 쪽에서 수정된 개인 엔드포인트 상태를 작성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="e6f2a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6f2a-111">PARAMETERS</span></span>

### <span data-ttu-id="e6f2a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6f2a-112">-AsJob</span></span>
<span data-ttu-id="e6f2a-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e6f2a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6f2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f2a-114">-DefaultProfile</span></span>
<span data-ttu-id="e6f2a-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6f2a-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6f2a-116">-PrivateEndpoint</span></span>
<span data-ttu-id="e6f2a-117">개인 엔드포인트를 설정해야 하는 상태를 나타내는 개인 엔드포인트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

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

### <span data-ttu-id="e6f2a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f2a-118">CommonParameters</span></span>
<span data-ttu-id="e6f2a-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f2a-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f2a-121">입력</span><span class="sxs-lookup"><span data-stu-id="e6f2a-121">INPUTS</span></span>

### <span data-ttu-id="e6f2a-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6f2a-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="e6f2a-123">출력</span><span class="sxs-lookup"><span data-stu-id="e6f2a-123">OUTPUTS</span></span>

### <span data-ttu-id="e6f2a-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6f2a-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="e6f2a-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e6f2a-125">NOTES</span></span>

## <span data-ttu-id="e6f2a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6f2a-126">RELATED LINKS</span></span>

[<span data-ttu-id="e6f2a-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6f2a-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="e6f2a-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6f2a-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="e6f2a-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6f2a-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


