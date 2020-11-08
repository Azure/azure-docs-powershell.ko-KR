---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204454"
---
# <span data-ttu-id="95d39-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="95d39-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="95d39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d39-102">SYNOPSIS</span></span>
<span data-ttu-id="95d39-103">이동 컬렉션에서 이동 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="95d39-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95d39-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="95d39-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95d39-105">DESCRIPTION</span></span>
<span data-ttu-id="95d39-106">이동 컬렉션에서 이동 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="95d39-107">예제의</span><span class="sxs-lookup"><span data-stu-id="95d39-107">EXAMPLES</span></span>

### <span data-ttu-id="95d39-108">예제 1: 이동 컬렉션에서 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="95d39-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="95d39-109">지정 된 구독 내의 이동 컬렉션에서 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="95d39-110">변수</span><span class="sxs-lookup"><span data-stu-id="95d39-110">PARAMETERS</span></span>

### <span data-ttu-id="95d39-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95d39-111">-AsJob</span></span>
<span data-ttu-id="95d39-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="95d39-112">Run the command as a job</span></span>

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

### <span data-ttu-id="95d39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d39-113">-DefaultProfile</span></span>
<span data-ttu-id="95d39-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95d39-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="95d39-115">-MoveCollectionName</span></span>
<span data-ttu-id="95d39-116">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="95d39-117">-이름</span><span class="sxs-lookup"><span data-stu-id="95d39-117">-Name</span></span>
<span data-ttu-id="95d39-118">이동 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d39-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="95d39-119">-NoWait</span></span>
<span data-ttu-id="95d39-120">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="95d39-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="95d39-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95d39-121">-PassThru</span></span>
<span data-ttu-id="95d39-122">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="95d39-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d39-123">-ResourceGroupName</span></span>
<span data-ttu-id="95d39-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="95d39-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95d39-125">-SubscriptionId</span></span>
<span data-ttu-id="95d39-126">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="95d39-127">-확인</span><span class="sxs-lookup"><span data-stu-id="95d39-127">-Confirm</span></span>
<span data-ttu-id="95d39-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d39-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d39-129">-WhatIf</span></span>
<span data-ttu-id="95d39-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95d39-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d39-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d39-132">CommonParameters</span></span>
<span data-ttu-id="95d39-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d39-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95d39-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d39-135">입력</span><span class="sxs-lookup"><span data-stu-id="95d39-135">INPUTS</span></span>

## <span data-ttu-id="95d39-136">출력</span><span class="sxs-lookup"><span data-stu-id="95d39-136">OUTPUTS</span></span>

### <span data-ttu-id="95d39-137">Api20191001Preview를 통해. PowerShell. a. i. i a m-IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="95d39-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="95d39-138">상속자</span><span class="sxs-lookup"><span data-stu-id="95d39-138">NOTES</span></span>

<span data-ttu-id="95d39-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="95d39-139">ALIASES</span></span>

## <span data-ttu-id="95d39-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95d39-140">RELATED LINKS</span></span>

