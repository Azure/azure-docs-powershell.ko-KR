---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201900"
---
# <span data-ttu-id="5c735-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="5c735-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="5c735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c735-102">SYNOPSIS</span></span>
<span data-ttu-id="5c735-103">해결되지 않은 종속성 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c735-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="5c735-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c735-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5c735-105">설명</span><span class="sxs-lookup"><span data-stu-id="5c735-105">DESCRIPTION</span></span>
<span data-ttu-id="5c735-106">해결되지 않은 종속성 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c735-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="5c735-107">예제</span><span class="sxs-lookup"><span data-stu-id="5c735-107">EXAMPLES</span></span>

### <span data-ttu-id="5c735-108">예제 1: 해결되지 않은 종속 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="5c735-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="5c735-109">이동 컬렉션에 대해 해결되지 않은 종속 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c735-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="5c735-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c735-110">PARAMETERS</span></span>

### <span data-ttu-id="5c735-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c735-111">-DefaultProfile</span></span>
<span data-ttu-id="5c735-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c735-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c735-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="5c735-113">-MoveCollectionName</span></span>
<span data-ttu-id="5c735-114">컬렉션 이동 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c735-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="5c735-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c735-115">-ResourceGroupName</span></span>
<span data-ttu-id="5c735-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c735-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="5c735-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c735-117">-SubscriptionId</span></span>
<span data-ttu-id="5c735-118">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5c735-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="5c735-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c735-119">CommonParameters</span></span>
<span data-ttu-id="5c735-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c735-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c735-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c735-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c735-122">입력</span><span class="sxs-lookup"><span data-stu-id="5c735-122">INPUTS</span></span>

## <span data-ttu-id="5c735-123">출력</span><span class="sxs-lookup"><span data-stu-id="5c735-123">OUTPUTS</span></span>

### <span data-ttu-id="5c735-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="5c735-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="5c735-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c735-125">NOTES</span></span>

<span data-ttu-id="5c735-126">별칭</span><span class="sxs-lookup"><span data-stu-id="5c735-126">ALIASES</span></span>

## <span data-ttu-id="5c735-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c735-127">RELATED LINKS</span></span>

