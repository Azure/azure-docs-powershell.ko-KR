---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: 58ba131ab0bebc65d8fd5259d24b2846da229721
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491725"
---
# <span data-ttu-id="a55aa-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a55aa-101">Get-AzPeering</span></span>

## <span data-ttu-id="a55aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a55aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a55aa-103">구독에 대한 피어링 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a55aa-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="a55aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="a55aa-104">SYNTAX</span></span>

### <span data-ttu-id="a55aa-105">BySubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="a55aa-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a55aa-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="a55aa-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a55aa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a55aa-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a55aa-108">설명</span><span class="sxs-lookup"><span data-stu-id="a55aa-108">DESCRIPTION</span></span>
<span data-ttu-id="a55aa-109">구독, 리소스 그룹 또는 이름으로 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a55aa-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="a55aa-110">예제</span><span class="sxs-lookup"><span data-stu-id="a55aa-110">EXAMPLES</span></span>

### <span data-ttu-id="a55aa-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a55aa-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeering

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}

Name                 : ContosoSeattlePeering
Sku                  : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringSku
Kind                 : Direct
Connections          : {99999}
UseForPeeringService : False
PeerAsn              : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSSubResource
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions/resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="a55aa-112">구독에 대한 모든 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a55aa-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="a55aa-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a55aa-113">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceGroupName test -Name myExchangePeering1

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="a55aa-114">명명된 Exchange 피어링을 얻습니다. `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="a55aa-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="a55aa-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="a55aa-115">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceId $resourceId

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="a55aa-116">리소스 ID에 따라 명명된 Exchange `myExchangePeering1` 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a55aa-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="a55aa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a55aa-117">PARAMETERS</span></span>

### <span data-ttu-id="a55aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a55aa-118">-DefaultProfile</span></span>
<span data-ttu-id="a55aa-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a55aa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a55aa-120">-Kind</span><span class="sxs-lookup"><span data-stu-id="a55aa-120">-Kind</span></span>
<span data-ttu-id="a55aa-121">종류에 따라 모든 피어링 리소스를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a55aa-121">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a55aa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a55aa-122">-Name</span></span>
<span data-ttu-id="a55aa-123">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a55aa-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a55aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a55aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="a55aa-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a55aa-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a55aa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a55aa-126">-ResourceId</span></span>
<span data-ttu-id="a55aa-127">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a55aa-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a55aa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a55aa-128">CommonParameters</span></span>
<span data-ttu-id="a55aa-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a55aa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a55aa-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a55aa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a55aa-131">입력</span><span class="sxs-lookup"><span data-stu-id="a55aa-131">INPUTS</span></span>

### <span data-ttu-id="a55aa-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a55aa-132">System.String</span></span>

## <span data-ttu-id="a55aa-133">출력</span><span class="sxs-lookup"><span data-stu-id="a55aa-133">OUTPUTS</span></span>

### <span data-ttu-id="a55aa-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="a55aa-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a55aa-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a55aa-135">NOTES</span></span>

## <span data-ttu-id="a55aa-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a55aa-136">RELATED LINKS</span></span>
