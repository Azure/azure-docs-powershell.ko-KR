---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 34cae1bcc6020e2e0c2a8b2f6b70e302c8576f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999995"
---
# <span data-ttu-id="d6c4a-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="d6c4a-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="d6c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c4a-103">해결되지 않은 종속성 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="d6c4a-104">구문</span><span class="sxs-lookup"><span data-stu-id="d6c4a-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DependencyLevel <DependencyLevel>] [-Filter <String>] [-Orderby <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d6c4a-105">설명</span><span class="sxs-lookup"><span data-stu-id="d6c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="d6c4a-106">해결되지 않은 종속성 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="d6c4a-107">예제</span><span class="sxs-lookup"><span data-stu-id="d6c4a-107">EXAMPLES</span></span>

### <span data-ttu-id="d6c4a-108">예제 1: 이동 컬렉션에 대한 해결되지 않은 종속 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-108">Example 1: Get list of unresolved dependent resources for a Move Collection.</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -DependencyLevel Descendant
Count Id                                                                                                                                        
----- --                                                                                                                                        
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111   
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
    3 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm
```

<span data-ttu-id="d6c4a-109">이동 컬렉션에 대한 해결되지 않은 종속 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-109">Get a list of unresolved dependent resources for a Move Collection.</span></span>

## <span data-ttu-id="d6c4a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d6c4a-110">PARAMETERS</span></span>

### <span data-ttu-id="d6c4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6c4a-111">-DefaultProfile</span></span>
<span data-ttu-id="d6c4a-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6c4a-113">-DependencyLevel</span><span class="sxs-lookup"><span data-stu-id="d6c4a-113">-DependencyLevel</span></span>
<span data-ttu-id="d6c4a-114">종속성 수준을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-114">Defines the dependency level.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.DependencyLevel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c4a-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="d6c4a-115">-Filter</span></span>
<span data-ttu-id="d6c4a-116">작업에 적용할 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-116">The filter to apply on the operation.</span></span>
<span data-ttu-id="d6c4a-117">예를 들어 $apply=filter(eq 2 계산).</span><span class="sxs-lookup"><span data-stu-id="d6c4a-117">For example, $apply=filter(count eq 2).</span></span>

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

### <span data-ttu-id="d6c4a-118">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="d6c4a-118">-MoveCollectionName</span></span>
<span data-ttu-id="d6c4a-119">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-119">The Move Collection Name.</span></span>

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

### <span data-ttu-id="d6c4a-120">-Orderby</span><span class="sxs-lookup"><span data-stu-id="d6c4a-120">-Orderby</span></span>
<span data-ttu-id="d6c4a-121">쿼리에 따라 OData 순서 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-121">OData order by query option.</span></span>
<span data-ttu-id="d6c4a-122">예를 들어 $orderby=Count desc를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-122">For example, you can use $orderby=Count desc.</span></span>

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

### <span data-ttu-id="d6c4a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6c4a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6c4a-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="d6c4a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6c4a-125">-SubscriptionId</span></span>
<span data-ttu-id="d6c4a-126">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="d6c4a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c4a-127">CommonParameters</span></span>
<span data-ttu-id="d6c4a-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d6c4a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c4a-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6c4a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c4a-130">입력</span><span class="sxs-lookup"><span data-stu-id="d6c4a-130">INPUTS</span></span>

## <span data-ttu-id="d6c4a-131">출력</span><span class="sxs-lookup"><span data-stu-id="d6c4a-131">OUTPUTS</span></span>

### <span data-ttu-id="d6c4a-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="d6c4a-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span></span>

## <span data-ttu-id="d6c4a-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d6c4a-133">NOTES</span></span>

<span data-ttu-id="d6c4a-134">별칭</span><span class="sxs-lookup"><span data-stu-id="d6c4a-134">ALIASES</span></span>

## <span data-ttu-id="d6c4a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6c4a-135">RELATED LINKS</span></span>

