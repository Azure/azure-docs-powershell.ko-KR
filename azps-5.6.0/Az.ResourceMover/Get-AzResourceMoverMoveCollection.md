---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: a10ac77515b225c5e5ef06335f9cee1e99ecd3b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000043"
---
# <span data-ttu-id="2eb19-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="2eb19-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="2eb19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eb19-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb19-103">이동 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2eb19-103">Gets the move collection.</span></span>

## <span data-ttu-id="2eb19-104">구문</span><span class="sxs-lookup"><span data-stu-id="2eb19-104">SYNTAX</span></span>

### <span data-ttu-id="2eb19-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="2eb19-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2eb19-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="2eb19-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2eb19-107">List1</span><span class="sxs-lookup"><span data-stu-id="2eb19-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2eb19-108">설명</span><span class="sxs-lookup"><span data-stu-id="2eb19-108">DESCRIPTION</span></span>
<span data-ttu-id="2eb19-109">이동 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2eb19-109">Gets the move collection.</span></span>

## <span data-ttu-id="2eb19-110">예제</span><span class="sxs-lookup"><span data-stu-id="2eb19-110">EXAMPLES</span></span>

### <span data-ttu-id="2eb19-111">예제 1: 구독의 모든 이동 컬렉션에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="2eb19-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"270119e0-0000-0c00-0000-5f5c94940000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"39015ed4-0000-0c00-0000-5f5ce2760000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections
"1000b505-0000-0c00-0000-5f69db6e0000" centraluseuap MoveCollection-cus-eus-ccy         Microsoft.Migrate/moveCollections


```

<span data-ttu-id="2eb19-112">구독의 모든 이동 컬렉션에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2eb19-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="2eb19-113">예제 2: 구독에서 지정된 이동 컬렉션 이름으로 이동 컬렉션에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="2eb19-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PS-centralus-westcentralus-demoRMS"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="2eb19-114">구독에서 지정된 이동 컬렉션 이름으로 이동 컬렉션에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2eb19-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="2eb19-115">예제 3: 구독에서 지정된 리소스 그룹 이름으로 이동 컬렉션에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="2eb19-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"4e02b0a9-0000-0c00-0000-5fd101cc0000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="2eb19-116">구독에서 지정된 리소스 그룹 이름으로 컬렉션 이동에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2eb19-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="2eb19-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2eb19-117">PARAMETERS</span></span>

### <span data-ttu-id="2eb19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb19-118">-DefaultProfile</span></span>
<span data-ttu-id="2eb19-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb19-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb19-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2eb19-120">-Name</span></span>
<span data-ttu-id="2eb19-121">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb19-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb19-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb19-122">-ResourceGroupName</span></span>
<span data-ttu-id="2eb19-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb19-123">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb19-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2eb19-124">-SubscriptionId</span></span>
<span data-ttu-id="2eb19-125">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb19-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="2eb19-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb19-126">CommonParameters</span></span>
<span data-ttu-id="2eb19-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb19-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb19-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2eb19-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb19-129">입력</span><span class="sxs-lookup"><span data-stu-id="2eb19-129">INPUTS</span></span>

## <span data-ttu-id="2eb19-130">출력</span><span class="sxs-lookup"><span data-stu-id="2eb19-130">OUTPUTS</span></span>

### <span data-ttu-id="2eb19-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="2eb19-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="2eb19-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2eb19-132">NOTES</span></span>

<span data-ttu-id="2eb19-133">별칭</span><span class="sxs-lookup"><span data-stu-id="2eb19-133">ALIASES</span></span>

## <span data-ttu-id="2eb19-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2eb19-134">RELATED LINKS</span></span>

