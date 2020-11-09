---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309934"
---
# <span data-ttu-id="7a9ae-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="7a9ae-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="7a9ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7a9ae-103">해결 되지 않은 종속성의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a9ae-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="7a9ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a9ae-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7a9ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7a9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="7a9ae-106">해결 되지 않은 종속성의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a9ae-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="7a9ae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7a9ae-107">EXAMPLES</span></span>

### <span data-ttu-id="7a9ae-108">예제 1: 확인 되지 않은 종속 리소스 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="7a9ae-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="7a9ae-109">이동 모음에 대 한 확인 되지 않은 종속 리소스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a9ae-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="7a9ae-110">변수</span><span class="sxs-lookup"><span data-stu-id="7a9ae-110">PARAMETERS</span></span>

### <span data-ttu-id="7a9ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a9ae-111">-DefaultProfile</span></span>
<span data-ttu-id="7a9ae-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a9ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a9ae-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="7a9ae-113">-MoveCollectionName</span></span>
<span data-ttu-id="7a9ae-114">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a9ae-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="7a9ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a9ae-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a9ae-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a9ae-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="7a9ae-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a9ae-117">-SubscriptionId</span></span>
<span data-ttu-id="7a9ae-118">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7a9ae-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="7a9ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a9ae-119">CommonParameters</span></span>
<span data-ttu-id="7a9ae-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a9ae-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7a9ae-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a9ae-122">입력</span><span class="sxs-lookup"><span data-stu-id="7a9ae-122">INPUTS</span></span>

## <span data-ttu-id="7a9ae-123">출력</span><span class="sxs-lookup"><span data-stu-id="7a9ae-123">OUTPUTS</span></span>

### <span data-ttu-id="7a9ae-124">Api20191001Preview. IUnresolvedDependencyCollection에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7a9ae-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="7a9ae-125">상속자</span><span class="sxs-lookup"><span data-stu-id="7a9ae-125">NOTES</span></span>

<span data-ttu-id="7a9ae-126">별칭과</span><span class="sxs-lookup"><span data-stu-id="7a9ae-126">ALIASES</span></span>

## <span data-ttu-id="7a9ae-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a9ae-127">RELATED LINKS</span></span>

