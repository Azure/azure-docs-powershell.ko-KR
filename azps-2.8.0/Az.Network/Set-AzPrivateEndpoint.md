---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: afb61df71ce0cf0833f82868a7f3f345cf31b023
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872258"
---
# <span data-ttu-id="31a30-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="31a30-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="31a30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31a30-102">SYNOPSIS</span></span>
<span data-ttu-id="31a30-103">개인 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="31a30-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="31a30-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31a30-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31a30-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31a30-105">DESCRIPTION</span></span>
<span data-ttu-id="31a30-106">**AzPrivateEndpoint** cmdlet은 개인 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="31a30-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="31a30-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31a30-107">EXAMPLES</span></span>

### <span data-ttu-id="31a30-108">1: 개인 끝점을 만들고 해당 서브넷 중 하나를 다른 종점으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="31a30-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="31a30-109">이 예제에서는 서브넷이 하나인 개인 끝점을 만든 다음 가상 네트워크의 메모리 내 표현에서 다른 서브넷으로 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="31a30-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="31a30-110">그런 다음 서비스 쪽에서 수정 된 개인 끝점 상태를 쓰는 데 Set-PrivateEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31a30-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="31a30-111">변수</span><span class="sxs-lookup"><span data-stu-id="31a30-111">PARAMETERS</span></span>

### <span data-ttu-id="31a30-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31a30-112">-AsJob</span></span>
<span data-ttu-id="31a30-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="31a30-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31a30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a30-114">-DefaultProfile</span></span>
<span data-ttu-id="31a30-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31a30-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31a30-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="31a30-116">-PrivateEndpoint</span></span>
<span data-ttu-id="31a30-117">개인 끝점을 설정 해야 하는 상태를 나타내는 개인 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31a30-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

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

### <span data-ttu-id="31a30-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a30-118">CommonParameters</span></span>
<span data-ttu-id="31a30-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31a30-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a30-120">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31a30-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a30-121">입력</span><span class="sxs-lookup"><span data-stu-id="31a30-121">INPUTS</span></span>

### <span data-ttu-id="31a30-122">PSPrivateEndpoint에 대 한.</span><span class="sxs-lookup"><span data-stu-id="31a30-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="31a30-123">출력</span><span class="sxs-lookup"><span data-stu-id="31a30-123">OUTPUTS</span></span>

### <span data-ttu-id="31a30-124">PSPrivateEndpoint에 대 한.</span><span class="sxs-lookup"><span data-stu-id="31a30-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="31a30-125">상속자</span><span class="sxs-lookup"><span data-stu-id="31a30-125">NOTES</span></span>

## <span data-ttu-id="31a30-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31a30-126">RELATED LINKS</span></span>

[<span data-ttu-id="31a30-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="31a30-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="31a30-128">새로운 AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="31a30-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="31a30-129">제거-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="31a30-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


