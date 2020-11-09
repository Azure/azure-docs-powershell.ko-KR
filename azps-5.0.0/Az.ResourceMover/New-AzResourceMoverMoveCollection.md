---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309925"
---
# <span data-ttu-id="f7a11-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f7a11-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="f7a11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7a11-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a11-103">이동 모음을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="f7a11-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f7a11-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f7a11-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f7a11-105">DESCRIPTION</span></span>
<span data-ttu-id="f7a11-106">이동 모음을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="f7a11-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f7a11-107">EXAMPLES</span></span>

### <span data-ttu-id="f7a11-108">예제 1: 새 Move collection을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="f7a11-109">구독 내에서 새 Move collection을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="f7a11-110">변수</span><span class="sxs-lookup"><span data-stu-id="f7a11-110">PARAMETERS</span></span>

### <span data-ttu-id="f7a11-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a11-111">-DefaultProfile</span></span>
<span data-ttu-id="f7a11-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7a11-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="f7a11-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="f7a11-114">Principal id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="f7a11-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="f7a11-115">-IdentityTenantId</span></span>
<span data-ttu-id="f7a11-116">테 넌 트 id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="f7a11-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f7a11-117">-IdentityType</span></span>
<span data-ttu-id="f7a11-118">지역 이동 서비스에 사용 되는 id 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-118">The type of identity used for the region move service.</span></span>

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

### <span data-ttu-id="f7a11-119">-위치</span><span class="sxs-lookup"><span data-stu-id="f7a11-119">-Location</span></span>
<span data-ttu-id="f7a11-120">리소스가 상주 하는 지리적 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="f7a11-121">-이름</span><span class="sxs-lookup"><span data-stu-id="f7a11-121">-Name</span></span>
<span data-ttu-id="f7a11-122">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="f7a11-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7a11-123">-ResourceGroupName</span></span>
<span data-ttu-id="f7a11-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="f7a11-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="f7a11-125">-SourceRegion</span></span>
<span data-ttu-id="f7a11-126">소스 영역을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="f7a11-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7a11-127">-SubscriptionId</span></span>
<span data-ttu-id="f7a11-128">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="f7a11-129">태그</span><span class="sxs-lookup"><span data-stu-id="f7a11-129">-Tag</span></span>
<span data-ttu-id="f7a11-130">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="f7a11-130">Resource tags.</span></span>

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

### <span data-ttu-id="f7a11-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="f7a11-131">-TargetRegion</span></span>
<span data-ttu-id="f7a11-132">대상 영역을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="f7a11-133">-확인</span><span class="sxs-lookup"><span data-stu-id="f7a11-133">-Confirm</span></span>
<span data-ttu-id="f7a11-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7a11-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7a11-135">-WhatIf</span></span>
<span data-ttu-id="f7a11-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7a11-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7a11-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a11-138">CommonParameters</span></span>
<span data-ttu-id="f7a11-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7a11-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a11-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f7a11-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a11-141">입력</span><span class="sxs-lookup"><span data-stu-id="f7a11-141">INPUTS</span></span>

## <span data-ttu-id="f7a11-142">출력</span><span class="sxs-lookup"><span data-stu-id="f7a11-142">OUTPUTS</span></span>

### <span data-ttu-id="f7a11-143">Api20191001Preview를 통해. a. i. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7a11-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="f7a11-144">상속자</span><span class="sxs-lookup"><span data-stu-id="f7a11-144">NOTES</span></span>

<span data-ttu-id="f7a11-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="f7a11-145">ALIASES</span></span>

## <span data-ttu-id="f7a11-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7a11-146">RELATED LINKS</span></span>

