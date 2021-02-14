---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183713"
---
# <span data-ttu-id="5a491-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="5a491-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="5a491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a491-102">SYNOPSIS</span></span>
<span data-ttu-id="5a491-103">이동 컬렉션을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="5a491-104">구문</span><span class="sxs-lookup"><span data-stu-id="5a491-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5a491-105">설명</span><span class="sxs-lookup"><span data-stu-id="5a491-105">DESCRIPTION</span></span>
<span data-ttu-id="5a491-106">이동 컬렉션을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="5a491-107">예제</span><span class="sxs-lookup"><span data-stu-id="5a491-107">EXAMPLES</span></span>

### <span data-ttu-id="5a491-108">예제 1: 새 이동 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="5a491-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="5a491-109">구독 내에서 새 이동 컬렉션을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="5a491-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a491-110">PARAMETERS</span></span>

### <span data-ttu-id="5a491-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a491-111">-DefaultProfile</span></span>
<span data-ttu-id="5a491-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a491-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="5a491-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="5a491-114">보안 주체 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="5a491-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="5a491-115">-IdentityTenantId</span></span>
<span data-ttu-id="5a491-116">테넌트 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="5a491-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5a491-117">-IdentityType</span></span>
<span data-ttu-id="5a491-118">지역 이동 서비스에 사용되는 ID 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-118">The type of identity used for the region move service.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.ResourceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a491-119">-Location</span><span class="sxs-lookup"><span data-stu-id="5a491-119">-Location</span></span>
<span data-ttu-id="5a491-120">리소스가 있는 지리적 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="5a491-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5a491-121">-Name</span></span>
<span data-ttu-id="5a491-122">컬렉션 이동 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-122">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a491-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a491-123">-ResourceGroupName</span></span>
<span data-ttu-id="5a491-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="5a491-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="5a491-125">-SourceRegion</span></span>
<span data-ttu-id="5a491-126">원본 지역을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="5a491-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a491-127">-SubscriptionId</span></span>
<span data-ttu-id="5a491-128">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-128">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a491-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a491-129">-Tag</span></span>
<span data-ttu-id="5a491-130">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="5a491-130">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a491-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="5a491-131">-TargetRegion</span></span>
<span data-ttu-id="5a491-132">대상 지역을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="5a491-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a491-133">-Confirm</span></span>
<span data-ttu-id="5a491-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a491-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a491-135">-WhatIf</span></span>
<span data-ttu-id="5a491-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5a491-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a491-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a491-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a491-138">CommonParameters</span></span>
<span data-ttu-id="5a491-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5a491-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a491-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5a491-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a491-141">입력</span><span class="sxs-lookup"><span data-stu-id="5a491-141">INPUTS</span></span>

## <span data-ttu-id="5a491-142">출력</span><span class="sxs-lookup"><span data-stu-id="5a491-142">OUTPUTS</span></span>

### <span data-ttu-id="5a491-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="5a491-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="5a491-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5a491-144">NOTES</span></span>

<span data-ttu-id="5a491-145">별칭</span><span class="sxs-lookup"><span data-stu-id="5a491-145">ALIASES</span></span>

## <span data-ttu-id="5a491-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a491-146">RELATED LINKS</span></span>

