---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverrequiredforresources
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
ms.openlocfilehash: 9aa09de52a6b731fbf57b309fb605c0ba07325da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000011"
---
# <span data-ttu-id="70374-101">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="70374-101">Get-AzResourceMoverRequiredForResources</span></span>

## <span data-ttu-id="70374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70374-102">SYNOPSIS</span></span>
<span data-ttu-id="70374-103">팔 리소스가 필요한 이동 리소스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="70374-103">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="70374-104">구문</span><span class="sxs-lookup"><span data-stu-id="70374-104">SYNTAX</span></span>

```
Get-AzResourceMoverRequiredForResources -MoveCollectionName <String> -ResourceGroupName <String>
 -SourceId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="70374-105">설명</span><span class="sxs-lookup"><span data-stu-id="70374-105">DESCRIPTION</span></span>
<span data-ttu-id="70374-106">팔 리소스가 필요한 이동 리소스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="70374-106">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="70374-107">예제</span><span class="sxs-lookup"><span data-stu-id="70374-107">EXAMPLES</span></span>

### <span data-ttu-id="70374-108">예제 1: 지정된 리소스를 추가하려면 추가해야 하는 필수 리소스 ARMID 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="70374-108">Example 1: Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>
```powershell
PS C:\> Get-AzResourceMoverRequiredForResources -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups"

/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="70374-109">지정된 리소스를 추가하려면 추가해야 하는 필수 리소스 ARMID 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="70374-109">Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>

## <span data-ttu-id="70374-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="70374-110">PARAMETERS</span></span>

### <span data-ttu-id="70374-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70374-111">-DefaultProfile</span></span>
<span data-ttu-id="70374-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70374-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70374-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="70374-113">-MoveCollectionName</span></span>
<span data-ttu-id="70374-114">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70374-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="70374-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70374-115">-ResourceGroupName</span></span>
<span data-ttu-id="70374-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70374-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="70374-117">-SourceId</span><span class="sxs-lookup"><span data-stu-id="70374-117">-SourceId</span></span>
<span data-ttu-id="70374-118">api가 호출되는 sourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="70374-118">The sourceId for which the api is invoked.</span></span>

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

### <span data-ttu-id="70374-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70374-119">-SubscriptionId</span></span>
<span data-ttu-id="70374-120">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="70374-120">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70374-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70374-121">CommonParameters</span></span>
<span data-ttu-id="70374-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70374-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70374-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70374-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70374-124">입력</span><span class="sxs-lookup"><span data-stu-id="70374-124">INPUTS</span></span>

## <span data-ttu-id="70374-125">출력</span><span class="sxs-lookup"><span data-stu-id="70374-125">OUTPUTS</span></span>

### <span data-ttu-id="70374-126">System.String</span><span class="sxs-lookup"><span data-stu-id="70374-126">System.String</span></span>

## <span data-ttu-id="70374-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="70374-127">NOTES</span></span>

<span data-ttu-id="70374-128">별칭</span><span class="sxs-lookup"><span data-stu-id="70374-128">ALIASES</span></span>

## <span data-ttu-id="70374-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70374-129">RELATED LINKS</span></span>

